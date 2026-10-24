# strategy

*Last updated: 2026-10-22*

**Its job in the system:** every idea from LISTEN (brain-dump, trend-analysis, swipe-file) passes through here before it reaches CLAIM. If an idea doesn't serve a goal below, or doesn't fit the ICP, it gets dropped or reframed here — no matter how trending or well-crafted it could become. This is the step that keeps the content system pointed at the business, not just at engagement.

## The business

**What Vidushi sells**: Hands-on Claude Code workshops in Berlin for non-technical professionals (small groups, learn-by-doing), plus AI/marketing consulting under SocialFlo.

**Why it exists**: Non-technical people are being told "just use AI" but have no one who will actually sit with them and show them how. Vidushi is that person.

**The bigger picture**: Workshops are the top of a funnel that also includes corporate B2B training, a cohort programme, and a paid community tier — the 2026 growth goal runs through all of it, not just workshop seats. This is why content now has to do double duty: fill workshops **and** build the authority that makes the next-stage offers credible.

## Goals (ranked)

1. **Fill each upcoming workshop.** Immediate revenue, immediate signal. Current focus: *update with next workshop date.*
2. **Build authority as "the person who teaches non-technical Berliners how to actually use AI at work"** — not "AI thought leader," not "prompt engineer." That specific niche.
3. **Build credibility for the funnel** — position Co-Work & / SocialFlo as the natural next step beyond a single workshop (corporate training, cohort, community), so later offers aren't a cold pitch.
4. **Personal connection.** People should feel they know Vidushi — her story, her humor, her frustrations — not just her events.

## The customer (ICP)

- **Role**: Marketer, PM, founder, consultant, operations, HR — non-technical but knowledge worker
- **Age**: 28-45
- **Location**: Berlin (or commuting distance / occasional visitors)
- **Attitude toward AI**: Curious but anxious. Feels behind. Has tried ChatGPT casually, hasn't gone deeper.
- **What they want**: To actually *use* AI for their real work — not slides about "the future of work"
- **What they trust**: Human teachers in a room, not YouTube tutorials or courses they never finish
- **What they distrust**: Tech bros who talk over them, jargon, hype
- **Where they hang out**: LinkedIn (primary), Berlin startup Slack groups, meetups, some Instagram

Note: Marketing-pillar content (positioning SocialFlo, not just workshops) may reach a slightly wider audience than this core ICP. Worth watching, not yet a reason to redefine it.

## Positioning statement

> "For non-technical Berliners who want to actually use AI at work — not just hear about it — Vidushi runs hands-on Claude Code workshops. Small groups, real projects, no jargon."

## What we are NOT

- Not another "prompt engineering course"
- Not for developers
- Not thought-leadership-about-AI-in-general
- Not yet a scaled cohort/community business — that's the 2026 goal, not today's reality. Content can build toward it but shouldn't claim it's live before it is.

## How the pillars serve these goals (the actual filter)

This is what makes FILTER concrete at CLAIM time — a pillar tells you which goal an idea is supposed to serve:

- **AI** → mainly Goal 2 (authority), indirectly Goal 1 (demonstrates competence that fills workshops)
- **Marketing** → mainly Goal 3 (funnel credibility)
- **Founder's Journey** → mainly Goal 4 (personal connection), secondarily Goal 3
- **Berlin Community & Workshops** → mainly Goal 1 (direct workshop fill)

If an idea doesn't map cleanly to one of these, it's not ready for CLAIM yet — go back and ask which goal it's actually serving.

## Conversion rules

- **Everything happens on LinkedIn.** No external forms, no landing pages, no email captures (for now). Comments are the signal, DMs are the close.
- The "would you be interested?" post pattern is the proven warm-lead generator — run it before each workshop.
- After comments come in, Vidushi DMs each commenter within 24h with details.
- Marketing-pillar content doesn't need a hard CTA — its job is trust-building for the later funnel stages, not immediate conversion.

## The audience saturation problem

Current follower count: *re-check and update.*
The core audience is warm but exhausted from seeing workshop posts. **Every workshop-mention post now has to earn its place by being genuinely interesting to someone who's seen five before.**

**The fix (see ****`posting-rhythm`****):** 3 authority/value posts for every 1 workshop-mention post. Reach beyond the core audience via personal stories, DMs, comments on adjacent creators' posts, and asks in Berlin-specific communities.

---

## The full system — where every piece lives

The content system is a closed loop, not a file dump. Fourteen instruction files, five stages, plus one content store:

| Stage | Files | Job |
| --- | --- | --- |
| **LISTEN** | `Ideas for posts`, `examples`, `trend-analysis` | Capture raw material — your own ideas, any external/reference material you want to feed the system, and what's happening externally/in the swipe-file |
| **FILTER** | `strategy` (this file) | Decide which ideas actually serve the business — drop or reframe anything that doesn't |
| **CLAIM** | `content-pillars`, `posting-rhythm`, `pillar-mix-tracker` | Decide what to make and when — pillar, format, cadence, and whether the mix is actually balanced |
| **VOICE** | `voice`, `instructions`, `hooks-log`, `visuals`, `drafts` | Actually write and design it — personality, universal anti-AI-tell baseline, hook, matching visual (via Claude Design), draft record, approval |
| **SHIP → FEEDBACK** | `post-log`, `feedback` | Record what shipped, learn from it, and route real changes back upstream |

`instructions` is the pillar-agnostic craft floor — read on every draft regardless of pillar — while `voice` stays the authority on personality and pillar-specific tone. `visuals` works the same way for images that `voice` does for copy: Claude Design reads it plus the approved post content to generate a matching visual.

**The 15th component**: the **Draft posts** database, linked from `drafts`. It's not an instruction file — it's the actual content store, where a draft's full copy, hook, CTA, and visual live as a row. `drafts` holds the process only; it never holds post content itself, to keep instructions and content from getting mixed into one page again.

`examples` is an inbox, not a decision point: anything dropped there (a post, a hook, a visual, a swipe) gets routed out to `trend-analysis`'s swipe file, `hooks-log`'s bank, or `feedback` once reviewed — it's never read directly when building a draft.

Nothing skips a stage. An idea that goes straight from `Ideas for posts` to a published post without passing through FILTER/CLAIM/VOICE is exactly what this rebuild was meant to stop.

## How "a week's worth of content" actually runs end to end

This is the full pipeline `drafts` executes when asked for a week of content — written here too, because strategy is where the orchestration logic should be visible at a glance:

1. **LISTEN** — pull everything unprocessed from `Ideas for posts`; check `trend-analysis` for anything timely or swipe-file-worthy this week; sweep `examples` for anything still unrouted that's actually relevant, and route it to its real home (swipe file / hooks-log / feedback) before building.
2. **FILTER** (this file) — for each idea, does it map to a Goal above? Drop or reframe anything that doesn't.
3. **CLAIM** — `pillar-mix-tracker` says which pillars need attention; `content-pillars` + `posting-rhythm` decide the actual format/cadence/workshop-cap for the week.
4. **VOICE** — check `voice`'s "Vidushi's real profile" section first (her real Apify-verified identity — Berlin, SocialFlo, microbiology background — not a generic persona), then write each post in the right pillar mode; generate hooks through `hooks-log`'s process (read the post → pick mechanism → distinct options → 14-point check); land it as a row in the **Draft posts** database (linked from `drafts`, which holds the process, never the content itself).
5. **Vidushi reviews and approves** each draft in the **Draft posts** database.
6. **SHIP** — on publish, the full record moves into `post-log` (the only place `published` posts live).
7. **FEEDBACK** — as results and reactions come in, they're dropped into `feedback`; once evidence clears the 2+ instance bar, real changes route back into `voice`, `content-pillars`, `trend-analysis`'s swipe-file, or this file.

That last step is what makes it a loop instead of a pipeline — results change the next week's output, not just get logged.

## System must-haves (non-negotiable, across every file)

- **Never fabricate.** No invented post URLs, dates, quotes, metrics, competitor claims, or personal anecdotes — ever, in any file. A gap is marked "not available," never filled in.
- **Distinguish fact from interpretation.** Anything that's a read on data, not the data itself, is explicitly labelled `[ANALYSIS]` or `[HYPOTHESIS]` — never stated as plain fact.
- **One sighting is never proof.** A pattern, trend, or hook only gets promoted into something permanent (signature move, swipe-file entry, strategy change) after **2+ real instances** — in `voice`, `trend-analysis`, `hooks-log`, and `feedback` alike.
- **Show structure before creating it in Notion.** Any new page or database gets shown to Vidushi for approval before it's pushed — not after.
- **Preserve established naming.** Pillar names, format taxonomy, hook patterns, goal numbers — reused exactly across files, never renamed or re-invented. A real naming conflict gets flagged, not silently resolved by creating a duplicate file.
- **History is append-only.** Performance snapshots, routing-log entries, experiment results — new entries get added, old ones are never edited or overwritten.
- **Only ****`post-log`**** holds ****`published`**** posts.** The **Draft posts** database (linked from `drafts`) holds everything before that; nothing is double-counted or duplicated across the two.
- **Workshop-mention cap: max 1-in-3 posts** (from `posting-rhythm`), checked every time a batch is built.
- **No automatic upstream edits.** `pillar-mix-tracker` and `post-log` only flag/record — only `feedback`, once evidence clears the bar, actually changes `voice`/`content-pillars`/`strategy`/`trend-analysis`.

---

## Review cadence

Reviewed **quarterly**, same as before — but also reviewed **whenever FEEDBACK flags it**: if a post outside current strategy performs well, that's a signal this file is stale, not just an interesting outlier. Last review: 2026-10-22. Next scheduled review: ~2027-01-22.
