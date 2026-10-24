# drafts

**Purpose**: The workspace where a week's worth of content actually gets written — from raw idea to an approved, ready-to-ship draft. This is the only file in the system that's a workspace, not a decision-maker: everything here is still in motion. Once a post is actually published, `post-log` takes over as the record — `drafts` never holds a `published` post.

**This page holds the process only, never the posts themselves.** The actual draft content lives in the **Draft posts** database, kept deliberately separate so the instructions and the content never get mixed into one page again.

**Relationship to other files**: This is where the whole Loop runs in practice. A draft here pulls from `Ideas for posts` (the raw material), gets checked against `trend-analysis`, routed through `strategy` → `content-pillars` → `posting-rhythm` (what to make and when), written in `voice`, given a hook via `hooks-log`'s process, and once approved and shipped, logged properly in `post-log`.

---

## 1. How a week's content gets built (the actual flow)

When asked for "a week's worth of content," this is the process:

1. **Pull from `Ideas for posts`** — everything in "New" that hasn't been processed yet.
2. **Cross-reference `trend-analysis`** — anything timely, or a swipe-file pattern worth adapting this week.
3. **Check `pillar-mix-tracker`** — which pillars are under-represented and should get priority this week.
4. **Run through `strategy`** — which objective each piece should serve.
5. **Apply `posting-rhythm`** — how many posts this week (baseline 3), which formats, workshop-cap check (max 1-in-3), no back-to-back repeated formats.
6. **Write in `voice`** — check "Vidushi's real profile" section first (her real Apify-verified identity, not a generic persona), then the correct pillar mode and personality dial.
7. **Generate hooks via `hooks-log`'s process** — read the actual post first, pick the mechanism or creative direction, check it against a real example in `examples`, `trend-analysis`, or `voice.md`'s "Verified real samples," offer genuinely distinct options, run the 14-point check, reject and rewrite anything that fails rather than flagging it and moving on.
8. **Check against `instructions`** — run the final anti-AI-tell check (Section 5) before a draft can move to `approved`.
9. **Generate the visual via Claude Design** — once copy is approved, read `visuals` + the actual post content, generate a matching visual, attach it to the draft's row.
10. **Land each piece as a row in the Draft posts database** (schema below), status `planned` or `drafted`.
11. Move the used idea(s) in `Ideas for posts` from "New" to "Processed."

Nothing here is invented without a real idea behind it — if there aren't enough raw ideas to fill the week, that's flagged rather than padded with generic filler posts.

## 2. Draft posts database — schema

The posts themselves are rows in the linked **Draft posts** database, not content on this page. Each row holds:

| Column | What goes in it |
| --- | --- |
| Post | Draft ID + working title |
| Date | The date it was drafted |
| Pillar | From `content-pillars` |
| Format | From `posting-rhythm`'s taxonomy |
| Hook type | From `hooks-log`'s taxonomy/creative directions |
| Status | `planned` / `drafted` / `approved` / `published` |
| Post copy | The full post, verbatim, in one cell |
| CTA | The exact CTA, or "none" |
| Visual | Generated once copy is approved, per `visuals` |
| Open questions | Anything needing Vidushi's confirmation before it ships — especially any detail that's illustrative rather than a verified real moment |

A draft never lands here with an invented statistic, customer story, workshop moment, or quote presented as fact — if a detail is illustrative rather than confirmed, it goes in "Open questions," not silently into the copy.

## 3. This week's batch

Batch of 2026-10-23 — 5 posts, 5 different formats (no back-to-back repeat), workshop-mention subject count 1-in-5 (under the 1-in-3 cap) — is in the **[Draft posts](https://app.notion.com/p/f79933a9ca81456bb86b7b29c53f0d83)** database: DRAFT-2026-10-23-01 through 05.

`Ideas for posts` was empty when this batch was built, so all 5 are grounded in `voice.md`'s "Verified real samples" and established real facts about Co-Work &, not a logged idea — flagged here rather than silently padded. Each row's "Open questions" field marks which specific moments are illustrative and need Vidushi's confirmation before approval.

## 4. Approval → handoff to post-log

- `planned` → `drafted` → `approved` all live as a row's `Status` in the **Draft posts** database.
- The moment a draft is actually posted on LinkedIn, its `Status` flips to `published` and the full record — Post ID, exact copy, hook, pattern, timestamp — moves into `post-log`. It's removed from the active batch there, not duplicated.
- The **Draft posts** database never holds a `published` row — if it's live, it belongs in `post-log`.

## 5. Operating rules

- A draft is never invented from nothing — it traces back to a real idea, a real trend observation, or a real gap flagged by `pillar-mix-tracker`.
- Hooks are generated through `hooks-log`'s actual process every time, not shortcut for speed. A hook that fails the checklist is rejected and rewritten, never shipped with a "needs improvement" label attached.
- Workshop-cap and format-repeat rules from `posting-rhythm` are checked before a batch is considered final, not after.
- Vidushi reviews and approves before anything ships — this file (and its database) produces drafts, it doesn't publish them.
- **This page is process only.** Post content always lives in the Draft posts database, never pasted into this page — that mixing is exactly what caused confusion before.
