# examples

**Purpose**: A single raw-intake inbox. Drop in anything — a post you liked, a competitor's hook, a screenshot/visual, a swipe, a half-formed "we should do something like this" — with zero classification required at the point of capture. This is reference material, not a decision yet. Claude reviews it and routes each item to where it actually belongs.

**Relationship to other files**: Different from `Ideas for posts` — that's *your own* post ideas. This is *external or reference* material: things you saw, liked, or want the system to learn from. Nothing here is permanent — every entry eventually gets routed out to `trend-analysis` (swipe file), `hooks-log` (hook bank/experiments), or `feedback`, and this file stays a clean inbox, not an archive.

---

## How to add an example

Paste in whatever you have, however rough:

```markdown
#### [DATE] — [one-line label]
- **What it is**: post / hook / visual / screenshot / general swipe
- **Content**: [paste the text, link, or describe the visual]
- **Source** (if known):
- **Why I'm flagging it**:
```

## New (unsorted)

*(drop examples here — anything, anytime, no classification needed)*

---

## Routing rules (what happens on review)

1. **A competitor/external post or pattern** → goes to `trend-analysis`'s Swipe File once it has enough real detail (source, pillar, reusable principle) — stays a candidate until 2+ sightings confirm it.
2. **A specific hook** → goes to `hooks-log`'s bank (Confirmed/Promising) or Active Experiments if it's untested.
3. **A visual/design reference** → goes to `visuals` as a new Reference example, once it has enough real detail (source, aesthetic notes) — same 2+ instance rule before anything there is called "confirmed."
4. **Your own reaction/review, not a new piece of material** → that's actually `feedback`, not this file — gets redirected there.
5. Nothing gets promoted into something permanent off one example — same 2+ instance rule as everywhere else.

Move each item from "New" to "Processed" with one line on where it went.

## Processed

*One line per example once routed — keeps "New" showing only what hasn't been looked at.*

- 2026-10-23 — Emily Penny "Four Levels of Copywriting" post (hand-drawn pyramid visual, 439 likes) — fetched via Apify, routed to `visuals` as Reference example #1
- 2026-10-24 — 8 of Vidushi's own real LinkedIn posts (efs5tkUd, ec2VRmEM, edRyNkrH, etyXVYP5, eGyTRZNa, eKM2S85R, evs8YDde, e-Q6p92k) — all fetched and read in full via Apify (`apify--web-fetch`) per her explicit "use apify strictly and only then draw conclusions" instruction — routed to `hooks-log`'s Confirmed bank (HOOK-2026-10-24-01 through 08) and flagged to `feedback` for the real-pattern finding (see `feedback` 2026-10-24 entry)
- 2026-10-24 — Vidushi's own LinkedIn profile (https://www.linkedin.com/in/vidushimalhan/) — fetched via Apify, real name/location/current company/education/About line/recommendations — routed to `voice.md`'s new "Vidushi's real profile" section as the non-negotiable anchor every draft gets checked against

---

## Operating rules

- Never invent missing detail (source, performance, context) to make an example feel more complete than it is.
- An example sitting here unrouted is fine — it's a holding pen, not a backlog that must be cleared.
- This file never gets read directly when generating content — `drafts` pulls from the files examples get routed *into*, not from here.
