# pillar-mix-tracker

**Purpose**: A simple read-out of whether the shipped content actually matches the target mix — not a planning tool, not a log. It reads `post-log`, counts, and shows drift. Nothing here is edited by hand; it's recalculated each time from `post-log`'s real entries.

**Relationship to other files**: `content-pillars` sets the target percentages. `post-log` is the only source of truth for what counts. This file just does the math and flags when the two have drifted apart.

---

## 1. The targets (from content-pillars — not redefined here)

| Pillar | Target % |
| --- | --- |
| AI | 40% |
| Marketing | 25% |
| Founder's Journey | 20% |
| Berlin Community & Workshops | 15% |

## 2. Counting rules (from post-log's integration contract)

- Counts **`published`****/****`updated`** posts only — `planned`/`drafted`/`approved` are never counted.
- Counts by **primary pillar only** — a post's secondary pillar is never counted, to avoid double-counting the ratio.
- Window: **trailing 10 shipped posts** (rolling — drop the oldest once an 11th ships).
- If fewer than 10 posts have shipped yet, the tracker still runs on however many exist, but flags that the read is low-confidence until 10 are in.

## 3. Current snapshot

```markdown
#### Snapshot — calculated [DATE]
**Posts counted**: [N] of trailing 10 (window: [oldest Post ID] → [newest Post ID])

| Pillar | Target | Actual count | Actual % | Drift |
|---|---|---|---|---|
| AI | 40% | — | — | — |
| Marketing | 25% | — | — | — |
| Founder's Journey | 20% | — | — | — |
| Berlin Community & Workshops | 15% | — | — | — |

**Workshop-mention cap check**: [X of last 3 posts mentioned a workshop] — cap is 1-in-3 (from posting-rhythm)
**Flag**: [none / pillar X is Y points over-target / pillar X is Y points under-target]
```

*(empty — no shipped posts yet; first snapshot runs once post-log has real published entries)*

## 4. What counts as drift worth acting on

- **±5 points or less** from target — normal variance, no action.
- **More than ±5 points, sustained across 2 consecutive snapshots** — worth a note to `feedback`, not an automatic rebalance.
- **A pillar at 0% for 10 straight shipped posts** — flagged regardless of the ±5 rule; something's being avoided.
- Workshop cap breach (more than 1-in-3) — flagged immediately, every snapshot, not just on sustained drift.

This file never edits `strategy` or `content-pillars` itself — it flags, `feedback` decides whether the evidence is strong enough to actually change the targets.

## 5. Operating rule

Recalculate whenever asked, or automatically whenever a new post in `post-log` flips to `published`/`updated`. Each new snapshot is appended below the previous one — history stays visible, nothing overwritten.

---

## Snapshot history

*(empty)*
