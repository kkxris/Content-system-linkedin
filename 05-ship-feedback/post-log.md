# post-log

**Purpose**: The canonical record of what actually shipped. This is the single source of truth every SHIP/FEEDBACK process reads from — pillar-mix-tracker, hooks-log, and feedback all depend on this file being accurate and complete. Nothing here is fabricated; a missing value stays marked missing, never invented or assumed zero.

---

## Schema

### A. Publication identity

| Field | Required? | Notes |
| --- | --- | --- |
| Post ID | Required | Format: `YYYY-MM-DD-slug` (e.g. `2026-10-22-claude-secrets`). If two posts ship same day, append `-a`, `-b`. Stable once assigned — never reused, never reassigned. |
| Status | Required | `planned` / `drafted` / `approved` / `published` / `updated` / `deleted`. Only `published` or `updated` count as shipped — `planned`/`drafted`/`approved` must never be counted by pillar-mix-tracker. |
| Published date & time | Required once shipped | Include timezone (Vidushi is Europe/Berlin) |
| Platform & account | Required | LinkedIn / Vidushi personal, unless stated otherwise |
| Live post URL | Required once shipped |  |
| Short internal title | Required |  |
| Exact published copy | Required once shipped | Full text, or a stable link to it in the **Draft posts** database |
| Planned vs. actual date | Optional | Only if they differ |

### B. Content classification

| Field | Required? | Allowed values |
| --- | --- | --- |
| Primary pillar | Required | `AI` / `Marketing` / `Founder's Journey` / `Berlin Community & Workshops` (exact names from content-pillars) |
| Secondary pillar | Optional | Same list — only if genuinely serving two |
| Format | Required | From posting-rhythm's taxonomy: `Personal story/confession` / `Community question/ask` / `Educational breakdown/numbered list` / `Contrarian take/opinion` / `Practical tip/tool/experiment` / `Behind-the-scenes/build-in-public` / `Workshop/event announcement` / `Social proof/recap` / `Timely trend response` |
| Objective | Required | From strategy's ranked goals: `Goal 1 — Fill workshop` / `Goal 2 — Build authority` / `Goal 3 — Funnel credibility` / `Goal 4 — Personal connection` |
| Audience segment | Optional | Defaults to strategy's core ICP unless stated otherwise |
| Campaign/workshop/initiative | Optional | Free text, only if tied to a specific event |
| Promotional classification | Required | `Direct promotion` / `Organic mention` / `Community/value-led` / `Not applicable` (first two defined in posting-rhythm; last two cover non-workshop content) |

### C. Hook and creative decisions

| Field | Required? | Allowed values |
| --- | --- | --- |
| Exact opening hook | Required once shipped | As published, verbatim |
| Hook pattern | Required | From voice.md's existing taxonomy — see list below. If genuinely ambiguous, use `Uncategorized — flag for review`, never guess. |
| Creative angle | Optional | One line |
| CTA type & exact CTA | Optional | e.g. `Comment [WORD]` per Signature move #1 |
| Voice mode | Optional | AI / Marketing / Founder's Journey / Berlin (per voice.md's per-pillar modes) |
| Related experiment ID | Optional | Ties to hooks-log once it exists |

**Hook pattern allowed values** (from voice.md, not invented here):
`Signature move #1` (Comment WORD CTA) · `#2` (Hey community opener) · `#3` (Rule-of-3 stack) · `#4` (Named specificity) · `#5` (Clap-cadence) · `#6` (In-medias-res opening) · `#7` (We/our language) · `#8` (PS ending) · `#9` (You-pivot) · `External Pattern 1` (Stop X) · `External Pattern 2` (Numbered list) · `External Pattern 3` (I can't believe X) · `External Pattern 4` (Almost nobody knows X) · `External Pattern 5` (You think you've mastered X) · `External Pattern 6` (Big thing eating up X) · `Uncategorized — flag for review`

A hook pattern is not the same as a format — a numbered list is a format (section B), a curiosity gap is a hook pattern (section C). Don't conflate them.

### D. Performance results (repeatable — never overwritten)

Each post can have multiple snapshots over time. Append a new snapshot block, don't edit old ones.

```javascript
#### Snapshot — measured [DATE, TIME, timezone] — post age: [X days/hours]
- Impressions/reach: [number, or "not available"]
- Reactions: [number]
- Comments: [number]
- Reposts/shares: [number]
- Saves: [number, or "not available"]
- Link clicks: [number, or "not available"]
- Profile visits / follower change: [number, or "not attributable"]
- Business outcome: [DMs received / signups attributed / "none observed"]
```

Standard cadence: one snapshot at 24-48h (per voice.md's existing convention), optionally a second at 7 days if a post is still moving. Missing data stays marked "not available" — never recorded as 0.

### E. Feedback and learning

| Field | Required? | Notes |
| --- | --- | --- |
| Outcome vs. objective | Required once reviewed | Did it do what Section B's objective said it should? |
| Qualitative signals | Optional | Notable comments, repeated questions, objections |
| Interpretation | Optional | Explicitly labelled `[ANALYSIS]` — never stated as fact |
| Recommendation | Optional | Repeat / change / test / stop — and why |
| Related hook experiment / trend / strategy link | Optional |  |
| Feedback status | Required | `not reviewed` / `reviewed` / `action identified` |

---

## Blank post-record template

```markdown
## [POST-ID] — [short title]

**Status**: planned
**Published**: —
**Platform**: LinkedIn / Vidushi personal
**URL**: —
**Copy**: [link to drafts entry, or pasted once shipped]

**Pillar (primary)**:
**Pillar (secondary)**:
**Format**:
**Objective**:
**Promotional classification**:

**Hook (exact)**:
**Hook pattern**:
**CTA**:
**Voice mode**:

### Performance snapshots
_(none yet)_

### Feedback
**Feedback status**: not reviewed
**Outcome vs. objective**:
**Interpretation**:
**Recommendation**:
```

---

## Data integrity rules (non-negotiable)

- Never fabricate URLs, dates, copy, or metrics
- Never mark `published` without confirmation it's actually live
- Missing ≠ zero — always marked explicitly
- Ambiguous hook pattern → flagged, never guessed
- Historical snapshots are append-only, never edited or deleted
- `planned`/`drafted`/`approved` are never counted as shipped by any downstream consumer
- A post spanning two pillars gets a primary + secondary — pillar-mix-tracker counts primary only, to avoid double-counting the ratio
- Duplicate prevention: Post ID is the uniqueness check — same date+slug is never reused

## Operating procedure

**SHIP → log**: 1) Post ID assigned the moment a draft is approved (status `approved`) → 2) on actual publish, status flips to `published`, URL + exact copy + timestamp recorded → 3) first performance snapshot at 24-48h → 4) optional second snapshot at 7 days.

**Log → FEEDBACK**: Feedback stage scans for `feedback status: not reviewed` entries with at least one snapshot recorded → reviews outcome vs. objective → writes interpretation (labelled as analysis) and recommendation → status flips to `reviewed` or `action identified` → if a recommendation is actually acted on (promoted to voice.md, swipe-file, pillar-mix rebalance, strategy review), that's logged in the `feedback` file itself, not here — this file stays factual record only.

## Downstream integration contract

- **pillar-mix-tracker**: counts `published`/`updated` posts only, by primary pillar, over the trailing 10
- **hooks-log**: pulls every post sharing a hook pattern to compare outcomes; preserves each experiment's original hypothesis separately from this file's factual results
- **feedback**: reads `not reviewed` entries, routes evidence-backed learnings upstream; never changes strategy/voice off a single post
- **the Draft posts database** (linked from `drafts`, the content-calendar equivalent): planned/drafted/approved posts live there as rows, full copy included; this log only takes over once a post is `published`

## Validation checklist (per entry)

- [ ] Post ID unique and correctly formatted
- [ ] Status accurate (not prematurely marked published)
- [ ] Primary pillar matches content-pillars' exact 4 names
- [ ] Format matches posting-rhythm's taxonomy exactly
- [ ] Hook pattern matches voice.md's list or is flagged uncategorized
- [ ] No metric overwritten — snapshot appended, not edited
- [ ] Feedback status set, interpretation labelled as analysis if present

---

## Entries

*(empty — no verified historical posts were available to import; starts clean)*
