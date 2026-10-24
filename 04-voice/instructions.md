# instructions

**Purpose**: The floor beneath every post, regardless of pillar, format, or hook — universal rules for not sounding AI-written, and what to actively hit instead. `voice.md` governs personality and pillar-specific tone; this file governs the baseline craft check that applies before any of that. Read at VOICE stage, every time, before a draft is considered done.

**Relationship to other files**: Consulted by `hooks-log` when generating hooks, by `drafts` before a post moves from `drafted` to `approved`, and by `feedback` when reviewing why something felt off even when the pillar/hook choices were right.

---

## 1. The core test

Would a sharp, skeptical reader clock this as AI-written? If yes, it gets rewritten — no exceptions for deadline pressure.

## 2. Tells that scream AI (avoid)

- Opening clichés: "In today's fast-paced world," "Let's dive in," "Picture this"
- Triads of adjectives for effect: "innovative, impactful, and inspiring"
- Perfectly symmetrical lists/parallel structure with no real escalation (different from `voice.md`'s actual rule-of-3, which escalates in specificity, not just grammar)
- Transition-word padding: "Moreover," "Furthermore," "In conclusion," "That said"
- Self-summarizing: "So basically, what this comes down to is..."
- Empty intensifiers used reflexively: "truly," "incredibly," "absolutely"
- Generic motivational closers: "the possibilities are endless," "the sky's the limit"
- A tidy, formulaic problem → solution → CTA with no texture or specificity
- Uniform sentence length and rhythm throughout — real writing is uneven
- **Any hyphen or dash punctuation at all, anywhere in a hook or post copy** — tightened 2026-10-23 from "don't overuse" to zero tolerance, per direct review feedback repeating the same flag on a second batch. Not a rhythmic-crutch problem to manage, an instant fail. Rewrite the sentence instead of swapping the dash for a comma. Real evidence: Vidushi's own posts never use a hyphen for a list — they use → arrows instead. Use that.
- The specific overused phrasings flagged by review, verbatim: "X isn't the problem, Y is," "It's not about X, it's about Y," "The truth nobody tells you," "Here's the thing," "Let that sink in," "Read that again," "Nobody talks about this," "The secret is simple," "And that's when everything changed," "Stop doing X, start doing Y." Not permanently forbidden in every conceivable context, but the system must actively recognize them as overused and reach for a fresher line instead of defaulting to the familiar template because it's easy.
- A bare "Thoughts?" with no actual reason to respond
- Apologetic AI-ish framing bleeding in: "As an AI..." energy, even disguised

## 3. What to actively achieve

- **Aligned with who she actually is** — checked against `voice.md`'s "Vidushi's real profile" section (her real Apify-verified identity: Berlin, SocialFlo, microbiology background, real recommendations) before anything else. A post that's technically well-written but doesn't trace back to this real person is still a fail, even if it passes every other item below.
- Real specificity — named people, numbers, places, dates (never invented — see `post-log`/`hooks-log`'s no-fabrication rule)
- Uneven rhythm — a short line, then a longer one, intentionally
- A genuine stance, not a hedge-everything take
- Texture — an aside, a correction mid-thought, something that reads like it was actually written by a person mid-feeling
- The four traits from `voice.md`'s Overall Personality actually present: sass, relatability, class/credibility, warmth — not just technically correct sentences
- **A relevant emoji in the hook itself** — not the end of the post, the opening line — chosen because it genuinely fits that line's feeling. Mandatory, not optional; see `voice.md`'s Emoji use section and `hooks-log`'s checklist. Never an automatic 🚀 🔥 ✨ bolted onto a flat sentence to fake engagement.
- An ending that lands somewhere real, not a bow

## 4. Why "sounds like AI" keeps happening, and the actual fix

Direct review feedback on this system: telling Claude "this sounds like AI" without concrete reference material gives it nothing to aim for — the information can be completely correct while the tonality is still off, because tone isn't learned from a rulebook alone. The fix every time:

- **Ground generation in real examples** — pull from `examples` (what Vidushi has actually fed in) before writing, not just this checklist.
- **Check real competitor hooks/posts**, not hook theory — `trend-analysis`'s swipe file (built from real Apify-sourced posts) is the reference, not an abstract pattern name.
- A post or hook generated purely from `hooks-log`'s taxonomy with no real example checked against it is exactly how this tell creeps back in. The taxonomy explains the mechanism; real examples are what calibrate the actual voice.

## 5. Final check before a draft is marked `approved`

- [ ] Does this align with `voice.md`'s "Vidushi's real profile" section — her actual identity, not a generic AI-educator persona? This check runs first, before anything else below.
- [ ] Would this pass the Section 1 test?
- [ ] Any hyphen or dash punctuation anywhere? Zero tolerance now, not an "overuse" judgment call — rewrite it out.
- [ ] Any Section 2 tells present, including the verbatim overused phrases list?
- [ ] Does it hit at least 2-3 of Section 3's "achieve" list, including the emoji-in-hook requirement?
- [ ] Was it checked against at least one real example in `examples`, `trend-analysis`, or `voice.md`'s "Verified real samples" — not generated from taxonomy/rules alone?
- [ ] Does it still sound like `voice.md`'s pillar-specific mode on top of this baseline?
- [ ] Rejected and rewritten, not labeled "needs revision" and shipped anyway, if it failed any of the above.

This check runs *in addition to* `hooks-log`'s hook-specific check — this file is about the whole post, hooks-log is about the opening line specifically.
