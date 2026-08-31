SkyMash — BuildThis Specification

Domain: https://skymash.bisks.net

Build SkyMash, a Bluesky version of the basic mechanic behind Mark Zuckerberg’s original Harvard Facemash: two eligible profiles appear side-by-side and the user picks LEFT or RIGHT.

Eligibility

This is not all of Bluesky.

Only profiles that are Simcluster members or Simcluster-adjacent according to the Shimmer Math Labs membership framework are eligible to appear.

Canonical methodology:

https://shimmermathlabs.com/are_you_in_the_simcluster.pdf

Use Shimmer Math Labs’ “Are You in the Simcluster?” methodology as the source of truth.

The paper defines:

• 40–59: ADJACENT
• 60–79: CORE
• 80–100: SEED / INNER CORE

Therefore:

> **SkyMash eligibility = Simcluster Score ≥ 40**

Do not substitute follower count, starter-pack membership, vibes, or a homemade graph-distance rule.

Calculate membership from the same underlying signals described by Shimmer Math Labs: seed following, seed followership, reciprocal seed connections, and hub proximity.

Determine eligibility from current Bluesky graph data, not a permanently frozen list. Cache results so the site is fast, but periodically re-evaluate accounts because the Simcluster graph changes over time.

Core Experience

The main page should be brutally simple.

Two profiles.

LEFT vs RIGHT.

Each side shows:

• Large profile image
• Display name
• @handle
• Latest 50 public posts

Nothing else should compete with the comparison.

Fetch the latest 50 posts from each profile and place them in separate, independently scrollable columns beneath their profile image.

The point is that the voter can actually inspect what both people post before deciding.

Voting

Voting happens by clicking or tapping the PROFILE IMAGE.

• Tap the left avatar → LEFT wins
• Tap the right avatar → RIGHT wins

Do not make individual posts vote buttons.

After a vote:

1. Update the rankings immediately.
2. Replace both profiles with another eligible matchup.
3. Never match an account against itself.
4. Avoid repeating the same pair during the same session.

Add a small SKIP button.

A skip means exactly that:

• No winner
• No loser
• No ranking change
• Immediately generate another matchup

Ranking

Use an Elo-style rating system.

Every eligible account starts from the same baseline. LEFT/RIGHT outcomes update both ratings.

Do not use any of the following as part of the SkyMash rating:

• Followers
• Likes
• Reposts
• Existing engagement
• Simcluster Score

Simcluster Score determines eligibility only.

SkyMash ranking should be generated exclusively from head-to-head LEFT vs RIGHT votes.

A highly followed account should receive zero automatic advantage.

Matchmaking should usually pair profiles with reasonably similar SkyMash Elo ratings so comparisons remain meaningful.

Occasionally introduce less-compared eligible profiles so new accounts can enter the ecosystem and the leaderboard does not calcify.

Leaderboard

Add:

/leaderboard

Show:

• Rank
• Avatar
• Display name
• Handle
• Elo
• Wins
• Losses
• Total matchups
• Win percentage

The leaderboard contains only profiles currently meeting the Simcluster Score ≥ 40 eligibility threshold.

If an account later falls below the threshold:

• Stop serving it in new matchups.
• Do not erase its historical results.
• Mark it inactive/ineligible until it qualifies again.

Match History and Abuse Prevention

Keep enough matchup history to prevent obvious farming.

Track pair history and avoid repeatedly serving the exact same pair to the same voter.

Do not let someone hammer one account against favorable opponents indefinitely.

If authentication is needed for abuse prevention, use AT Protocol / Bluesky OAuth.

Login should not become the product.

Use identity primarily for:

• Rate limiting
• Duplicate-vote protection
• Basic anti-manipulation controls

Keep the actual vote anonymous publicly.

Do not create public lists showing who voted for whom.

The leaderboard should represent aggregate results, not expose individual voters.

Include basic anti-bot protections and sensible rate limits.

Do not over-engineer this into a surveillance system. The goal is preventing trivial leaderboard manipulation, not fingerprinting everyone who visits.

Bluesky Data and Moderation

Respect Bluesky moderation state.

Do not display:

• Deleted accounts
• Deleted posts
• Unavailable content
• Takedowns
• Content the AT Protocol APIs indicate should not be displayed

Provide a straightforward profile opt-out.

Store profiles by DID, not handle.

Handles can change.

Use DID as the durable identity and resolve the current:

• Handle
• Display name
• Avatar

from Bluesky.

Periodically refresh profile metadata and recent posts.

Do not permanently cache someone’s old avatar, old handle, or an ancient set of 50 posts.

Deleted posts should disappear after refresh.

Deleted accounts should stop appearing.

If a profile opts out, remove it from future matchmaking promptly while preserving only whatever minimal aggregate historical data is necessary.

Post Selection

Show the latest 50 public posts for each profile.

Include replies and quote posts if they are part of that account’s normal public output.

Do not silently cherry-pick “best” posts based on engagement.

Reposts can be visually distinguished or excluded if necessary to keep the comparison focused on what the person actually writes.

Whatever rule is chosen, apply it consistently to everyone and document it.

Visual Design

The visual design should deliberately evoke an extremely primitive 2003 college web project.

Use:

• White or very light background
• Huge profile pictures
• Basic typography
• Thin borders
• Minimal UI
• Almost no ornamentation

It should be fast as hell.

Do not turn this into a modern SaaS dashboard.

No:

• Giant cards
• Gradient-filled analytics panels
• Onboarding flow
• Excessive settings
• Algorithmic home feed

The comparison is the application.

Desktop

Desktop should feel like the page has been cut directly down the middle:

LEFT | RIGHT

Each profile owns half of the viewport.

Both post histories should be independently scrollable.

Mobile

On mobile, preserve the LEFT vs RIGHT rivalry instead of collapsing everything into a normal vertical social feed.

Both profiles and both voting targets should remain visually obvious.

The user must never wonder which side they are voting for.

Keep the profile images visible or easily reachable while the user examines posts.

Voting should remain a deliberate tap on the avatar, not an accidental tap while scrolling through posts.

Transparency

Beneath the matchup, include a tiny explanation:

> Profiles shown here have a Shimmer Math Labs Simcluster Score of 40 or higher. SkyMash rankings come only from head-to-head votes.

Link the eligibility explanation directly to the Shimmer Math Labs paper:

https://shimmermathlabs.com/are_you_in_the_simcluster.pdf

Do not paraphrase the methodology and then leave users unable to inspect the source.

Add a small:

/about

page explaining:

• What SkyMash is
• How voting works
• How Elo works
• What Simcluster eligibility means
• Why the ≥40 threshold is used
• How to opt out

Make the ranking implementation transparent.

Publish:

• The Elo formula
• The starting rating
• The basic matchmaking rules

The site should not pretend SkyMash rank is an objective measurement of a person.

The Simcluster score and the SkyMash score are completely separate systems.

> **Shimmer Math Labs score = who gets into the pool.**

> **SkyMash Elo = how that eligible profile performs in head-to-head comparisons.**

Never merge the two numbers.

Architecture and Performance

Pair generation should be efficient.

Maintain a cached pool of currently eligible DIDs and their SkyMash ratings rather than recomputing the entire Bluesky graph every time somebody presses LEFT.

Keep the core interaction extremely fast:

Vote → ranking update → next pair

The transition should feel effectively instantaneous.

Do not interrupt every vote with a results screen or animation.

You may briefly show the rating change after a vote, but do not make the user click another Continue button.

The next matchup should already be loading.

MVP Scope

Build this loop first:

1. Shimmer membership calculation/check
2. Eligible profile pool
3. Matchup selection
4. Two profiles
5. Latest 50 posts for each
6. Tap LEFT or RIGHT avatar
7. Elo update
8. Next matchup
9. Leaderboard

Do not broaden scope until that loop works perfectly.

No:

• DMs
• Comments
• Social graph
• Follow button
• Prediction markets
• Profile customization
• Badges

Just SkyMash.

Final Product

https://skymash.bisks.net

A deliberately simple Bluesky Simcluster head-to-head ranking site, grounded in the Shimmer Math Labs membership methodology:

https://shimmermathlabs.com/are_you_in_the_simcluster.pdf

Two profiles. Fifty posts each. Pick one.
