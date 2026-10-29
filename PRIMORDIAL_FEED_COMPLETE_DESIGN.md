# THE PRIMORDIAL FEED
## A Living Ecology of Public Information
### Comprehensive Concept, Product, Experience, and Simulation Design Document

**Document status:** Foundational design proposal  
**Version:** 1.0  
**Scope:** Product vision, interaction design, information ecology, simulation behavior, visual identity, editorial philosophy, ethics, and experience requirements.  
**Explicitly out of scope:** Code, frameworks, infrastructure, APIs, database schemas, deployment, algorithms expressed as executable procedures, and implementation schedules.

---

# 1. The Proposition

The Primordial Feed is a living aquarium of public social information. Posts arriving from Bluesky enter the aquarium as organisms. Each organism possesses traits derived from the content and context of its source post. These traits shape how it moves, feeds, competes, cooperates, reproduces, ages, and dies within a bounded artificial ecology.

The aquarium does not simply animate an existing feed ranking. It **creates a new way to select information**: the feed is a view of organisms that have survived ecological pressures, not a list of posts awarded a predetermined relevance score.

The visitor watches information behave as life. Ideas crowd into niches, imitate one another, exhaust shared resources, form temporary alliances, proliferate, become prey, and disappear. A post can thrive without popularity. A popular post can collapse after consuming its niche. A tiny, unfamiliar idea can persist for hours while a wave of nearly identical posts burns out in minutes.

**Core proposition:** *What would a social feed look like if information had to live somewhere?*

The site has two equally important identities:

1. **A public artificial-life experiment.** A legible, evolving ecology whose phenomena are worth observing even without opening a single post.
2. **An alternative discovery instrument.** A feed of original posts selected through the ecological consequences of their properties and relationships.

Neither identity should be sacrificed to the other. A beautiful aquarium that only disguises engagement ranking fails. A novel ranking experiment with no compelling living world also fails.

## 1.1 Foundational commitments

- **Ecology before ranking.** Fitness is an outcome of living in the tank, not an input score.
- **Information is material.** Words, concepts, structure, relationships, and novelty must influence organism behavior.
- **Scarcity is real within the fiction.** Energy, space, food, and attention are finite; not everything survives.
- **Life is local and relational.** The meaning of a trait depends on the current environment and neighboring organisms.
- **Survival is not truth.** Ecological success is not evidence of factual correctness, moral worth, or public importance.
- **Visibility is not endorsement.** The site must never imply that a surviving post is verified or recommended as safe.
- **Every visible outcome should be explainable.** Visitors should be able to learn the meaningful causes of an organism's fate.
- **Source fidelity matters.** Every organism remains traceable to its actual source post. Simulated descendants must never masquerade as authored posts.
- **The tank should surprise its designers.** Avoid hand-authoring winners or forcing predetermined storylines.
- **Observation should be rewarding.** The ecosystem should be interesting in motion, in history, and in the resulting feed.

## 1.2 What this is not

The Primordial Feed is not a conventional social network, a replacement for Bluesky, a popularity contest, a scientific model of human intelligence, a truth detector, a personality test, a generative-post machine, or a battle royale with arbitrary winners. It is not a promise that evolution will naturally produce quality content. It is an experiment in ecological information selection, presented as an observable public world.

---

# 2. The Intended Experience

A visitor arrives to find a dark, luminous tank already alive. Hundreds of small entities drift, pursue, cluster, divide, pulse, or vanish. The tank is not waiting for the visitor to start it. Its activity conveys that a much larger stream of public information is passing through a limited world.

A compact strip of observations gives context: the living population, recent arrivals, deaths, dominant niches, and notable events. The visitor can select a creature and discover the original post, its inherited traits, its ecological history, its diet, its rivals, and the reason it remains alive. A companion feed lists the posts represented by surviving organisms. Switching from the feed to the tank should feel like moving between an ecological field guide and the ecosystem itself.

Within the first minute, the visitor should understand three things:

1. These creatures correspond to real posts.
2. They are actually interacting under persistent rules.
3. Their survival affects what appears in the feed.

Within ten minutes, the visitor should notice at least one surprising phenomenon: a colony, a sudden die-off, an isolated survivor, a bloom, a predator, or an unexpectedly resilient organism.

On returning later, the visitor should find a changed world with a discoverable history, rather than an unrelated animation that resets without consequence.

## 2.1 Desired emotional register

The tone is **scientific, eerie, dryly funny, and quietly absurd**. The site should evoke an old natural-history museum exhibit, a microscopy laboratory, and a forgotten artificial-life program. It should not resemble a mobile game economy, a cheerful gamified dashboard, or a corporate AI demo.

The joke is that the internet has been reduced to a nutrient broth. The site should not explain this joke too loudly.

Suggested microcopy:

- “The tank is experiencing a topical bloom.”
- “This organism has outlived 98% of its cohort.”
- “Three nearly identical organisms competed for the same nutrients. One remains.”
- “Cause of death: starvation.”
- “No organisms currently occupy this niche.”
- “Popularity did not prevent extinction.”
- “A colony has formed around a new concept.”
- “The ecosystem is not a measure of truth.”

Avoid celebratory language such as “Your post won!” or “Top creator dominates the tank.”

---

# 3. The World Model

## 3.1 The tank

A **tank** is a bounded, persistent ecological world. It has limited capacity, shared resources, environmental conditions, a population, a history, and a set of stable biological laws. Incoming posts do not enter an empty stage; they arrive in a world already shaped by previous inhabitants.

The tank must be finite. Without limits, the ecology becomes an endless particle visualization in which scarcity has no meaning. Its boundaries can be visually soft, but the consequences of limited room and limited nourishment must be unmistakable.

## 3.2 The organism

An **organism** is the ecological embodiment of one original post. Its source identity does not change. It has a birth, a lifetime, an internal condition, relationships, and possibly a death. It can produce simulated descendants, but those descendants do not represent new posts from the author.

The organism has two distinct layers:

- **Source identity:** the original post, author attribution, timestamp, text, and available context.
- **Ecological identity:** its traits, condition, location, behavior, lineage, interactions, and history in this particular tank.

The same source post could lead to different fates in different tank conditions. That variability is a feature, not an error.

## 3.3 The environment

The environment is not a passive backdrop. It contains distributions of nutrients, zones of competition, waste, ecological opportunities, and changing conditions. Incoming information changes the environment even when its organism dies quickly.

A useful guiding metaphor is a pond ecosystem, not a boxing arena. Organisms do not need to attack constantly. Many should survive through efficient metabolism, scavenging, symbiosis, or occupying niches others ignore.

## 3.4 The feed

The **survival feed** is a readable collection of source posts corresponding to organisms that satisfy a selected ecological view. The feed is a window into the tank, not an independent ranking system with an ecological theme pasted over it.

## 3.5 The archive

The **archive** records births, interactions, lineages, environmental changes, and deaths. It allows the ecosystem to be understood over time. An extinction is not an erasure of historical existence, although source deletion and privacy obligations take precedence over archival curiosity.

---

# 4. The Biological Vocabulary

The project needs a precise shared language to avoid metaphor drifting into contradictory mechanics.

| Concept | Meaning in this world | What it must not imply |
|---|---|---|
| Genome | Stable traits derived from a source post at birth | A claim about the author's genetics or character |
| Phenotype | Observable form and behavior shaped by genome and environment | A permanent label of content quality |
| Energy | Capacity to remain active and survive | A direct synonym for likes |
| Nutrient | Environmental resource usable by organisms with compatible traits | A measure of factual truth |
| Niche | A pattern of resources and relationships an organism can exploit | A fixed editorial category |
| Predation | One organism gains resources at another's expense | A moral judgment against the consumed post |
| Competition | Multiple organisms draw on overlapping scarce resources | An arbitrary winner-takes-all comparison |
| Symbiosis | Organisms improve one another's prospects | Proof their authors agree |
| Colony | A persistent group whose members share ecological consequences | A fabricated conversation |
| Reproduction | An organism produces a simulated descendant | A real Bluesky repost or authored publication |
| Mutation | Variation within simulated descendants or phenotype | Changing the original post's words |
| Senescence | Age-related decline in resilience or efficiency | Automatic invalidation of older ideas |
| Decomposition | Dead organisms return some resources to the world | Permanent preservation of deleted content |
| Fitness | Observed success under specific environmental conditions | An assigned universal score |
| Extinction | Disappearance of a lineage or niche from the living population | Erasure of a topic from public discourse |
| Bloom | Rapid expansion of a population or niche | Necessarily meaningful popularity |

These definitions should appear in a concise public field guide and remain consistent throughout the product.

---

# 5. Translating Posts into Living Traits

The most important design decision is not how organisms look. It is how public information becomes biology without collapsing back into a disguised engagement score.

A post's characteristics should influence several **independent traits** with benefits and costs. No single feature should be universally good. Long text might provide rich resources but demand more energy. Repetition might improve camouflage within a colony but increase competition for identical food. Novelty might open a niche but reduce compatibility with existing nutrient pools.

## 5.1 Candidate source characteristics

- Length and density of text.
- Vocabulary variety and repetition.
- Presence of questions, assertions, quotations, or structured lists.
- Language and script, without treating one language as biologically superior.
- Conceptual overlap with other currently living posts.
- Novel combinations of otherwise familiar terms.
- References to links, images, or other media, where available and appropriate.
- Relationship to reply threads and repost contexts.
- Topic continuity with the recent environment.
- Available public interaction signals, treated as context rather than a universal food supply.
- Time since publication and time since entry to the tank, which are different quantities.

The design should explicitly resist mapping demographic identity, presumed intelligence, personal worth, political affiliation, or sensitive personal attributes to superior biological traits.

## 5.2 Candidate organism traits

### Body mass

Affects space requirements, visibility, and nutritional needs. Larger bodies may resist certain predators but starve more easily. A longer post may have a larger body, but the mapping should not imply that verbosity equals strength.

### Metabolic rate

Determines how quickly energy is spent and how actively an organism searches for resources. High metabolism creates bursts of activity and risk; low metabolism favors endurance and patience.

### Dietary specialization

Describes which environmental resources an organism can use efficiently. Specialists thrive in narrow conditions; generalists survive changing environments but may be less efficient at any single resource.

### Sensory range

Determines the breadth of nearby resources, organisms, or ecological signals the organism can detect. Broad sensing is useful but costly.

### Mobility

Controls how rapidly an organism can move through the tank and whether it can migrate when a niche collapses. Movement consumes energy.

### Armor or resistance

Represents resilience to predation or environmental stress. Defense must have a cost, such as reduced mobility or higher maintenance needs.

### Adhesion

Determines the ability to form persistent colonies or mutually beneficial associations. Strong adhesion can help in scarcity but trap an organism in a failing group.

### Reproductive investment

Determines how much energy an organism can devote to descendants. Fast reproduction can produce short-lived blooms; slower reproduction can preserve resources for survival.

### Lifespan potential

Sets the general shape of aging, but should not make longevity entirely predetermined. Environment and behavior still matter.

### Novelty tolerance

Represents whether an organism can exploit unusual resources or unfamiliar neighborhoods. Novelty may be opportunity or danger depending on the tank.

## 5.3 Trait tradeoffs are mandatory

Every major advantage must carry a meaningful cost or contextual weakness. A trait system with universal advantages becomes a hidden scoring system. The design should invite ecological diversity: small scavengers, slow specialists, short-lived opportunists, colonial generalists, and large predators should all have plausible survival strategies.

## 5.4 Source traits versus acquired traits

Stable inherited traits should be distinguished from conditions gained through experience. An organism may be born with a dietary preference but acquire injury, energy reserves, symbiotic partners, or learned ecological advantages. The original post never changes because the organism changes.

## 5.5 Unknown information

Missing context should not be interpreted as weakness. A post with little interaction data, a non-English post, or a post without external media should remain a viable ecological participant. The world must not punish absent metadata as though it were a negative attribute.

---

# 6. Energy, Nutrients, and Scarcity

Energy is the central survival constraint. It is acquired through feeding and spent through metabolism, movement, defense, reproduction, and other activity. Organisms that cannot meet their costs eventually become inactive and die.

The tank should have **multiple resource types** rather than one universal energy pool. This allows niches to emerge. Different information characteristics can correspond to different ecological resources, and organisms can be differently equipped to exploit them.

## 6.1 Nutrient families

Potential resource families include:

- **Topical nutrients:** resources associated with recurring concepts and subjects.
- **Lexical nutrients:** resources associated with particular word patterns or linguistic structures.
- **Novelty nutrients:** temporary opportunities created by genuinely uncommon combinations.
- **Context nutrients:** resources arising from conversational or relational structure.
- **Detritus:** recyclable material released through death, abandonment, or exhausted blooms.

These are ecological constructs, not labels of merit.

## 6.2 Resource regeneration

Resources must renew, but not without limit. A niche may recover after heavy consumption. New posts may introduce new resources. Decaying organisms may enrich areas that previously seemed barren. Environmental conditions may temporarily favor some resource families over others.

## 6.3 Avoiding popularity as food

Likes, reposts, and replies may be allowed to affect particular traits or environmental pressures, but they should not serve as a continuously replenished universal energy supply. Otherwise highly engaged posts gain an automatic survival advantage and the ecology merely ratifies conventional popularity.

## 6.4 The meaning of starvation

Starvation means the organism could not secure sufficient resources in its local environment under its current costs. It does **not** mean the original post was uninteresting, inaccurate, or worthless.

---

# 7. Feeding and Predation

Predation is the project's most visually legible and philosophically provocative behavior. It should also be the most carefully designed.

## 7.1 What makes prey?

A plausible default is **resource overlap**. Organisms that depend on similar information resources are likely to compete, and under certain conditions one can consume the other. This gives predation an intelligible relationship to information redundancy: posts occupying similar niches are especially likely to encounter one another.

However, similarity must not automatically imply predation. Similar organisms might cooperate, ignore one another, or become competitors depending on their traits, energy state, relative size, local scarcity, and existing relationships.

## 7.2 The act of consumption

A successful predatory event should have visible stages: encounter, pursuit or engagement, transfer of resources, and ecological consequence. It should not resemble a random instant deletion.

Predation should not always be lethal. Partial consumption can weaken prey, allow escape, or change subsequent behavior. Lethal predation should be consequential and rare enough to remain meaningful.

## 7.3 Redundancy without censorship

If a hundred near-identical posts enter the tank, it is plausible that most cannot occupy the same niche indefinitely. Yet the tank must avoid assuming that one survivor is the authoritative representative of an event. Multiple perspectives may be meaningfully different despite lexical similarity.

## 7.4 Scavenging

Some organisms should specialize in resources released by death or discarded activity. Scavengers prevent the ecosystem from becoming a simple hierarchy of predators and prey. Their existence also makes death generative: the remains of one informational moment can sustain a different one.

## 7.5 Predation explanations

An organism's history should describe the meaningful reason for a predatory outcome in plain language: shared nutrient dependence, local scarcity, a defensive disadvantage, or an energetic opportunity. “The algorithm chose a winner” is not an acceptable explanation.

---

# 8. Cooperation, Symbiosis, and Colonies

A system containing only solitary competition will likely become visually repetitive and conceptually shallow. Cooperation should be a first-class ecological possibility.

## 8.1 Mutualism

Two organisms may gain a survival advantage through proximity or complementary resource use. For example, a specialist that efficiently transforms one resource may sustain a neighbor that consumes its byproducts.

## 8.2 Commensalism

One organism may benefit from another's presence without substantially helping or harming it. This allows opportunistic ecological relationships that are not friendships or rivalries.

## 8.3 Parasitism

An organism may extract resources from a host without immediately killing it. Parasites can thrive during booms and collapse when their hosts disappear.

## 8.4 Colony formation

Colonies should arise from repeated compatible interactions, not merely from sharing a hashtag. They may pool protection, modify the local environment, or create a new ecological niche. Membership should be contingent and reversible.

## 8.5 Colony identity

A colony may have a name derived from its dominant informational features, but that label is an observational convenience. The interface must not invent an author, consensus statement, or collective opinion for a group of posts.

## 8.6 Colony collapse

Colonies should be vulnerable to overspecialization, nutrient depletion, parasites, internal competition, and changing environmental conditions. A massive colony should be impressive but never permanently unbeatable.

---

# 9. Reproduction, Inheritance, and Mutation

Reproduction makes the world evolutionary rather than merely competitive. It also introduces the greatest risk of confusing simulated entities with actual social posts.

## 9.1 What reproduces?

An organism may generate a **simulated descendant** that inherits some ecological traits and varies in others. Descendants are explicitly artificial. They are not reposts, replies, quotes, or new writings by the source author.

## 9.2 What persists?

A lineage is an ecological history anchored to a source post. A descendant may retain the source association while having its own organism identity, birth time, and fate. The interface should always distinguish original source organisms from simulated descendants.

## 9.3 Mutation

Mutation changes ecological traits, not the text or meaning of the source post. Variation should be bounded enough for ancestry to remain intelligible, but sufficient to permit new strategies and unexpected adaptations.

## 9.4 Reproduction costs

Reproduction should require substantial resources or expose the parent to risk. Otherwise fast reproduction becomes an automatic victory condition.

## 9.5 Population accounting

The site must distinguish **living organisms**, **unique source posts**, and **living lineages**. One successful source post could have many descendants. A feed should not become filled with repeated copies of that same post simply because its lineage reproduced successfully.

## 9.6 Recommended feed rule

For the default survival feed, show a source post at most once. Its descendants contribute to its ecological history and may influence whether its lineage is considered extant, but they do not create duplicate feed cards.

---

# 10. Aging, Death, and Decomposition

Death is necessary to make selection meaningful, but it should not become a visual punishment for authors.

## 10.1 Causes of death

- Starvation after sustained resource scarcity.
- Fatal predation.
- Senescence after a long life.
- Environmental stress beyond the organism's resilience.
- Colony collapse or loss of essential symbiotic support.
- Reproductive exhaustion.

A source post removed or made unavailable for policy or source-state reasons should **exit the display through a distinct administrative state**, not be described as biologically defeated.

## 10.2 The moment of death

Death should be visually clear without being grotesque: dimming, fragmentation, dissolution, or sinking into detritus. It should be possible to follow the transfer of matter back into the environment.

## 10.3 Historical remembrance

A tombstone or specimen record may show lifetime, ecological role, descendants, major interactions, and cause of death. It must never imply that the author or the underlying idea has died in the real world.

## 10.4 Natural turnover

A healthy tank should have regular births and deaths. Permanent survival should be exceptional. Yet forced expiration purely to keep the screen fresh would undermine the ecology; longevity should be an actual outcome of the rules.

---

# 11. Ecological Niches and Species

A niche is not simply a topic label. It is a set of environmental opportunities and dependencies. Two posts about the same subject may occupy different niches if their structures, relationships, or resource strategies differ. Posts about different subjects may share a niche if they exploit similar ecological opportunities.

## 11.1 Species as an emergent classification

A species should be a descriptive grouping of organisms with related ecological strategies, not a rigid taxonomy assigned by the site at birth. The grouping may evolve as the population changes.

Possible observational labels include:

- Fast-blooming opportunists.
- Slow metabolic generalists.
- Specialized detritivores.
- Colonial symbionts.
- High-mobility predators.
- Resource-efficient solitary survivors.

These names describe the simulation, not the people who wrote the posts.

## 11.2 Topic versus species

A topic such as astronomy is not itself a species. Astronomy posts could support many different species. Conversely, a scavenging species could contain posts from many unrelated topics.

## 11.3 Invasive species

An arriving lineage may expand rapidly into niches previously occupied by others. This should be observable as an ecological phenomenon, without framing the underlying people or communities as invasive.

## 11.4 Biodiversity

The tank's diversity should be meaningful. A world where a single organism type dominates forever is less informative and less compelling. The design should allow diversity to emerge through different survival strategies, rather than guaranteeing a politically or topically predetermined balance.

---

# 12. Environmental Events and Long-Term Dynamics

The aquarium should have recognizable ecological weather without becoming a scripted disaster game.

## 12.1 Blooms

A burst of similar incoming information can enrich a niche, allowing rapid population growth. Blooms may be followed by depletion, predation, or collapse.

## 12.2 Droughts

A decline in certain resource types can make previously successful specialists vulnerable. Droughts should arise from understandable environmental conditions, not random punishment.

## 12.3 Succession

After a collapse, different organisms may occupy the vacant niche. A dead dominant lineage can create opportunities for smaller competitors.

## 12.4 Ecological cascades

The loss of one important organism or colony may indirectly affect others through nutrient availability, predation, and symbiosis. The interface should surface such chains when they are significant.

## 12.5 Regime shifts

Over time, the tank may transition from one dominant ecological structure to another. These transitions should be observable historically and not necessarily treated as progress.

## 12.6 No artificial drama requirement

The site should not fabricate predation, extinctions, or sudden crises merely to entertain visitors. Periods of relative stability are valid and can be visually beautiful.

---

# 13. Admission and the Problem of Scale

The Bluesky stream contains far more information than a visitor can meaningfully watch. The tank therefore needs an explicit **admission philosophy**, distinct from ecological selection.

## 13.1 Admission is not survival

Some incoming posts may never enter a particular tank. This is a sampling or eligibility decision, not an ecological death. The interface must not conflate these states.

## 13.2 Fair entry principles

Admission should avoid systematically favoring already popular accounts, English-language posts, familiar topics, or content with abundant metadata. It should not reward authors for manipulating post frequency.

## 13.3 Capacity and cohorts

The tank should maintain a bounded living population. Visitors should be able to understand how many source posts are being represented and that the aquarium is a sample of a much larger public stream.

## 13.4 Separate worlds

Future tanks might explore different conditions: a general public pond, a technology pond, a language-specific pond, or a historically bounded specimen tank. These are different ecological environments, not separate universal rankings of human worth.

## 13.5 Recommended initial experience

Begin conceptually with **one canonical public tank** and one clear survival feed. Multiple tanks should be a later product extension, after the behavior and meaning of a single world are understandable.

---

# 14. The Survival Feed

The survival feed must be useful even to visitors who never watch the aquarium. It should contain recognizable source posts, clear attribution, enough context to interpret the content, and a compact explanation of ecological status.

## 14.1 Default view

**Living survivors** is the default editorial view. It shows distinct source posts associated with currently living organisms or extant lineages, with a clear indication of which definition is in use.

## 14.2 Feed modes

| View | What it reveals | Essential caveat |
|---|---|---|
| Longest-lived | Posts whose organisms have survived the longest | Age is not accuracy |
| Recent survivors | New arrivals that remain alive after initial exposure | Newness is not novelty |
| Predator records | Organisms with consequential predatory histories | Predation is not virtue |
| Resilient specialists | Organisms surviving in narrow or scarce niches | Specialization is contextual |
| Unusual survivors | Organisms occupying rare ecological strategies | Unusual is not automatically valuable |
| Successful lineages | Source posts associated with persistent descendant populations | Descendants are simulated |
| Colony members | Posts participating in durable ecological groups | A colony is not a shared viewpoint |
| Recent extinctions | Posts whose organisms recently died | Extinction is not a content verdict |

## 14.3 What a feed card contains

- Original post text or an appropriate excerpt.
- Source author and a link to the original post.
- Publication time, distinct from ecological birth time.
- Organism visual identity.
- Ecological age and current condition.
- Niche or species descriptor, where meaningful.
- A one-sentence explanation of its survival status.
- A way to locate the organism in the aquarium.
- A way to inspect its history.

The feed must not visually suggest that the site itself authored the original content.

## 14.4 Why this survived

A visitor should be able to expand a short explanation, such as:

> “This organism survived by using a low-demand nutrient niche. Its nearest competitors exhausted their reserves during a local bloom.”

The explanation should refer to observed ecological events, not an opaque universal quality label.

## 14.5 Avoiding repeated winners

The feed should not let one prolific author or one reproducing lineage monopolize the screen simply because it produces many source posts or descendants. Any diversity or repetition controls should be disclosed as **presentation rules**, not passed off as natural selection.

---

# 15. The Aquarium Interface

## 15.1 First impression

The aquarium is the primary visual object. It should feel deep, alive, and spatially coherent. A dark field supports delicate luminous organisms, resource clouds, subtle trails, and occasional bursts of ecological activity.

The tank should not look like a screensaver of randomly wandering dots. Organisms need distinctive movement, recognizable relationships, and visible responses to environmental conditions.

## 15.2 Spatial organization

The tank may contain gradients, patches, currents, nutrient-rich zones, dead zones, and colony structures. Spatial differences should have ecological meaning. They should not merely organize posts by arbitrary screen coordinates.

## 15.3 Organism visual grammar

Organisms should be recognizable without reading labels. Shape, motion, internal texture, edge quality, and color can communicate traits or ecological roles. However, no single color should stand for content quality, truth, or author worth.

Possible visual relationships:

- Larger bodies: greater mass and maintenance burden.
- Pulsation rate: metabolic activity.
- Filaments or cilia: mobility or sensing.
- Membranes: defensive specialization.
- Tendrils: adhesion or symbiosis.
- Faint halos: nutrient uptake or local influence.
- Budding structures: reproduction.
- Fragmentation: death and decomposition.

## 15.4 Movement

Movement should be purposeful enough to read but irregular enough to feel alive. Predators should not chase continuously; scavengers should respond to detritus; colonies should exhibit cohesion without becoming rigid icons.

## 15.5 Environmental visibility

Nutrient fields should be visible in an optional layer. The default view can be atmospheric, but visitors should be able to reveal enough environmental structure to understand why organisms congregate in particular areas.

## 15.6 Labels

The default tank should avoid covering every organism with text. Labels appear on selection, focus, or meaningful events. A calm field of life is preferable to a crowded dashboard.

---

# 16. Interaction Design

## 16.1 Observe

A visitor can simply watch. The default state should be compelling without requiring a tutorial, login, or any action.

## 16.2 Inspect

Selecting an organism reveals its original post, biological profile, current condition, lineage, and recent interactions. The selected creature remains visibly identified within the tank.

## 16.3 Follow

A visitor can follow an organism's movements and major events. Following is an observation mode, not an intervention that improves the organism's fitness.

## 16.4 Compare

Two organisms can be compared in terms of traits, niches, life histories, and ecological strategies. The comparison must avoid presenting a single authoritative “better post” score.

## 16.5 Explore history

Visitors can examine previous ecological moments and notable events. Historical views must be clearly distinguished from the live world.

## 16.6 Find a post

A visitor may search for an eligible source post or source author to discover whether it entered the tank and what happened. If it was never admitted, the interface should say so plainly rather than invent a death.

## 16.7 Observe without controlling

The canonical tank should not let visitors pay, vote, or click to feed their favorite organisms. Such intervention would turn the ecosystem into an attention game and compromise its selection premise.

## 16.8 Experimental interaction

A separate sandbox might eventually let visitors vary ecological conditions. Its results must never be confused with the canonical public survival feed.

---

# 17. Navigation and Information Architecture

The site should have a small number of conceptually distinct destinations.

### The Tank

The living world, current events, selected organisms, and environmental layers.

### Survivors

The readable source-post feed, with ecological sorting and explanations.

### Field Guide

A concise illustrated explanation of organisms, traits, resources, niches, interactions, and selection philosophy.

### Specimens

Detailed organism and lineage histories, including extinct specimens where source availability permits.

### Chronicle

A history of notable blooms, collapses, migrations, colony formations, and long-lived survivors.

### About the Experiment

A transparent account of what the site does, what it does not claim, the role of source data, known biases, and limitations.

The visitor should be able to move from a post in Survivors to its creature in the Tank and back without losing context.

---

# 18. Specimen Profiles

A specimen profile should feel like a natural-history record of a real informational event.

## 18.1 Profile anatomy

**Identity:** source post, author, original publication time, ecological birth time.  
**Classification:** observed niche, current species or strategy grouping, lineage.  
**Morphology:** visible traits and their source-derived influences.  
**Condition:** energy state, age, injury or stress, reproductive state.  
**Diet:** principal resource types and recent feeding.  
**Relationships:** prey, predators, symbionts, colony members, descendants.  
**Life history:** major encounters, migrations, reproduction, and environmental changes.  
**Status:** living, dead, unavailable at source, or otherwise removed from display.

## 18.2 Explanatory narrative

The profile should turn simulation history into readable natural history without inventing subjective intent. For example, “The organism moved into a nutrient-rich patch” is appropriate; “The author desperately sought attention” is not.

## 18.3 Death records

If dead, show its ecological cause of death and age. If unavailable for non-ecological reasons, say so without fabricating a biological cause.

---

# 19. Visual Identity and Art Direction

## 19.1 Aesthetic thesis

**A natural-history instrument from an alternate history of computing.** The visual language should combine restrained laboratory typography, dark microscopy, subtle phosphor glow, and the precise melancholy of older scientific software.

## 19.2 Reference qualities

- Microscopy, plankton, protozoa, rotifers, and microbial colonies.
- Museum specimen labels and scientific illustration.
- Early artificial-life experiments and old simulation displays.
- Subtle CRT persistence and analog instrument panels.
- Understated editorial layouts that respect original post content.

These are directional references, not instructions to imitate a particular copyrighted interface.

## 19.3 Palette

The world should begin with charcoal, near-black blue, muted gray, and off-white. Biological accents may include cold cyan, pale green, amber, violet, and subdued coral. Color should communicate ecology consistently and remain distinguishable without relying on hue alone.

## 19.4 Typography

Use legible editorial typography for reading posts, with a restrained technical or monospaced voice for specimen identifiers, measurements, and event logs. Avoid excessive pseudo-scientific decoration.

## 19.5 Motion

Motion is essential but must be meaningful. Organisms should pulse, drift, orient, and respond to contact. Transitions should be soft, with moments of sudden activity justified by ecological events. Offer reduced-motion and still-image alternatives.

## 19.6 Sound

Sound should be optional and off by default. If present, it should evoke an ambient laboratory rather than a video game. Important events must never require audio to understand.

## 19.7 Naming and voice

“The Primordial Feed” is a working name. Other possibilities include **The Tank**, **Infusoria**, **The Information Pond**, **The Petri Feed**, **Microfeed**, **The Broth**, and **Natural Selection**. The final name should feel like a curious scientific artifact, not a startup pitch.

---

# 20. Live Events and the Chronicle

The ecosystem needs a way to make long-term changes visible to people who do not watch continuously.

## 20.1 Event categories

- New organism born.
- Predation event.
- First reproduction in a lineage.
- Colony formed or dissolved.
- Rapid population bloom.
- Significant local nutrient depletion.
- Major extinction or die-off.
- Unusually long-lived specimen.
- Niche succession or ecological regime shift.

## 20.2 Event significance

Not every collision deserves a notification. The Chronicle should highlight events with substantial consequences, unusual patterns, or strong explanatory value. Its editorial selection criteria must be distinct from the organisms' survival mechanics.

## 20.3 Narration style

Use precise, dry, observational language. Do not anthropomorphize posts as if they consciously intend to kill, cooperate, or dominate. The humor should emerge from the discrepancy between mundane social posts and grand biological descriptions.

## 20.4 Daily and historical views

A daily field report could summarize the tank's ecological condition: total births and deaths, biodiversity changes, notable survivors, dominant resource families, and surprising collapses. It should describe what happened, not declare which ideas deserved to win.

---

# 21. The Observer's Understanding

The system must be explainable without becoming a textbook.

## 21.1 Three layers of explanation

**Immediate:** “This post is alive because its organism continues to secure sufficient nutrients.”  
**Contextual:** “It is a low-metabolism specialist in a sparsely populated niche.”  
**Detailed:** “Its recent feeding, resource scarcity, competition, and survival history.”

## 21.2 What the system can legitimately claim

It can say that an organism survived longer than its cohort, consumed another organism, joined a colony, or exploited a scarce resource. It can say that these results emerged from the rules of a particular artificial world.

## 21.3 What the system cannot claim

It cannot infer that a surviving post is true, important, original in an absolute sense, ethically superior, more intelligent, or deserving of greater human attention. It cannot claim the simulation reproduces biological evolution or real social dynamics faithfully.

## 21.4 The central disclosure

A concise persistent explanation should say:

> “Posts become organisms in an artificial ecosystem. The feed shows what survives under its rules. Survival is not a measure of truth or quality.”

---

# 22. Fairness, Safety, and Source Respect

The site's metaphors can be provocative. Its treatment of real people should not be careless.

## 22.1 People are not organisms

The simulation models posts, not authors. Avoid descriptions that call users parasites, pests, inferior species, or evolutionary failures. A predatory organism is not a predatory person.

## 22.2 Avoid harassment amplification

The aquarium should not become a mechanism for celebrating attacks on individuals, identifying targets, or turning vulnerable people into public spectacle. Harmful or sensitive content requires a clear moderation and display policy independent of ecological fitness.

## 22.3 Source deletion and availability

Respect source removal, content availability, and applicable moderation restrictions. A deleted or restricted post should not remain exposed simply because the simulation produced an interesting lineage. Historical ecological counts can remain where appropriate without retaining or displaying prohibited source content.

## 22.4 Attribution and context

Maintain accurate source attribution. Quotes, replies, sarcasm, and screenshots can be misleading without context; the interface should avoid treating extracted text as a complete statement of an author's views.

## 22.5 Language equity

No language or writing system should be treated as inherently less fit. Different languages may require different ways of understanding vocabulary and similarity, but that must not translate into a hidden universal preference.

## 22.6 Political and topical neutrality

The project should not secretly favor a viewpoint, political camp, or editorial category through ecological traits. Any deliberate content eligibility or safety rules should be acknowledged separately from the biological fiction.

## 22.7 Anti-manipulation philosophy

The site should not reward mass posting, brigading, artificial engagement, or attempts to game the tank through repetition. At the same time, defenses should not erase legitimate bursts of public discussion.

## 22.8 No individual biological verdicts

Do not publish humiliating author leaderboards, “least fit users,” or scores of personal worth. Specimens are posts and lineages, not personality assessments.

---

# 23. Accessibility and Inclusive Observation

The visual tank is important, but understanding the ecosystem must not depend on sight, color perception, precise pointing, or continuous animation.

- Every organism must have a textual identity and meaningful description.
- Major ecological events must be available as readable chronological entries.
- Color must not be the only signal of species, condition, or activity.
- The tank must support reduced motion and a pauseable observation mode.
- Feed and specimen views must remain useful without the visual aquarium.
- Dense interfaces should offer simpler presentation modes.
- Selection and navigation should be possible without precise dragging.
- Text must remain legible against the dark visual language.
- The site should distinguish visual ambiance from essential information.

A good test: a visitor using only the feed, specimen records, and Chronicle should still understand what happened in the ecosystem and why.

---

# 24. Experimental Design Questions

The project should make its open questions explicit. These are design choices to test, not facts to assume.

## 24.1 What should similarity do?

**Option A: Predation.** Similar posts compete and consume one another, potentially reducing redundancy.  
**Option B: Cooperation.** Similar posts cluster, producing topic colonies and collective persistence.  
**Option C: Context-dependent relationships.** Similarity increases encounter probability, while organism traits and environmental conditions determine the outcome.

**Recommended hypothesis:** C. It creates richer ecological possibilities and avoids making topical similarity synonymous with either conflict or solidarity.

## 24.2 Should organisms reproduce?

**Option A:** No reproduction; a pure ecology of unique source posts.  
**Option B:** Reproduction as visible simulated descendants, with clear lineage attribution.  
**Option C:** Reproduction only as colony growth or inherited ecological influence, without multiplying visible individual creatures.

**Recommended hypothesis:** B, but with strict source identity and feed deduplication. It offers genuine evolutionary dynamics while preserving the integrity of the original posts.

## 24.3 How much should engagement matter?

**Option A:** No engagement signals.  
**Option B:** Engagement modifies a few context-dependent traits.  
**Option C:** Engagement changes the environment around a post but does not directly refill its energy.

**Recommended starting hypothesis:** A or C. The site's value lies in discovering something that conventional popularity signals miss.

## 24.4 How long should organisms live?

Short lifetimes create spectacle and a rapidly changing feed. Long lifetimes create history, resilience, and meaningful ecological succession. The correct answer is not a fixed target lifespan but a world where both short-lived blooms and exceptional long-lived survivors can occur.

## 24.5 Should the world be fully deterministic?

A repeatable world is easier to explain and compare; stochastic variation creates ecological surprise. The design should aim for **rule consistency with bounded contingency**, and preserve the ability to distinguish environmental luck from trait advantages.

## 24.6 Should users influence the tank?

The canonical world should remain observational. Experimental interventions belong in clearly separated sandbox worlds so the survival feed is not distorted by audience participation.

---

# 25. Illustrative Ecological Scenarios

These are thought experiments, not promised outcomes.

## Scenario 1: The Repetition Bloom

A major public event produces many similar posts. The tank receives a flood of organisms with overlapping resource requirements. Initially the niche becomes crowded and active. Competition intensifies. A few efficient specialists persist, while many others starve or are consumed. The resulting feed may show a small number of surviving perspectives—but the interface must not call them definitive or representative without qualification.

**What this tests:** Whether redundancy can be reduced through ecological scarcity without simply selecting the most popular source.

## Scenario 2: The Quiet Specialist

An obscure post arrives with an unusual combination of concepts. It occupies a niche with little competition and low nutrient availability. Because its metabolism is efficient, it persists long after flashier organisms die.

**What this tests:** Whether the ecology can preserve unusual information without requiring engagement.

## Scenario 3: The Viral Collapse

A highly engaged post enters as a large, active organism. It expands rapidly, feeds aggressively, and produces descendants. Its lineage depletes local resources and suffers a cascade of starvation. Its popularity did not guarantee long-term survival.

**What this tests:** Whether high activity can create ecological liabilities rather than automatic dominance.

## Scenario 4: The Colony

Several complementary posts occupy neighboring resource niches. Their interactions produce a colony that recycles byproducts efficiently. The colony survives a resource drought that kills larger solitary organisms.

**What this tests:** Whether cooperative strategies can emerge without treating textual similarity as proof of agreement.

## Scenario 5: The Predator's Dependence

A dominant predator consumes many smaller organisms. Its prey population collapses. The predator subsequently starves, allowing scavengers and small generalists to expand.

**What this tests:** Whether ecological dominance naturally creates fragility.

## Scenario 6: The Empty Tank

An extended period of low eligible activity causes population decline. Rather than fabricating drama, the site shows a quiet ecosystem with a few persistent organisms and a growing detritus field.

**What this tests:** Whether the experience remains meaningful without constant spectacle.

## Scenario 7: The Return of an Old Idea

A resource family disappears from the active population, then reappears as new posts enter. A dormant-looking niche becomes active again. The site may show ecological recurrence without pretending the old posts themselves have been republished.

**What this tests:** Whether the Chronicle can reveal patterns across time.

---

# 26. Quality Criteria for the Ecosystem

A successful ecology is not one that always chooses the posts its designers personally like. It is one that demonstrates coherent, nontrivial, interpretable behavior.

## 26.1 Ecological coherence

- Organisms respond to resource availability and local conditions.
- Similar traits do not always produce identical outcomes.
- Different strategies can succeed in different conditions.
- Competition, predation, and cooperation have observable consequences.
- The world has meaningful population turnover.

## 26.2 Emergence

- Colonies, blooms, collapses, and succession can arise without being scripted.
- Local interactions can produce larger-scale patterns.
- The environment retains consequences of previous activity.
- The designers can encounter outcomes they did not explicitly prescribe.

## 26.3 Information discovery

- The feed sometimes reveals posts that conventional engagement sorting would miss.
- Surviving posts are not merely the most liked or most reposted.
- The system can distinguish near-duplicate information without treating every similar perspective as interchangeable.
- A visitor can explain why a selected post appeared in the feed.

## 26.4 Trust and legibility

- Source posts remain attributable.
- Simulated descendants are visibly artificial.
- Source removal is respected.
- Survival is never presented as truth or objective merit.
- The distinction between admission, ecological death, and administrative removal remains clear.

## 26.5 Experience quality

- The tank feels alive rather than randomly animated.
- Visitors can understand the premise quickly.
- There is a reason to observe for several minutes.
- There is a reason to return later.
- The feed remains readable and useful on its own.

---

# 27. Failure Modes and Design Responses

| Failure | Why it matters | Design response |
|---|---|---|
| Likes secretly determine survival | The product becomes ordinary ranking in disguise | Keep engagement separate from universal energy and fitness |
| Big organisms always win | The ecology collapses into a single strategy | Enforce trait costs, resource limits, and contextual vulnerabilities |
| Every similar post kills another | Nuance and cooperative behavior disappear | Make relationships contingent on ecology, not similarity alone |
| Every post lives forever | Survival loses meaning | Maintain genuine energy costs, scarcity, and aging |
| Every post dies immediately | The feed becomes unstable and arbitrary | Permit low-cost strategies and persistent niches |
| Descendants appear as new posts | The site misattributes generated content | Clearly separate simulation identity from source authorship |
| The screen becomes particle noise | Visitors cannot understand ecological behavior | Establish legible motion, relationships, selection, and event narration |
| A dominant author fills the feed | The result feels spammed and unrepresentative | Distinguish source diversity presentation from ecological outcomes |
| Novelty is always rewarded | The system incentivizes nonsense and random wording | Make novelty situational and potentially costly |
| Source removal is ignored | Trust and privacy are compromised | Treat source availability as a binding display constraint |
| The site claims scientific authority | Visitors mistake a designed metaphor for objective truth | Disclose limits and avoid normative labels |
| Moderation is mistaken for natural selection | Visitors receive misleading explanations | Separate content policy from ecological mechanics |
| Constant drama is manufactured | The experiment loses credibility | Allow quiet periods and authentic stability |
| Non-English content fares poorly | The ecology encodes linguistic bias | Evaluate language-related traits without universal language hierarchies |

---

# 28. Product Boundaries and Non-Goals

The initial product should not include user accounts, private tanks, paid boosts, creator monetization, direct messaging, post composition, badges for authors, voting on organisms, competitive user leaderboards, or the ability to purchase nutrients. These features would distract from the core experiment or contaminate the ecological premise.

It should not try to replace Bluesky's social graph. The site is a lens onto public information, not a new social relationship system.

It should not claim to solve misinformation, bias, attention inequality, or recommendation quality simply because it uses an evolutionary metaphor. Those are possible research questions, not built-in outcomes.

---

# 29. Conceptual Product Phases

These phases describe the **experience to be designed**, not an engineering schedule.

## Phase I — The Living Pond

One public tank. Source posts become distinct organisms. They feed, move, compete, age, and die. A companion feed shows current survivors. Every specimen has an understandable life record. The visual world and feed agree on what is alive.

**Experience milestone:** A visitor can watch a post enter, understand what it needs to survive, and see its eventual fate reflected in the feed.

## Phase II — The Ecological Web

Introduce symbiosis, scavenging, colonies, richer resource niches, and consequential environmental changes. The Chronicle begins to reveal larger-scale phenomena.

**Experience milestone:** Visitors can identify emergent communities and ecological cascades that are not reducible to simple one-on-one fights.

## Phase III — Evolution and Lineage

Introduce explicit simulated reproduction, inheritance, mutation, species descriptions, and lineage histories. Keep simulated descendants distinct from original posts.

**Experience milestone:** Visitors can follow a lineage across generations and understand why its strategy persisted or failed.

## Phase IV — Comparative Worlds

Offer additional clearly labeled tanks with different ecological conditions, plus historical comparisons and observational experiments.

**Experience milestone:** The same informational population can produce different survival patterns under different environments, making the contingency of fitness obvious.

## Phase V — The Public Natural History of Information

The site becomes a persistent archive of ecological events, notable lineages, and changing informational niches. It remains a living feed, but also becomes a record of how public information behaved under a particular artificial world.

**Experience milestone:** A visitor can explore not just which posts survived today, but how the ecosystem itself changed over weeks and months.

---

# 30. Open Design Decisions

The following questions should be answered deliberately before the concept is considered stable.

1. **What is the smallest meaningful biological rule set?** Too few rules produce trivial ranking; too many make behavior unintelligible.
2. **What exactly is a nutrient?** The definition must be interpretable and avoid smuggling in a content-quality score.
3. **What makes two organisms interact?** Similarity, proximity, complementary diets, and scarcity may all matter.
4. **What distinguishes predation from ordinary resource competition?** Both must have distinct consequences.
5. **Can organisms survive without consuming other posts?** They should, if environmental feeding is a valid strategy.
6. **How do source posts introduce new resources?** New arrivals should change the world, not just compete within a fixed pantry.
7. **How much should the environment remember?** Detritus, depleted niches, and long-lived colonies could create ecological history.
8. **When is a lineage alive?** If the original organism dies but descendants remain, the interface needs an unambiguous definition.
9. **Which survival feed is canonical?** Individual survivors, extant lineages, or both in distinct views?
10. **How should the tank represent multilingual information?** Language diversity must not be mistaken for ecological deficiency.
11. **How should unusually sensitive posts be handled?** Safety and dignity take precedence over spectacle.
12. **How can an observer understand causality?** The system needs explanations that are truthful without claiming more certainty than it has.
13. **What happens during quiet periods?** The site should remain interesting without manufacturing action.
14. **What does a healthy ecosystem look like?** Diversity and turnover matter, but should not become forced targets that override emergence.
15. **How do we know the feed is genuinely different?** It must be compared conceptually against chronological and engagement-driven discovery, without assuming superiority.

---

# 31. Design Principles to Protect During Revision

1. **Do not assign fitness directly.** Fitness is what survives under environmental pressure.
2. **Do not turn popularity into calories.** Social engagement may be context, but must not be a universal life force.
3. **Do not confuse organisms with people.** The ecology acts on representations of posts.
4. **Do not fabricate source content.** Evolution changes simulated traits, not what an author wrote.
5. **Do not fake emergent events.** Interesting phenomena should arise from consistent rules.
6. **Do not hide editorial or safety decisions inside the biological metaphor.** Admission and moderation are distinct from selection.
7. **Do not make one strategy universally superior.** Every strength needs a cost or dependency.
8. **Do not assume similarity means agreement.** Related posts may compete, cooperate, or coexist.
9. **Do not assume survival means value.** The feed is a discovery experiment, not a moral verdict.
10. **Do not let the aquarium obscure the posts.** The information remains accessible, readable, and attributable.
11. **Do not let the feed obscure the ecology.** Every selection must remain connected to actual ecological history.
12. **Do not punish obscurity.** The experiment should give low-engagement information a plausible route to survival.
13. **Do not reward spam through raw volume.** A flood of posts should create competition and scarcity, not guaranteed dominance.
14. **Do not erase history casually.** Ecological events should remain inspectable where source permissions allow.
15. **Do not require visitors to believe the metaphor.** They should be able to enjoy it while understanding its limits.

---

# 32. The Defining Thought Experiment

Imagine two posts entering the tank at the same moment.

The first is viral. Thousands of people have repeated its idea. It is surrounded by related organisms, crowded into a nutrient-rich but heavily contested niche. It is large, energetic, and immediately successful. It consumes competitors, expands, and reproduces. Soon the niche is depleted. Its descendants compete with one another. The lineage collapses.

The second is barely noticed. It has a peculiar structure and belongs to a sparse informational niche. Its body is small. Its metabolism is slow. It consumes little and encounters few competitors. It survives the day, then the night, then the next wave of arrivals.

In a conventional feed, the first post wins immediately.

In this world, the second post might still be alive when the first has become detritus.

That does not make the second post better. It makes its survival **interesting**.

The Primordial Feed exists to expose that difference.

---

# 33. Final Vision

The finished site should feel like someone connected the internet to a microscope and discovered that information has a metabolism.

Posts drift through a dark, bounded world. They consume resources, compete, cooperate, reproduce, and vanish. New arrivals inherit no guarantee of attention. Old survivors retain no guarantee of permanence. Entire niches bloom and collapse. Colonies form around temporary ecological opportunities. The environment remembers what passed through it.

Alongside the tank is a feed of actual public posts. The feed is not ordered by the loudest authors or the largest engagement counts. It is the visible remainder of an ongoing artificial ecology. A visitor can open any survivor and see not only what it says, but the history of how its organism managed to remain alive.

The experience is at once absurd and serious: an elaborate microscopic civilization made from fleeting social posts, and an experiment in whether selection through ecological interaction can reveal information that conventional feeds overlook.

**The ultimate promise is not that the fittest information is the best information. It is that a different definition of survival might let us encounter a different internet.**

---

## Appendix A — Public-Facing One-Paragraph Description

**The Primordial Feed** is a living aquarium fed by public Bluesky posts. Every post becomes a microscopic organism with traits drawn from its content. Organisms feed, compete, cooperate, reproduce, and die in a shared artificial ecosystem. The posts whose organisms survive appear in a changing feed. It is not a measure of truth, quality, or popularity. It is an experiment in what happens when information has to survive somewhere.

## Appendix B — Short Tagline Candidates

- **The internet, under a microscope.**
- **A feed selected by survival.**
- **Watch information eat itself.**
- **An artificial ecology of public thought.**
- **Some posts are still alive.**
- **Everything enters. Not everything survives.** *(Use only if admission is genuinely universal; otherwise avoid this line.)*
- **The feed is what remains.**

## Appendix C — Conceptual Acceptance Questions

Before declaring the design successful, ask:

- Can a quiet, low-engagement post plausibly outlive a viral one?
- Can two similar posts cooperate instead of automatically fighting?
- Can an organism survive through efficiency rather than aggression?
- Can a dominant lineage collapse because of its own ecological success?
- Can a visitor understand a survivor's history without reading a technical manual?
- Can a visitor tell simulated descendants from real authored posts?
- Can the aquarium remain interesting during quiet periods?
- Can the feed be read independently of the visual simulation?
- Can the site explain that survival is not truth, value, or endorsement?
- Does the ecology produce consequences that were not individually scripted?

If the answer to these questions is consistently yes, the project has a coherent identity beyond an animated feed.

---

# Appendix D — Single-Document Product Contract for BuildThis

This appendix is part of the same authoritative design document. It does not supersede the preceding vision; it makes the intended observable product unambiguous. BuildThis should use this entire file as its sole product-design source. Technical implementation choices are deliberately unspecified.

## D.1 Interpretation and priority

Where language elsewhere in this document is speculative ("could," "might," "consider," or an open question), it is an exploration, **not** a required feature. Where this appendix uses **must**, it describes an observable product requirement. If two requirements conflict, preserve the core proposition: real posts become consequential organisms, ecological survival produces the feed, and the behavior is inspectable. Do not silently replace ecological selection with an engagement score or decorative animation.

The project should favor a small, demonstrably coherent living ecology over a broad collection of features that only simulate the appearance of life. A first version need not implement every biological possibility in this document. It must, however, demonstrate an authentic cycle of birth, competition for limited resources, interaction, and death, with consequences for the survivor feed.

## D.2 Required product experience

1. **Real provenance.** Organisms originate from genuine public Bluesky posts. Each living organism retains a traceable association with its source. Synthetic specimens may appear in a clearly labeled demonstration, but must never be presented as live posts.
2. **Legible transformation.** A visitor can learn which source-post characteristics shaped an organism's traits. The organism's properties must not be arbitrary visual decoration.
3. **A bounded ecology.** The environment has meaningful scarcity, costs, and tradeoffs. Organisms cannot all thrive indefinitely merely because new posts continue to arrive.
4. **Consequential interactions.** At least some encounters change organisms' resources, prospects, or survival. Predation or competition must have real effects on the simulated ecology, not just trigger an animation.
5. **Actual mortality.** Organisms can die through ecological processes. Death removes them from the living population and changes the available survivor feed. A death has a visible, intelligible cause.
6. **Survival-derived feed.** The feed lists real source posts whose organisms are alive or otherwise meet an explicitly named ecological survival criterion. It must not quietly fall back to chronological, engagement, or editorial ranking while calling that result survival.
7. **Inspectable history.** A visitor can select an organism and see its source post, relevant traits, current condition, and significant events in its lifetime. Claims about why it survived must be grounded in actual recorded behavior.
8. **Two connected views.** The living aquarium and readable feed are views of the same world. Changes in the ecology are reflected in the feed, and selecting a feed item identifies its organism when it remains present.
9. **Time and change.** The tank visibly evolves. New arrivals, encounters, resource changes, deaths, and shifts in the survivor population should be observable without needing to infer them from cosmetic movement alone.
10. **Source respect.** The experience attributes original authors, links to source posts, clearly distinguishes simulation outcomes from human worth, and respects source unavailability and deletion.

## D.3 The minimal coherent ecological contract

The initial world must define a comprehensible answer to each of these questions: What does an organism need to survive? Where does that resource come from? What does obtaining it cost? How can another organism affect its access? What makes death possible? How does survival alter what appears in the feed?

The initial design is free to choose a modest number of organism traits and interactions. **It must not invent elaborate species systems, mutation trees, or colony politics before establishing a believable resource cycle.** Additional complexity is justified only when it produces a new observable phenomenon.

The design must allow a quiet or unpopular post to survive under some conditions, and a popular post to die under others. These are required *possibilities*, not promised outcomes for every run. The system must not guarantee a desired winner by manually assigning a superior fitness score.

## D.4 What counts as a working first experience

A visitor can arrive, understand that the specimens are real posts, watch new organisms enter, observe at least one meaningful interaction, inspect a specimen, witness a death or consequential resource loss, and open a readable feed of current survivors. The visitor can follow a survivor to the original post and understand the difference between the source's social engagement and the organism's ecological history.

The site should make clear whether the aquarium is live, replayed, paused, or illustrative. A sparse or temporarily quiet stream should be communicated honestly, not hidden with fabricated activity.

## D.5 Observable evaluation scenarios

These are conceptual acceptance scenarios, not instructions for how to engineer them.

| Scenario | What the experience must demonstrate |
|---|---|
| A new post arrives | A new organism appears with identifiable source provenance and derived traits. |
| Several similar posts arrive | Their shared niche has an ecological consequence; the system does not simply treat them as unrelated particles. |
| A resource becomes scarce | At least some organisms face a survival cost or change in behavior. |
| An encounter occurs | A visible event corresponds to an actual change in organism state. |
| An organism dies | Its death is explained, its living status changes, and the survivor feed reflects that change. |
| A quiet post persists | The system can explain persistence without inventing likes or treating popularity as the sole cause. |
| A highly engaged post fails | The system can explain its ecological failure without contradicting its real-world engagement. |
| A visitor opens a survivor | They reach the genuine original post with clear attribution and context. |
| A source post is removed or inaccessible | The site does not continue presenting its full content as though it were available. |
| A visitor returns later | The world shows meaningful continuity or clearly labels a reset/new run. |

## D.6 Explanation is a first-class feature

An organism detail should distinguish **traits inherited at birth**, **conditions encountered in the world**, **events that affected it**, and **the present outcome**. Avoid invented causal narratives such as "this post won because it was insightful" unless the world actually models and supports that claim. Prefer statements such as "it retained energy because its niche had few competitors" when the ecology supports that observation.

An organism's survival is a statement about this artificial environment under its current rules. It is not an objective judgment about truth, quality, morality, or the author.

## D.7 Visual and editorial requirements

The aesthetic is closer to an observatory, scientific instrument, or natural-history exhibit than a conventional social dashboard. Organisms should be visually distinct and responsive to their actual states. Animation should reveal the ecology, not obscure it. The readable feed must remain usable even if a visitor ignores the aquarium. Color must not be the only way to distinguish important organism conditions. The experience should feel curious, unsettling, and precise rather than gamified for empty spectacle.

## D.8 Explicit exclusions and guardrails

Do not present popularity as biological fitness by another name. Do not let visitors pay, vote, or manually boost an organism's survival in the core ecology. Do not fabricate posts, engagements, authors, events, or causal explanations. Do not turn extinction into a verdict on a real person. Do not add unrelated social-network features merely because similar sites have them. Do not promise that emergent behavior will be interesting in every run; make boring, unstable, or failed ecological outcomes observable as legitimate experimental results.

## D.9 Decisions BuildThis may make without redefining the product

BuildThis may select a restrained initial visual treatment, choose a small set of interpretable organism traits, choose a bounded population and pace, and resolve minor interaction details consistent with this document. It may simplify speculative biology for the first version. It must surface major conceptual choices when they would change what predation means, what counts as survival, whether descendants represent posts, or how the survivor feed is selected. Those choices are product decisions, not merely aesthetic polish.

## D.10 Definition of design success

The project succeeds when someone can say: **"I found this post because it survived a comprehensible artificial ecology, and I can inspect what happened to it."** It fails if the same feed could be produced by an ordinary engagement ranking with a microscopic animation laid over it.

---

**End of the single authoritative design document.**
