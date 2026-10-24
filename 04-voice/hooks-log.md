# hooks-log

**Purpose**: Three jobs in one file — (1) a bank of proven, ready-to-use hooks Claude drafts from, (2) the playbook for how Claude generates new hooks that actually sound like Vidushi, and (3) a tracker connecting published hooks to what actually happened.

**Relationship to other files**: `voice.md` is the authority on personality and already holds the 9 signature moves + 6 external patterns — this file doesn't duplicate that, it operationalizes it: turns "here's a pattern" into "here's when to use it, here's a growing set of real examples, here's how to check a draft hook before it ships." `post-log` is the factual record of what shipped; this file classifies and learns from it, never re-records it.

---

## 1. Hook-generation principles (the non-negotiable filter)

Every hook Claude produces must pass through **sass + class + credibility + relatability**, read as a single working test, not four boxes to tick:

- **Sass without losing class** — sharp, witty, a point of view. Never a roast, never forced slang, never bait.
- **Personality without being unprofessional** — human, specific, occasionally delightful. Warmth and candor are allowed; sloppiness isn't.
- **Relatability ("that is so me")** — draws on a real, specific, recognizable moment. Never a manufactured anecdote.
- **Credibility** — real names, numbers, places when available. Bold claims only when the post backs them up. Never invented to make the hook stronger.

**The test**: *Would this sound like something Vidushi might genuinely say, or does it sound like a random LinkedIn creator copying a viral template?* If generic, overpolished, or interchangeable with any founder's account — rewrite it.

**This is a feel test, not a category-selection exercise.** Tightened 2026-10-23: picking a pattern from Section 2 and filling in its template is exactly how generic output keeps creeping back in, even when the pattern technically "fits." The taxonomy explains why a mechanism works — it is inspiration, never a form to complete mechanically.

*(Full personality detail — tone by pillar, what she doesn't do, what lands vs. doesn't, plus real verified samples — lives in **`voice.md`**. This file assumes that context; it doesn't restate it.)*

---

## 2. Hook pattern taxonomy

*Reused exactly from **`voice.md`** — no renaming, no new categories unless a real example genuinely doesn't fit any of these.*

**Use this to understand why a mechanism works, not as a dropdown to pick from.** A hook that technically matches a row below but doesn't sound like a specific person saying a specific thing still fails Section 1's test and Section 4 Step 6's checklist.

**Creative directions** (use alongside the taxonomy, pick whichever fits the material, don't force every pillar into every category): the slightly absurd observation · the candid admission · the playful confession · the insider observation · the unexpected detail · the cheeky opinion · the FOMO opener (real, never fake scarcity) · the warm personal moment · the elegant understated observation · the in medias res opening. These are directions, not templates — the test is still Section 1.

### Proven on her own audience (use first)

| # | Pattern | Mechanism | Fits when | Doesn't fit when | Evidence |
| --- | --- | --- | --- | --- | --- |
| 1 | Comment [WORD] CTA | Converts interest into a trackable DM funnel | Workshop/warm-lead posts only | Authority or personal posts | Her #1 lead-gen format, 47–140 comments |
| 2 | "Hey [community] 👋" opener | In-group signal, immediate warmth | Asks, community posts | Posts with no real community angle | — |
| 3 | Rule-of-3 vertical stack | Escalating specificity builds momentum | Most formats | Single-point, single-moment posts | — |
| 4 | Named specificity | Real names/numbers as social proof | Anywhere she has real detail | When detail isn't real — never fabricate | — |
| 5 | 👏Clap-cadence👏 | All-caps-between-claps emphasis | High-emotion posts only, rare (1-in-5–10) | Routine or low-emotion posts | — |
| 6 | In-medias-res opening | Drop into a moment, no preamble | Personal story, founder's journey | — | — |
| 7 | We/our community-first language | Removes "I'm selling you something" distance | Workshop/community posts | Solo-authority posts | — |
| 8 | PS ending | Self-deprecating aside, humanizes | Most personal posts | Hard-CTA or urgent posts | — |
| 9 | You-pivot mid-post | Second-person at the emotional peak (40–60% in) | Posts building to a point that should land on the reader | Pure narrative with no "lesson" beat | — |
| 10 | Flat real-statement opener | States a real, present-tense fact/feeling plainly in sentence one — no "picture this," no constructed scene, no invented dialogue | Any post, especially personal/reflective ones | Never fits — this is her default across all formats | 8/8 of her Apify-verified real posts (2026-10-24 batch) open this way; the two highest performers (173 and 82 reactions) are both this pattern |

### External patterns (adapt, never copy wording)

| # | Pattern | Mechanism | Fits when | Evidence |
| --- | --- | --- | --- | --- |
| E1 | "Stop [behavior]" | Direct, imperative, contrarian | Needs a real workshop/experience anchor | Untested on her account |
| E2 | Numbered list ("X [adjective] things") | Resource framing | AI/Marketing educational posts | **Zero in her last 20 — untested gap, good experiment candidate** |
| E3 | "I can't believe [X] did Y" | Surprise/awe | AI posts, already close to her lane | 235-like post used this shape |
| E4 | "Almost nobody knows X" | Insider framing | Only when the insider knowledge is genuinely real | Untested |
| E5 | "You think you've mastered X. [Twist]" | Ego-check | Comparison/myth-busting posts | Untested |
| E6 | "[Big thing] is eating up [X]" | Dramatic overstatement | Sparingly, only when backed up | Untested |

**Uncategorized — flag for review**: used when a real hook genuinely doesn't fit the above rather than forcing it into the nearest category.

New categories are added only when a repeated real example (2+ sightings) can't be described by anything on this list.

---

## 3. Proven hooks bank

*What Claude drafts from first. Each entry is a reusable, ready-to-fire example — distinct from the Active Experiments in Section 5, which are unresolved tests.*

### Template for adding a hook

```markdown
#### [HOOK-ID] — [short label]
- **Hook text (verbatim)**:
- **Source**: Vidushi's own post / external creator / adapted
- **Original URL**:
- **Creator/platform**:
- **Date published/discovered**:
- **Pillar**:
- **Format**:
- **Hook pattern**: (from Section 2)
- **Audience/objective**:
- **Why it works**: [ANALYSIS] or [HYPOTHESIS] — label explicitly
- **Performance evidence**: [numbers + date measured, or "not available"]
- **Reusable principle**:
- **Adaptation notes**: what to borrow vs. leave behind
- **Date added**:
```

### Confirmed (performance evidence exists)

*Added 2026-10-24 — Vidushi supplied 8 of her own real LinkedIn posts; all 8 fetched and verified via Apify (`apify--web-fetch`), full text read before any entry below was written. These are her only Confirmed hooks with real measured performance; everything previously in this file was Promising/hypothesis-only.*

#### HOOK-2026-10-24-01 — "I won't say I'm choosy, but I get inspired by a very selected few people."
- **Hook text (verbatim)**: I won't say I'm choosy, but I get inspired by a very selected few people.
- **Source**: Vidushi's own post
- **Original URL**: https://lnkd.in/p/efs5tkUd
- **Date published/discovered**: ~1 month before 2026-10-24
- **Pillar**: Founder's Journey
- **Format**: Admiration/reflection
- **Hook pattern**: Flat real-statement opener (#10)
- **Why it works**: [ANALYSIS] — self-aware, slightly wry admission in one plain sentence; sets up a real named person (Marie Martens, $6M ARR, team of 7) rather than an abstract lesson
- **Performance evidence**: 173 reactions, 21 comments — her highest-performing post in this batch by a wide margin
- **Reusable principle**: a plain personal admission that leads into genuine admiration for a specific real person outperforms every workshop-promo post in this sample
- **Date added**: 2026-10-24

#### HOOK-2026-10-24-02 — "I think I'm due for a RESET. 🔥"
- **Hook text (verbatim)**: I think I'm due for a RESET. 🔥
- **Source**: Vidushi's own post
- **Original URL**: https://lnkd.in/p/ec2VRmEM
- **Pillar**: Founder's Journey
- **Format**: Personal reflection/burnout
- **Hook pattern**: Flat real-statement opener (#10)
- **Why it works**: [ANALYSIS] — states the feeling directly, no scene, no metaphor; the post then earns it with a real bulleted list of exactly what she's juggling
- **Performance evidence**: 82 reactions, 16 comments — second-highest in this batch
- **Reusable principle**: a stated emotional state, immediately followed by concrete real specifics (not vague venting), is her strongest personal-post shape
- **Date added**: 2026-10-24

#### HOOK-2026-10-24-03 — "Three workshops in two weeks. How did that happen? 😂"
- **Hook text (verbatim)**: Three workshops in two weeks. How did that happen? 😂
- **Source**: Vidushi's own post
- **Original URL**: https://lnkd.in/p/etyXVYP5
- **Pillar**: Berlin Community & Workshops
- **Format**: Social proof/recap
- **Hook pattern**: Flat real-statement opener + self-aware rhetorical question
- **Why it works**: [ANALYSIS] — recap posts open with a real, slightly amused question about her own pace, not an invented "picture this" scene
- **Performance evidence**: 41 reactions, 9 comments
- **Reusable principle**: recap/social-proof posts can open with genuine self-amusement at real numbers (27+ events) instead of a manufactured anecdote
- **Date added**: 2026-10-24

#### HOOK-2026-10-24-04 — "Some of you are going to find out about this workshop on Sunday. And you're going to be SO annoyed that you didn't come. 😅😋"
- **Hook text (verbatim)**: Some of you are going to find out about this workshop on Sunday. And you're going to be SO annoyed that you didn't come.
- **Source**: Vidushi's own post
- **Original URL**: https://lnkd.in/p/eGyTRZNa
- **Pillar**: Marketing
- **Format**: Workshop announcement
- **Hook pattern**: Direct-address FOMO (real, not fake scarcity)
- **Why it works**: [ANALYSIS] — playful, direct-address urgency; backed by a real named co-host and a real tomorrow-not-someday date, never invented scarcity
- **Performance evidence**: 29 reactions, 10 comments
- **Reusable principle**: FOMO only works for her when the urgency is real (an actual date, an actual seat count)
- **Date added**: 2026-10-24

#### HOOK-2026-10-24-05 — "This is our second edition after the first one was a full house and became one of our most loved workshops. 💛"
- **Hook text (verbatim)**: This is our second edition after the first one was a full house and became one of our most loved workshops.
- **Source**: Vidushi's own post
- **Original URL**: https://lnkd.in/p/eKM2S85R
- **Pillar**: Marketing
- **Format**: Workshop announcement (second edition)
- **Hook pattern**: Flat real-statement opener + real social proof
- **Why it works**: [ANALYSIS] — leads with real social proof (first edition sold out) instead of hype language
- **Performance evidence**: 25 reactions
- **Reusable principle**: "second edition, first one sold out" is a real, reusable proof point for repeat workshops — never state this unless it's true for that specific workshop
- **Date added**: 2026-10-24

#### HOOK-2026-10-24-06 — "Today's the day. 🔥 We're building real outbound pipelines, live."
- **Hook text (verbatim)**: Today's the day. We're building real outbound pipelines, live.
- **Source**: Vidushi's own post
- **Original URL**: https://lnkd.in/p/evs8YDde
- **Pillar**: Marketing
- **Format**: Workshop day-of post
- **Hook pattern**: Flat real-statement opener, present tense, day-of energy
- **Why it works**: [ANALYSIS] — short, declarative, real-time; names the actual experts in the room rather than describing the workshop abstractly
- **Performance evidence**: 12 reactions, 7 comments
- **Reusable principle**: day-of posts work as a flat present-tense statement + real named experts, not a recap or a tease
- **Date added**: 2026-10-24

#### HOOK-2026-10-24-07 — "Lately, there's just so much information everywhere that I feel overstimulated all the time. 🫠"
- **Hook text (verbatim)**: Lately, there's just so much information everywhere that I feel overstimulated all the time.
- **Source**: Vidushi's own post
- **Original URL**: https://lnkd.in/p/e-Q6p92k
- **Pillar**: Productivity/personal
- **Format**: Personal tip/practical fix
- **Hook pattern**: Flat real-statement opener, vulnerable admission
- **Why it works**: [ANALYSIS] — names the real feeling first, then earns the tip with concrete, named specifics (LinkedIn, WhatsApp) before getting to the actual fix
- **Performance evidence**: 11 reactions, 9 comments
- **Reusable principle**: a practical tip post lands better led by the real problem/feeling than by the tip itself
- **Date added**: 2026-10-24

#### HOOK-2026-10-24-08 — (tool-stack post)
- **Source**: Vidushi's own post
- **Original URL**: https://lnkd.in/p/edRyNkrH
- **Pillar**: AI/tools
- **Format**: Resource/tool-stack list
- **Performance evidence**: 50 reactions, 7 comments
- **Note**: Already partially reflected in `voice.md`'s Verified real samples; full real tool list and prices confirmed again via this batch — no new entry needed beyond this cross-reference.
- **Date added**: 2026-10-24

**Cross-cutting finding from this batch (flagged to `feedback` per Section 7 — does not change `voice.md`/`strategy` from here directly):** across all 8 real posts, **zero** open with a constructed scene, invented dialogue, or "picture this" framing — every single one is pattern #10 (flat real-statement) or a close variant. The personal/reflective posts (173, 82 reactions) outperform every workshop-promo post (11–41 reactions) in this same batch.

### Promising (no performance data yet, but structurally strong)

*Seeded 2026-10-23 from the first real batch run through the full hooks-log process (Section 4) and the tightened Section 1/6 checks. Unshipped — no performance evidence yet, so none of these move to Confirmed until `post-log` has data.*

#### HOOK-2026-10-23-01 — "My Claude setup used to have more files than my actual laptop folder structure. 🫠"
- **Hook text (verbatim)**: My Claude setup used to have more files than my actual laptop folder structure. 🫠
- **Source**: Vidushi's own draft (unshipped)
- **Original URL**: —
- **Creator/platform**: Vidushi / LinkedIn (drafted, not yet published)
- **Date published/discovered**: drafted 2026-10-23
- **Pillar**: AI
- **Format**: Personal story/confession
- **Hook pattern**: Playful/bizarre admission (Section 2 creative direction)
- **Audience/objective**: Build authority
- **Why it works**: [HYPOTHESIS] — relatable self-deprecating admission, emoji carries the feeling instead of decorating a flat line, no hyphen anywhere
- **Performance evidence**: not available — unshipped
- **Reusable principle**: a bizarre-but-true confession about her own over-engineering lands the "that is so me" test without inventing anything
- **Adaptation notes**: the specific detail (files > folder structure) is hers; borrow the shape (admission + genuine emoji), not the exact line
- **Date added**: 2026-10-23

#### HOOK-2026-10-23-02 — "A workshop participant asked me last week why her Claude kept asking HER questions instead of just answering. 👀"
- **Hook text (verbatim)**: A workshop participant asked me last week why her Claude kept asking HER questions instead of just answering. 👀
- **Source**: Vidushi's own draft (unshipped)
- **Original URL**: —
- **Creator/platform**: Vidushi / LinkedIn (drafted, not yet published)
- **Date published/discovered**: drafted 2026-10-23
- **Pillar**: AI
- **Format**: Practical tip/tool/experiment
- **Hook pattern**: Insider observation/curiosity (Section 2 creative direction)
- **Audience/objective**: Build authority
- **Why it works**: [HYPOTHESIS] — in-medias-res workshop moment, curiosity gap resolved inside the post, not just teased
- **Performance evidence**: not available — unshipped
- **Reusable principle**: a genuine-sounding room moment works better than a dry tip when the tip needs a story wrapper (per posting-rhythm's known data)
- **Adaptation notes**: the specific participant exchange is illustrative, flagged open in the Draft posts database — confirm or swap before this one ships
- **Date added**: 2026-10-23

#### HOOK-2026-10-23-03 — "I used to brief Claude like I was defending a thesis. Three pages before the actual question. 😅"
- **Hook text (verbatim)**: I used to brief Claude like I was defending a thesis. Three pages before the actual question. 😅
- **Source**: Vidushi's own draft (unshipped)
- **Original URL**: —
- **Creator/platform**: Vidushi / LinkedIn (drafted, not yet published)
- **Date published/discovered**: drafted 2026-10-23
- **Pillar**: Founder's Journey
- **Format**: Behind-the-scenes/build-in-public
- **Hook pattern**: Candid confession (Section 2 creative direction)
- **Audience/objective**: Personal connection
- **Why it works**: [HYPOTHESIS] — specific, slightly absurd self-image (defending a thesis) makes an abstract habit concrete
- **Performance evidence**: not available — unshipped
- **Reusable principle**: a corporate-habit confession ties Founder's Journey back to her real pre-SocialFlo background without inventing a scene
- **Adaptation notes**: borrow the "old habit vs. new tool" framing, not the literal thesis image, for other founder-reflection posts
- **Date added**: 2026-10-23

#### HOOK-2026-10-23-04 — "I'll say the quiet thing: most of the 'AI setups' I see in my workshops are stage fright wearing a folder structure. ✨"
- **Hook text (verbatim)**: I'll say the quiet thing: most of the "AI setups" I see in my workshops are stage fright wearing a folder structure. ✨
- **Source**: Vidushi's own draft (unshipped)
- **Original URL**: —
- **Creator/platform**: Vidushi / LinkedIn (drafted, not yet published)
- **Date published/discovered**: drafted 2026-10-23
- **Pillar**: Marketing
- **Format**: Contrarian take/opinion
- **Hook pattern**: Cheeky/confident opinion (Section 2 creative direction)
- **Audience/objective**: Build authority
- **Why it works**: [HYPOTHESIS] — names a pattern plainly ("I'll say the quiet thing") instead of using the banned "nobody talks about this" template; metaphor (stage fright wearing a folder structure) is original, not a stock contrarian line
- **Performance evidence**: not available — unshipped
- **Reusable principle**: a contrarian take lands harder as an image/metaphor than as a flat "X isn't Y" claim — and this is the system's first real Contrarian take/opinion test since the format was flagged untested in posting-rhythm
- **Adaptation notes**: the "stage fright wearing X" framing could extend to other over-engineered-process posts; the specific workshop observation stays flagged as a stated pattern, not a cited instance
- **Date added**: 2026-10-23

#### HOOK-2026-10-23-05 — "There's a particular kind of quiet I've learned to trust in a workshop room. It usually means someone just got Claude to do something they didn't think it could. 🥹"
- **Hook text (verbatim)**: There's a particular kind of quiet I've learned to trust in a workshop room. It usually means someone just got Claude to do something they didn't think it could. 🥹
- **Source**: Vidushi's own draft (unshipped)
- **Original URL**: —
- **Creator/platform**: Vidushi / LinkedIn (drafted, not yet published)
- **Date published/discovered**: drafted 2026-10-23
- **Pillar**: Berlin Community & Workshops
- **Format**: Social proof/recap
- **Hook pattern**: Elegant/understated observation (Section 2 creative direction)
- **Audience/objective**: Personal connection
- **Why it works**: [HYPOTHESIS] — sensory, specific observation rather than a stated outcome claim; uses the real "27+ events" figure from voice.md's Verified real samples, not an invented count
- **Performance evidence**: not available — unshipped
- **Reusable principle**: a specific, observed detail (a kind of quiet, heads down, half-smiling) reads as more credible than a stated result for social-proof/recap posts
- **Adaptation notes**: the "two people in the same session" moment is illustrative, flagged open in the Draft posts database — confirm or replace before this ships
- **Date added**: 2026-10-23

---

## 4. How Claude generates a new hook (the process, every time)

**Step 1 — Read the actual post first.** Central message, strongest real detail, audience, pillar, format, objective/CTA, what the post can actually support. Never write hooks in isolation and force the post to fit.

**Step 2 — Pick the mechanism, not the trend — and check it against something real.** Scan Section 2/3 for what suits *this* post's substance. A pattern is a tool, not a quota to fill. But the taxonomy only explains the mechanism — it doesn't calibrate the actual voice. Before writing, check at least one real reference: `examples` (what Vidushi has fed in directly) or `trend-analysis`'s swipe file (real Apify-sourced competitor posts/hooks). A hook generated purely from this taxonomy with nothing real checked against it is exactly how generic, AI-sounding output creeps back in — see `instructions` Section 4 for why this matters. If the bank/swipe-file is thin for this pillar or angle, that's a signal to pull fresh competitor examples via `trend-analysis` before generating, not to write from the pattern description alone.

**Step 3 — Dial the personality to the post.** Not every hook needs sass. A candid founder story wants vulnerability; a marketing take wants a sharp observation; an AI post wants a grounded specific over hype; a workshop post wants a real outcome + real urgency. Read the content before deciding — don't apply a fixed mapping.

**Step 4 — Make sure the hook is paid off by the post.** No promising a revelation the post doesn't deliver, no borrowed urgency on an evergreen post, no contrarian stance manufactured just to sound bold.

**Step 5 — Generate genuinely distinct options**, not rewrites of one sentence. Each option should start differently — a different opening move, not the same sentence structure with different nouns. Typical spread when asked for multiple: one natural personality-led option, one sharper/sassier, one relatable/candid, one curiosity-driven, one credibility-led/understated — use only what the content actually supports, recommend the strongest with a one-line reason.

**Step 6 — Check every hook before delivery:**

1. Sounds like Vidushi, not generic LinkedIn copy?
2. Personality + class + credibility together?
3. Real reason for the reader to care, stop scrolling, feel curious, amused, or recognized?
4. Fits the content that follows?
5. Claim supported by the post?
6. Distinctive without straining?
7. Pattern/creative direction fits the pillar/format/audience/objective?
8. No stale clichés, no empty hype, no forced slang, no `instructions`-flagged AI tells or banned phrases?
9. Zero hyphens or dash punctuation anywhere in the hook — absolute, not a judgment call?
10. Contains a relevant emoji in the hook text itself, chosen for the actual feeling, not decorative or automatic?
11. Meaningfully different in construction (not just nouns swapped) from the other options offered?
12. Would she plausibly say this out loud?
13. Was it actually checked against a real example in `examples`, `trend-analysis`, or `voice.md`'s "Verified real samples," not written from the taxonomy alone?
14. Would a real reader feel something, smile, get curious, or want to know more — not just pattern-match a familiar LinkedIn shape?

**Reject and rewrite anything that fails** — never show a failing hook even as one of the options on offer, and never use a numeric score to excuse a hook that fails an essential item. "Needs improvement" is not a status a hook ships in.

---

## 5. Active experiments

*Unresolved hook tests — distinct from the proven bank above. Carried over from **`voice.md`**'s experiment queue.*

```markdown
#### [EXP-ID] — [pattern being tested]
- **Hypothesis**:
- **Pattern**: (from Section 2)
- **Target post**: (links to post-log Post ID once shipped)
- **Status**: queued / shipped, awaiting data / resolved
- **Result**: [measured, not interpreted]
- **Verdict**: supports / contradicts / inconclusive — [ANALYSIS]
```

**Carried over from ****`voice.md`****, unrun as of 2026-10-21:**

1. One numbered-list post (Pattern E2) — flagged gap: zero in her last 20 posts
2. One "Stop X" imperative post (Pattern E1)
3. One post with "♻️ repost if this helped you" CTA

---

## 6. Connecting to post-log (how hooks get evaluated)

For every post in `post-log` with a recorded hook pattern:

- Pull Post ID, live URL, exact hook as published, pattern, pillar, format, objective, experiment ID (if any), performance snapshots, feedback.
- Compare like-for-like only — same objective/audience/format tier, not raw likes across unrelated post types.
- State explicitly when there's insufficient evidence to conclude anything — never declare a winner off one post.
- Record useful failures, not just wins.
- A pattern only gets promoted into "Confirmed" (Section 3) after 2+ supporting posts — exactly `voice.md`'s existing promotion rule.

---

## 7. Operating rules

- **Discovering an example** → save source, classify pattern, explain principle, record evidence (or mark missing) — never backfilled with invented data.
- **Generating hooks** → run the Section 4 process every time, no shortcuts for a "quick" post.
- **A post ships** → link its exact hook to its `post-log` entry and experiment ID if any.
- **Results arrive** → append to the relevant hook's performance evidence; never overwrite.
- **A pattern earns real evidence** → update Section 2/3 notes and flag the implication to `feedback` — this file never pushes changes into `voice.md`, `strategy`, or `content-pillars` directly. One good post is a data point, not a mandate.
