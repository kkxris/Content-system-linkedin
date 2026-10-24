# visuals

**Purpose**: The visual equivalent of `voice.md` — written instructions precise enough that Claude Design can generate an on-brand visual for a post without guessing. Documents the aesthetic, typography, and composition rules to follow, seeded from a real reference example.

**Relationship to other files**: `drafts` triggers this once a post's copy is approved — Claude Design reads this file + the actual post content (from the **Draft posts** database) to generate the matching visual. `examples` is where new visual references get dropped in before they're folded in here.

**Status**: Seeded from **one reference example** (below) — this is the current direction, not yet a confirmed house style. Same rule as everywhere else in this system: a style gets "confirmed" status after 2+ real examples converge on it, not after one.

---

## 1. Reference example

**Source**: Emily Penny (LinkedIn), "Four Levels of Copywriting" post — 439 likes, 42 comments
**Fetched via**: Apify, 2026-10-23
**Original URL**: https://www.linkedin.com/posts/emily-penny_when-the-argument-emerges-that-copy-needs-activity-7509148483757568000-_KmO

A hand-drawn pyramid diagram, four numbered levels, annotated with arrows and bullet callouts, one highlighted term, credit signature bottom-right.

## 2. The aesthetic (what to generate)

**Overall direction**: Minimalist, hand-drawn, whiteboard/notebook feel — not a polished corporate graphic, not a stock-template infographic. Looks like something sketched by hand to explain an idea clearly, not designed to look "designed."

### Color
- **Base**: Pure white background, black ink linework and text. No gradients, no photo backgrounds, no busy color fills.
- **One accent only**: A single highlighter-style accent (yellow, used sparingly) on the one term/phrase that matters most in the whole visual — never more than one highlighted element per visual.
- No decorative color blocks, icons sets, or brand-kit palettes layered on top. The restraint is the point.

### Typography
- **Hand-lettered/marker-style font** throughout — looks handwritten, not a clean sans-serif. Mix of casual print and occasional cursive-adjacent flourishes (underlines, circles) for emphasis.
- **Clear size hierarchy**: Title largest (bold, often all-caps), structural labels medium, annotation/callout text smallest. Size does the hierarchy work — not color or boxes.
- Underline or circle key words by hand-style strokes instead of bold/color for emphasis.

### Composition
- **One central diagram or shape** anchors the visual (a pyramid, a stack, a flow, a simple framework shape) — not a grid of disconnected icons.
- **Annotations radiate outward** from the central shape via hand-drawn arrows, each pointing to the specific part it explains.
- **Numbered steps/levels** where the content has a sequence or hierarchy (1, 2, 3, 4...) — makes the structure scannable at a glance.
- **Generous white space.** Nothing crowds the edges. The diagram breathes.
- **Small credit line** bottom-right (name/brand), understated, not a logo lockup.

### What to avoid
- No stock icons, no 3D renders, no AI-image-generator "glossy" look
- No more than one color accent
- No cluttered multi-column layouts — one idea, one shape, clearly explained
- No generic bar/pie charts unless the post's actual content is genuinely numeric data

## 3. How Claude Design should use this (process)

1. **Read the approved post copy from the Draft posts database** (linked from `drafts`) — find the core structural idea (a hierarchy, a framework, a before/after, a numbered list, a contrast).
2. **Pick the shape that matches the idea** — pyramid for hierarchy/levels, stacked boxes for sequence, two-column for contrast, simple flow arrows for a process. Don't force a pyramid onto content that isn't hierarchical.
3. **Write the visual's text content directly from the post** — the real labels, the real numbers, the real point. Never invented filler text.
4. **Apply Section 2's aesthetic rules** — hand-drawn style, black ink + one highlight accent, size-based hierarchy, annotated arrows, white space.
5. **One highlight only** — pick the single most important word/phrase in the whole visual for the accent color.
6. **Credit line** — Vidushi's name or Co-Work & bottom-right, small.
7. Attach the generated visual to the post's row in the **Draft posts** database, in its `Visual` column, alongside the copy.

## 4. Adding more reference examples

When a new visual reference comes in (via `examples`), add it here as **Reference example #2, #3...** with the same source/URL/stats fields as Section 1. Once 2+ references converge on the same aesthetic choices, update Section 2 to reflect the confirmed pattern and note what changed. If a new reference pulls in a genuinely different direction, it's logged as a separate candidate style, not blended into this one by assumption.

---

## Reference library

### #1 — Emily Penny, "Four Levels of Copywriting" (seed example, above)

*(awaiting more references)*

### Applied in practice

**2026-10-23 batch**: 5 visuals generated following Section 2's spec (hand-drawn whiteboard, black ink + one yellow highlight, hand-lettered type, central diagram per post) for DRAFT-2026-10-23-01 through 05, each shape picked to match that post's actual structure (two-box contrast, 3-step flow, vertical before/after, two-tier "iceberg" stack) rather than one shape reused on everything. Attached to each row's `Visual` field in the **Draft posts** database. This is the first time the spec was actually run end to end — still one applied instance, not yet a second converging reference, so Section 2's status stays "current direction, not yet confirmed house style" until Vidushi's reaction to these comes back.
