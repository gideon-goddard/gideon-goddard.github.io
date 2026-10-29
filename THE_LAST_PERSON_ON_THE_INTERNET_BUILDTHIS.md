# THE LAST PERSON ON THE INTERNET
## BuildThis — Product and Experience Specification

**Tagline:** There can only be one. Unfortunately.

**Project type:** A live, full-screen, interactive elimination bracket for public AT Protocol identities.

**Primary directive:** Build the actual working experience, not a static mockup. Every indexed DID participates in a real, reproducible single-elimination tournament. Run elimination and visual playback as fast as practical while keeping the interface responsive.

---

## 1. The premise

The internet is reduced to one person. Then it happens again.

A huge tournament bracket contains the DIDs of publicly discoverable Bluesky accounts. Every match eliminates one DID. There are no avatars, profiles, popularity scores, posts, follower counts, or engagement-based judgments. The system does not know what anyone has said. It only knows that they exist.

At the beginning, the bracket is impossibly dense. It races through millions of eliminations. The geometry collapses toward one remaining line. The final DID is displayed with bureaucratic solemnity. A new tournament begins, seeded from the previous winner.

The comedy should be dry, impersonal, and faintly horrifying. No cartoon death, gore, sound effects of violence, or goofy gamer styling. The joke is the enormous seriousness applied to an arbitrary procedure.

## 2. Non-negotiable product requirements

1. **DID-native:** Use full AT Protocol DIDs as identity keys. Handles are not necessary for competition or display. Never rely on handles as stable IDs.
2. **Real bracket:** Every DID in a frozen tournament roster must have a genuine bracket position and a traceable path through actual matches. Do not fake the participant count or animate fabricated results.
3. **One winner:** For N entrants, run exactly N−1 matches and produce exactly one winner (for N ≥ 1). Handle N = 0 and N = 1 explicitly.
4. **Deterministic:** Given the same canonical roster snapshot, tournament seed, algorithm version, and bracket rules, results must be identical across runs and machines.
5. **Fast:** Compute matches without network calls and independently of rendering. Process as quickly as the environment permits; the renderer must remain responsive.
6. **Massive visualization:** Display a true tournament bracket with scalable, GPU-friendly or canvas-based level-of-detail rendering. Never mount millions of DOM nodes.
7. **Discoverable identities:** Support a real, deduplicated DID index sourced from public AT Protocol/Bluesky data. Show coverage and freshness honestly; never claim to contain every Bluesky user unless independently verified.
8. **Search:** A visitor can enter a DID and locate its bracket position, round of elimination, opponent, and path to the winner. Optional handle-to-DID resolution is a convenience only.
9. **Automatic cycles:** After a champion is declared, launch another tournament, using a documented seed derived from the previous winner and previous tournament metadata.
10. **Inspectable:** Publish tournament metadata, algorithm version, roster count, seed commitment, timing, and winner; permit verification/replay.

## 3. Visual identity

The site should feel like a forgotten institutional computer built to oversee an extinction event: early scientific computing, black-and-white plotting equipment, Cold War monitoring displays, restrained CRT typography. Museum-quality, not cheesy retro parody.

- Nearly black background, thin off-white lines, restrained red for eliminated branches, pale green or white for surviving paths.
- Monospaced typography. Minimal motion blur; precise geometry.
- Huge numeric counter: `12,491,822 IDENTITIES → 1 SURVIVOR`.
- The bracket fills nearly the entire viewport, with an unobtrusive overlay for controls.
- At distant zoom, branches are aggregated into dense geometric bands; at close zoom, show real match nodes and truncated DIDs, with the full DID accessible on selection.
- Eliminated branches dim, surviving paths remain visible. Avoid expensive individual particle effects.
- Use subtle, optional sound only; default muted. Respect reduced-motion preferences.
- Responsive desktop and mobile layouts, keyboard navigation, high-contrast text, accessible search and controls.

### Opening state

**THE LAST PERSON ON THE INTERNET**

`INDEXED IDENTITIES: 12,491,822` *(actual number only)*  
`TOURNAMENT #000001`  
`STATUS: ELIMINATION IN PROGRESS`

A dense, apparently endless bracket stretches across the screen. A small live readout displays matches processed, surviving identities, current round, computation time, and rendering rate.

### Champion state

**YOU HAVE WON THE INTERNET.**

`did:plc:...` *(full actual DID)*

*There is nobody left to congratulate you.*

Show the exact tournament ID, starting population, number of eliminations, and elapsed computation time. Then reset after a short, configurable interval. Allow a visitor to pause the automatic restart.

## 4. Core tournament rules

### Entrants and bracket structure

- Freeze a canonical, immutable roster for each tournament; sort and deduplicate full DIDs in a documented order.
- Assign stable integer entrant indices within the snapshot; use integers in the hot path.
- Create a standard single-elimination bracket. For non-power-of-two entrant counts, use deterministic, documented byes. A bye advances a participant but is **not** a match or elimination.
- Never silently add or remove participants during a tournament. Newly indexed DIDs join subsequent tournaments.
- Choose a deterministic seeding/shuffle strategy that is not biased by DID lexicographic order.

### Match outcomes

All participants have equal a priori chances; social popularity does not affect outcomes.

Use a versioned, deterministic, unbiased or negligibly biased pseudorandom selection method based on the tournament seed and match identity. A cryptographic hash-based derivation is acceptable; a high-performance deterministic PRNG is acceptable if its exact algorithm, seeding, and execution order are specified. Do **not** use `Math.random()` as the authoritative source of results.

Specify a canonical encoding of match coordinates (round and match position) so replay is independent of parallel execution order. The winner of a match must be one of its two actual entrants. Ensure no byes are counted as wins over an opponent.

### Tournament chaining

Tournament 1 uses a published initial seed. Each next tournament derives its seed using a versioned hash of the previous tournament seed, previous champion DID, and previous tournament ID. Preserve a record of the chain. Make it clear this is deterministic entertainment, not a secure lottery or contest for prizes.

### Performance

- N entrants require N−1 played matches; a bracket with byes must still satisfy this invariant.
- Use compact arrays, typed arrays, workers, or a backend native engine as appropriate.
- No per-match API requests; no repeated DID parsing in the hot loop.
- Keep authoritative simulation state separate from the display timeline.
- Batch progress messages instead of sending one message per elimination.
- Benchmark with 100,000; 1,000,000; and 10,000,000 synthetic DIDs or equivalent indexed participants. Report actual timings rather than promising fixed throughput.
- Avoid retaining a separate heavyweight object for each match. Store only the data needed to reconstruct paths and results.

## 5. Rendering and interaction

The bracket must be a *real geometric representation* of the tournament, not a fake animated background.

- Use Canvas/WebGL/WebGPU where supported, with graceful fallback.
- Implement level of detail: draw individual nodes and labels only when legible; aggregate remote branches at wide zoom.
- Support smooth pan, wheel/pinch zoom, fit-all, jump-to-finals, and jump-to-DID.
- Keep the main thread responsive; render only what is visible or appropriately aggregated.
- Use requestAnimationFrame for presentation and adapt animation work to device capability.
- Expose **MAX SPEED** (default), **PAUSE**, **REPLAY**, and **STEP ROUND** controls. The computation can finish ahead of the visualization; do not falsely imply a match was computed at the moment its animation appears.
- Max speed means advance the *presentation* as quickly as frames can convey meaningful state. It is acceptable to skip intermediate visual states; never skip actual matches.
- Make final 64 slowdown an **optional toggle**, not a mandatory cinematic delay.
- Show truthful `SIMULATION COMPLETE` status if results have already been calculated while playback is catching up.

### Search and inspect

Enter a DID to:

1. Find the entrant in the frozen roster.
2. Zoom to its real bracket location.
3. Highlight its wins and elimination (or championship).
4. Show opponents and the exact round of elimination.
5. Follow the path of the DID that eliminated it through subsequent rounds.
6. Copy a permalink identifying the tournament snapshot and DID.

If the DID was not indexed, say **NOT IN THIS TOURNAMENT'S ROSTER**. Do not pretend it was eliminated. Optional handle resolution must clearly distinguish resolution failure from roster absence.

## 6. Public AT Protocol identity indexing

A DID is a stable identifier, but a DID alone does **not** prove an account belongs to Bluesky, is active, or is currently accessible. Build the registry with explicit provenance.

- Discover public Bluesky/AT Protocol identities from appropriate public account indexes, repository events, and/or documented APIs.
- Persist unique DIDs, first-seen/last-seen times, source provenance, and relevant account state when available.
- Handle deletions, takedowns, deactivations, and DID migrations where observable. Clearly document what the roster includes and excludes.
- Do not rely on the live event stream alone to produce a complete historical roster.
- Avoid profile fetches, post ingestion, or follower graph collection unless needed for identity discovery; the game itself does not use them.
- Use compliant rate limits, backoff, durable checkpoints, incremental sync, and recovery after interruptions.
- Display `INDEXED PUBLIC DIDS` rather than `ALL BLUESKY USERS` unless full coverage is established.
- The app must work before the live index is complete: ship a clearly labeled synthetic-data demo mode and an actual-data mode. **Never mix synthetic identities into a real tournament without prominently saying so.**

## 7. Information architecture

**Primary screen:** Full-viewport bracket, counters, playback controls, DID search.

**Inspection panel:** Selected DID, bracket coordinates, opponents, result, elimination path, permalink.

**Archive:** Past tournaments with champion DID, roster snapshot identifier, seed, algorithm version, entrants, matches, duration, and replay link. Store summaries durably; choose a retention policy for full bracket data and make archival limitations clear.

**About / Method:** Plain explanation of DID discovery, coverage limits, bracket rules, deterministic selection, simulation/rendering separation, and data handling.

Avoid account registration, wallets, tokens, leaderboards based on social popularity, and unrelated social features.

## 8. Copy and tone

Keep language terse and clinical.

- `POPULATION REDUCTION IN PROGRESS`
- `8,192,000 IDENTITIES REMAIN`
- `NO INTERVENTION IS POSSIBLE`
- `THE FINAL MATCH HAS BEEN RESOLVED`
- `ONE IDENTITY REMAINS`
- `YOU HAVE WON THE INTERNET.`
- `THERE IS NOBODY LEFT TO CONGRATULATE YOU.`
- `REPOPULATING...`

Never imply real accounts have died or are being threatened. The interface is a fictional elimination of bracket entries, not people.

## 9. Implementation expectations for BuildThis

Choose an architecture that can deliver the product in stages without replacing the tournament engine:

**Phase A — Working prototype:** Synthetic DID roster, deterministic real bracket, fast tournament engine, responsive bracket rendering, zoom/pan, DID search, champion screen, restart, tests.

**Phase B — Real identities:** Durable public DID index, provenance and freshness indicators, immutable roster snapshots, actual-data tournament mode, recovery and incremental updates.

**Phase C — Scale and polish:** Millions of entries, LOD GPU rendering, performance profiling, archive/replay, accessible interaction, mobile optimization, robust deployment.

Do not block the prototype on obtaining millions of real DIDs. Make the distinction between demo and real data unmistakable.

### Tests and acceptance criteria

- For entrant counts 0, 1, 2, 3, 7, 8, 9, 100, and large randomized counts, verify bracket integrity and correct bye handling.
- For every N ≥ 1, exactly N−1 matches are played and exactly one champion remains.
- Every match winner was an actual entrant in that match; no DID is eliminated twice.
- Replaying the same snapshot, seed, and version produces bit-for-bit identical bracket results.
- Different worker counts and batch sizes do not change outcomes.
- Search resolves exact bracket paths and correctly reports absent DIDs.
- Zoomed-out rendering does not create per-entrant DOM nodes; frame rate and memory are measured on target devices.
- Stress-test a 10-million-entrant tournament and report computation time, peak memory, browser frame responsiveness, and archive size separately.
- Verify indexing resumes from checkpoints and deduplicates identities.
- Test keyboard, touch, reduced-motion, and small-screen usability.
- Include automated tests for all core rules and run them before delivery. Report failures and remaining limitations rather than claiming unsupported scale.

## 10. Final instruction

**Build the experience.** Prioritize a working, mathematically correct, reproducible tournament and an extraordinary zoomable bracket over decorative dashboards or speculative features. The central image should be unforgettable: millions of thin lines, extinguishing almost instantaneously, until a single DID remains.

**There is nobody left to congratulate you.**
