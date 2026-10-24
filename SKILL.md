---
name: linkedin-content-system
description: Use this skill when Vidushi (Co-Work &) asks for LinkedIn content — a week's worth of posts, a single draft, a hook, feedback on a post, or any work on her content system (ideas, strategy, pillars, voice, hooks, drafts, post log). Also use it when she wants to add an idea, example, or feedback into the system, or wants to review/update any part of it.
---

# LinkedIn Content System 2.0 — Co-Work &

This skill packages Vidushi's full LinkedIn content system: a closed, self-correcting loop (not a one-shot generator) for planning, drafting, shipping, and learning from LinkedIn content for Co-Work & / SocialFlo.

Read `README.md` first — it explains the 5-stage Loop (LISTEN → FILTER → CLAIM → VOICE → SHIP → FEEDBACK) and where every file lives.

## How to use this skill

**When asked for content** ("give me this week's content," "draft a post about X," "give me a hook for..."):
1. Read `02-filter/strategy.md`'s "How a week's worth of content actually runs end to end" — follow that sequence exactly, stage by stage. Don't skip a stage.
2. Pull raw material from `01-listen/ideas-for-posts.md` and `01-listen/examples.md` (sweep anything unrouted in examples first).
3. Filter against `02-filter/strategy.md`'s goals.
4. Decide pillar/format/cadence via `03-claim/content-pillars.md`, `03-claim/posting-rhythm.md`, `03-claim/pillar-mix-tracker.md`.
5. Check `04-voice/voice.md`'s "Vidushi's real profile" section first — her real Apify-verified identity (Berlin, SocialFlo, microbiology background, real recommendations), not a generic AI-educator persona. Then write in `voice.md`'s pillar mode, generate hooks via `04-voice/hooks-log.md`'s process (Section 4 — check against a real example, don't generate from taxonomy alone), check against `04-voice/instructions.md` before approving (its Section 5 now opens with the same profile-alignment check), generate the visual per `04-voice/visuals.md` once copy is approved.
6. Land each draft as a row in the **Draft posts** database (linked from `04-voice/drafts.md`), full copy and visual included — never pasted into `drafts.md` itself. `drafts.md` holds the process only; mixing the two is the one mistake this system has already had to correct.

**When something ships**: move the full record into `05-ship-feedback/post-log.md` per its schema — never fabricate a URL, date, or metric; mark anything unknown as "not available."

**When feedback or results come in**: log them in `05-ship-feedback/feedback.md`, follow its review process (Section 3) — label analysis vs. hypothesis, require 2+ supporting instances before promoting anything into a permanent change, except for a direct explicit correction from Vidushi (like the "sounds like AI" feedback already logged there), which can be actioned immediately.

**When Vidushi gives a new idea, example, or piece of feedback**: file it in the matching intake file (`ideas-for-posts.md`, `examples.md`, or `feedback.md`) rather than acting on it immediately, unless she's explicitly asking for a run right now.

## Non-negotiable rules (apply across every file)

- Never fabricate URLs, dates, quotes, metrics, competitor claims, or personal anecdotes. A gap is marked "not available," never invented.
- Label interpretation explicitly: `[ANALYSIS]` or `[HYPOTHESIS]`, never stated as plain fact.
- One sighting is never proof — 2+ real instances before anything becomes a confirmed pattern, signature move, or permanent change.
- Preserve established naming exactly across files (pillar names, format taxonomy, hook patterns, goal numbers) — never rename or invent a duplicate.
- History is append-only — never edit or overwrite a past snapshot, routing-log entry, or experiment result.
- Only `post-log.md` holds `published` posts; the **Draft posts** database (linked from `drafts.md`) holds everything before that. `drafts.md` itself never holds post content — process only.
- Workshop-mention cap: max 1-in-3 posts.
- No file changes another upstream file automatically — only `feedback.md`, once evidence clears the bar, routes real changes into `voice`, `content-pillars`, `strategy`, or `trend-analysis`.

Full detail on all of these: `02-filter/strategy.md`, section "System must-haves."

## Keeping this in sync with Notion

This repo mirrors the live Notion workspace. Notion is the source of truth. If asked to update the system, make the change in Notion first (showing the proposed structure before creating anything new, per this system's own rule), then reflect the same change here so the two don't drift.
