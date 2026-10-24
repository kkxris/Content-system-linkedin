# Content System 2.0 — Co-Work &

Vidushi's LinkedIn content system: a closed loop, not a file dump. 14 instruction files, 5 stages, plus one content store (the **Draft posts** database).

Mirrored from the live Notion workspace ("Content system 2.0"), last synced 2026-10-23. **Notion is the source of truth** — this repo is a portable, shareable, skill-embeddable copy of the same system, not a replacement for it. If the two drift, Notion wins; re-sync this repo from there.

## The Loop

```
LISTEN  →  FILTER  →  CLAIM  →  VOICE  →  SHIP → FEEDBACK
  │           │          │         │           │
  └───────────┴──────────┴─────────┴───────────┘
         results change the next week's output —
              that's what makes it a loop
```

| Stage | Folder | Files | Job |
|---|---|---|---|
| **LISTEN** | `01-listen/` | `ideas-for-posts.md`, `examples.md`, `trend-analysis.md` | Capture raw material — your own ideas, any external/reference material, and what's happening competitively |
| **FILTER** | `02-filter/` | `strategy.md` | Decide which ideas actually serve the business |
| **CLAIM** | `03-claim/` | `content-pillars.md`, `posting-rhythm.md`, `pillar-mix-tracker.md` | Decide what to make and when |
| **VOICE** | `04-voice/` | `voice.md`, `instructions.md`, `hooks-log.md`, `visuals.md`, `drafts.md` | Write and design it |
| **SHIP → FEEDBACK** | `05-ship-feedback/` | `post-log.md`, `feedback.md` | Record what shipped, learn from it, route real changes back upstream |

### The Draft posts database (not a file in this repo)

`drafts.md` is process only — it never holds a post's actual content. Every draft's full copy, hook, CTA, and generated visual lives as a row in a separate Notion database called **Draft posts**, linked from `drafts.md`. It has no local `.md` mirror here because it's a table of content, not an instruction file; its schema is documented in `drafts.md` Section 2 so it can be recreated from this repo alone if needed. This split exists because an earlier version of the system mixed draft content directly into `drafts.md` — that was a mistake, corrected once, and this repo should never regress to it.

## How to initiate a run

1. Drop raw material in whenever it occurs to you — an idea in `ideas-for-posts.md`, a reference post/hook/visual in `examples.md`, feedback/reactions in `feedback.md`.
2. Say **"give me this week's content"** (or similar) to whatever's reading this system (Claude, via the skill below). It runs the full pipeline — see `02-filter/strategy.md`'s "How a week's worth of content actually runs end to end" for the exact sequence.
3. Review the drafts landed as rows in the **Draft posts** database (linked from `04-voice/drafts.md`), approve what you want to ship.
4. Once a post is live, its record moves to `05-ship-feedback/post-log.md`.
5. Results and reactions go into `05-ship-feedback/feedback.md` — once evidence clears the 2+ instance bar, real changes route back upstream.

## System must-haves (non-negotiable)

See `02-filter/strategy.md` Section "System must-haves" for the full list. The short version: never fabricate, label analysis vs. fact, one sighting is never proof (2+ instances to promote anything permanent), show structure before creating it, preserve naming across files, keep history append-only, only `post-log` holds published posts, workshop-mention cap is 1-in-3, and nothing changes upstream files automatically except through `feedback`.

## Files by name (flat reference)

- `01-listen/ideas-for-posts.md`
- `01-listen/examples.md`
- `01-listen/trend-analysis.md`
- `02-filter/strategy.md`
- `03-claim/content-pillars.md`
- `03-claim/posting-rhythm.md`
- `03-claim/pillar-mix-tracker.md`
- `04-voice/voice.md`
- `04-voice/instructions.md`
- `04-voice/hooks-log.md`
- `04-voice/visuals.md`
- `04-voice/drafts.md`
- `05-ship-feedback/post-log.md`
- `05-ship-feedback/feedback.md`
