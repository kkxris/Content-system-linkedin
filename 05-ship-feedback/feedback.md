# feedback

**Purpose**: This is the stage where learning becomes change. You drop feedback in as it comes to you — a reaction, a result, a pattern you're noticing — anytime, no waiting for a formal review. Claude reads it, decides whether the evidence is strong enough to act on, and if so, routes the actual update into `voice`, `content-pillars`, `trend-analysis`'s swipe-file, or `strategy`. This is what closes the Loop — without this file, results just pile up in `post-log` and nothing changes.

**Relationship to other files**: `post-log` and `pillar-mix-tracker` are factual records — they don't interpret. `hooks-log` tracks hook-specific evidence. This file is where interpretation happens and where the decision to actually change something gets made and logged. Nothing upstream (`voice`, `strategy`, `content-pillars`, `trend-analysis`) gets edited directly from a single post — only from here, and only once the evidence clears the bar.

---

## 1. How to add feedback

Drop it in under "New" below, any time, any shape — a one-line reaction, a "this flopped and I think I know why," a "noticed this pattern across my last 3 posts." Doesn't need to be tied to a specific post, but link one if there is one.

```markdown
#### [DATE] — [one-line label]
- **Related Post ID** (if any):
- **What happened / what I noticed**:
- **My read on it** (your gut take, not yet [ANALYSIS]):
```

## 2. New (unreviewed)

*(write feedback here — anything, anytime)*

---

## 3. Review process

When reviewing an entry (triggered by you asking, or whenever a few have piled up):

1. **Check it against the evidence**, not just the feeling — pull the related `post-log` entry/snapshot, `pillar-mix-tracker` snapshot, or `hooks-log` pattern if one exists.
2. **Label the interpretation explicitly**: `[ANALYSIS]` if it's a reasoned read of real data, `[HYPOTHESIS]` if it's a hunch without enough evidence yet.
3. **Apply the promotion rule** — same one used everywhere else in this system: a pattern needs **2+ supporting instances** before it changes anything permanent. One flop or one win is a data point, never a verdict.
4. **Decide**:
   - *Not enough evidence yet* → stays open, flagged "watching," revisit next time something related ships.
   - *Enough evidence* → write the actual change and which file it goes into (Section 4).
5. Move the entry from "New" to "Reviewed" with its outcome.

## 4. Routing log (what actually changed, and where)

*Append-only — this is the audit trail of every real change this system has made to itself.*

```markdown
#### [DATE] — [what changed]
- **Triggered by**: [feedback entries / post IDs involved]
- **Evidence**: [the actual data, not the feeling]
- **Changed in**: voice / content-pillars / trend-analysis (swipe-file) / strategy / posting-rhythm
- **What changed, exactly**:
```

#### 2026-10-23 — Added `instructions` file + tightened `hooks-log`'s generation process

- **Triggered by**: Direct review feedback (not post-performance data) — explicit correction, actioned immediately rather than held to the 2+ instance rule, since it's a stated requirement, not an inferred pattern
- **Evidence**: Reviewer feedback: drafted content "sounds like AI," specifically called out hyphen/em-dash overuse as a tell; noted the information itself wasn't the problem, the tonality was; recommended grounding generation in real examples and real competitor hooks rather than abstract instruction alone
- **Changed in**: New file `instructions` (universal anti-AI-tell checklist + why this keeps happening); `hooks-log` (Section 4 now requires checking real examples/competitor hooks before generating, not taxonomy alone)
- **What changed, exactly**: See `instructions` Sections 2 and 4 for the specific tells and the fix; see `hooks-log` Section 4 Step 2 for the updated process

#### 2026-10-23 — Split draft content out of `drafts.md` into a separate Draft posts database

- **Triggered by**: Direct correction (not post-performance data) — explicit instruction, actioned immediately rather than held to the 2+ instance rule, since it's a stated requirement, not an inferred pattern
- **Evidence**: Vidushi's direct correction: "i do not want you to mixupp draft content and draft content's md instructions together, and these 5 posts should be organised in a table the post whole post should be in table with date and separate from md instructions file" — after an earlier pass had wrongly pasted 5 full draft posts directly into `drafts.md`
- **Changed in**: New Notion database "Draft posts" (full schema in `drafts.md` Section 2); `drafts.md` reverted to process-only and pointed at the database; `visuals.md`, `post-log.md`, `strategy.md`, `SKILL.md`, and `README.md` updated everywhere they referenced draft content as living inside `drafts.md` directly
- **What changed, exactly**: `drafts.md` Sections 1–5 rewritten so every step says "land as a row in the Draft posts database" instead of "land here"; the 5 draft posts from this batch (DRAFT-2026-10-23-01 through 05) live only as database rows, each with full copy, CTA, visual, and open questions; this routing-log entry is the permanent record so the mistake isn't repeated on the next batch

#### 2026-10-23 — First full pipeline run: 5 drafts + 5 matching visuals generated and logged

- **Triggered by**: Direct request ("start the content system gimme 5 draft post...") — first real end-to-end run of VOICE through the tightened `hooks-log`/`instructions`/`voice.md` rules from this session's earlier personality-gap fix
- **Evidence**: 5 drafts built via `hooks-log` Section 4's process, each checked against `voice.md`'s Verified real samples and `instructions` Section 5 before being marked `drafted`; 5 visuals generated per `visuals.md`'s spec, one shape per post's actual structure (not one shape reused everywhere); workshop-mention cap and format-variety checks both passed (1-in-5 and zero back-to-back repeats)
- **Changed in**: `hooks-log` Section 3 (5 hooks added to the Promising bank — see HOOK-2026-10-23-01 through 05); `visuals.md` Reference library (new "Applied in practice" note)
- **What changed, exactly**: No permanent rule changed here — this is the first real test of rules already tightened earlier today. Logged so the next batch's pillar mix and format variety can be checked against this one, and so these 5 hooks have a record once `post-log` eventually has performance data to compare against

#### 2026-10-24 — Added real confirmed hook bank from Vidushi's own 8 posts; flagged real-statement pattern and personal-vs-workshop engagement gap

- **Triggered by**: Direct correction — Vidushi reported the 5 generated drafts "sound very, very, very AI," hooks have "no pattern," and questioned whether the system was actually using her real profile/context. She then supplied 8 real lnkd.in post links with the explicit instruction "use apify stritcly and only then draw conclusions"
- **Evidence**: All 8 posts fetched and read in full via Apify (`apify--web-fetch` + `get-dataset-items`, no paraphrase, no gap-filling). Hooks (verbatim) and real engagement: "I won't say I'm choosy..." 173 reactions/21 comments; "I think I'm due for a RESET" 82/16; tool-stack post 50/7; "Three workshops in two weeks" 41/9; "Some of you are going to find out..." 29/10; "This is our second edition..." 25/—; "Today's the day..." 12/7; "Lately, there's just so much information..." 11/9. All 8 open with a flat, present-tense real statement — zero use a constructed scene, invented dialogue, or "picture this" framing. The two highest performers (173, 82) are both personal/reflective posts; every workshop-promo post in the batch scored lower (11–41)
- **Changed in**: `hooks-log` (new taxonomy pattern #10 "Flat real-statement opener"; 8 new entries in the Confirmed bank — HOOK-2026-10-24-01 through 08, the first entries in that section with real measured performance); `examples.md` (Processed log entry for all 8 posts)
- **What changed, exactly**: This is the pattern the 5 existing drafts were missing — they all used confession → *invented* scene → twist, which appears in zero of her real 8 posts. Not acted on beyond the hook bank per her explicit instruction ("do not rewrite rn we just have to change a few examples and hooks") — the 5 drafts themselves were not touched. The personal-outperforms-workshop-promo engagement gap is noted here as a single-batch observation (n=8, not yet 2+ independently-sourced batches) — flagged as [HYPOTHESIS], not promoted to `content-pillars` or `strategy` yet

#### 2026-10-24 — Added Vidushi's real LinkedIn profile to `voice.md` as the non-negotiable alignment anchor

- **Triggered by**: Direct instruction — "also apify and add vidushi's profile in the voice md with the most important point ALWAYS ALIGN WITH HER PROFILE AND ONLY IN THE VOICE SHE POSTS" + her profile URL
- **Evidence**: Fetched https://www.linkedin.com/in/vidushimalhan/ via Apify (`apify--web-fetch`). Real, verified: name, Berlin Metropolitan Area location, current company SocialFlo, education SRH Hochschule Berlin, 8K followers/500+ connections, her real (partially gated by LinkedIn's own UI) About line ("Once upon a time, I was a microbiologist..."), and two real recommendation excerpts (Eric Pitts/402PAYMENT, Lea Masina Leisse) confirming her actual professional work in LinkedIn strategy/content systems. Cross-checked against existing `profile.md` memory — consistent, no contradiction
- **Changed in**: `voice.md` — new section "Vidushi's real profile (the non-negotiable anchor)" added directly after the Living-document protocol, before Overall personality, so it's the first thing read on every draft
- **What changed, exactly**: Every draft now gets checked against her real identity and real profile facts before the hook/personality checks in `hooks-log` run — explicit instruction in bold caps per her wording, carried verbatim into the file

## 5. Reviewed (closed out, no action needed)

*One line per entry once reviewed and not promoted — keeps "New" showing only what's still open.*

- 2026-10-23 — "Sounds like AI / hyphen tell" feedback — reviewed immediately, routed to Section 4 (new `instructions` file + `hooks-log` update), not held to the 2+ instance rule since it was a direct stated correction

---

## 6. Operating rules

- Feedback can be dropped in raw and unfiltered — the review step is where rigor gets applied, not at the point of capture.
- Never skip straight from "New" to a changed file — every real change passes through Section 3's evidence check and gets logged in Section 4.
- A single bad or great post is never enough on its own, no matter how strongly it feels like a signal.
- This file never edits `post-log` — it only reads it.
