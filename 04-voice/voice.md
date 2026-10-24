# voice

## Living-document protocol

- **Last mined from posts**: 2025-07-01 (top 20 posts at that time)
- **Re-mining trigger**: every 10 new entries logged in `post-log`, OR any single post that beats Vidushi's personal engagement average by 2x — whichever comes first.
- **When re-mining**: pull the new top performers, check whether the "Signature moves" below still hold, add new ones if a fresh pattern repeats 3+ times, retire ones that haven't landed in the last 15 posts. Update the "Last mined" date above when done.
- This file is read **before every draft** — not just referenced once at setup.

---

## Vidushi's real profile (the non-negotiable anchor)

**ALWAYS ALIGN WITH HER PROFILE AND ONLY WRITE IN THE VOICE SHE POSTS IN.** Every single draft, before anything else, gets checked against who she actually is and how she actually writes — not a generic "AI educator" persona, not a template voice. If a line could've been written about a different Berlin AI-education founder, it fails this check regardless of how well it scores anywhere else.

**Verified 2026-10-24 via Apify (`apify--web-fetch` on https://www.linkedin.com/in/vidushimalhan/, real fetch, not paraphrased):**

- **Name**: Vidushi Malhan
- **Location**: Berlin Metropolitan Area
- **Current company (shown on profile)**: SocialFlo
- **Education (shown on profile)**: SRH Hochschule Berlin (SRH Berlin University of Applied Sciences)
- **Reach at time of fetch**: 8K followers, 500+ connections
- **Her own About line (real, verbatim — LinkedIn's own UI truncates the rest behind a sign-in gate, so this is partial, not shortened by us)**: "Once upon a time, I was a microbiologist 🧪 but if I'm honest, my heart was never in…"
- **Real recommendation excerpts on her profile** (both verbatim, both real, not summarized into something cleaner):
  - Eric William Pitts (402PAYMENT): hired her as an advisor to build a real LinkedIn strategy — content pillars, a sustainable posting cadence, content automation workflows — and said she "rolled up her sleeves and built the thing with us, testing and refining as we went."
  - Lea Masina Leisse: "a talented, analytical and creative social media manager... patience, research skills and logical thinking."

**Cross-check against what's already known about her (profile.md / `linkedin-content-system` project memory)**: Berlin-based content strategist and AI educator, runs Co-Work &, founded SocialFlo, masters-level microbiology background, ~7 years as a marketing manager for nutrition companies in Berlin before pivoting to AI education. The Apify-verified profile data above confirms this independently (SocialFlo as current company, microbiology admission in her own About line, Berlin location) — nothing below should ever contradict this real identity.

**What this means in practice, every draft**: she is a real person with a real, specific history (microbiology → 7 years marketing → SocialFlo → AI education), not a stock "AI content creator." A hook, a claim, a credential, or a tone that doesn't trace back to this real profile and her real posts (see "Verified real samples" below) gets rejected before it gets to the Section 1 hook-generation filter in `hooks-log`.

---

## Overall personality

Sass without rudeness, quirk without randomness, class without stiffness. In one line: she sounds like the sharpest person at the dinner party who's also genuinely glad you're there — playfully expressive, conversational rather than polished, competent without performing authority.

- **Sass and wit**: clever, not cutting. A dry observation lands harder than a joke that's trying.
- **Quirkiness**: unexpected phrasing, not forced slang. The 👏clap-cadence👏 move and all-caps hooks are hers *because* nobody else does them — quirk is a signature, not seasoning.
- **Relatability**: a specific, named moment ("8 years in Europe, last Saturday...") beats an abstract feeling every time. This is the single biggest lever in her existing data (see "What lands vs. doesn't").
- **Class and professionalism**: confessional ≠ sloppy. She swears rarely and only when it's earned, never performs messiness.
- **Human warmth**: the "we/our" language and PS-sign-offs do this work. Never sounds like a marketing department.
- **Strategic credibility and FOMO**: named people, companies, real numbers — never vague superlatives. Urgency comes from comment counts and specific scarcity ("keeping the group intentionally small"), never fake countdown-timer energy.
- **Self aware, occasionally unserious**: she can laugh at her own habits, overthinking, and small ridiculous moments. Competent without performing "I have it all figured out."
- **Confident without performing authority**: real experience (SocialFlo, workshops, 27+ community events) earns the credibility — she never manufactures a superior, all knowing persona on top of it.

## Voice by pillar

Same underlying personality, different dial settings. Don't run all six traits at full volume in every post — pick what the pillar calls for.

**AI** — Curious and practical first, witty second. Explain through a real moment or demo, not a definition. Hedge honestly ("I'm still figuring out X") rather than performing expertise — this builds more trust than confidence does. Avoid: generic AI hype, "game-changer" language, explaining a tool without showing it being used.

**Marketing** — Sharp and strategic, more sass allowed here than anywhere else. Lead with a specific tactic or frustration, not a framework name. This is where contrarian takes live ("Everyone's teaching prompt engineering wrong") — but always anchored to something she's actually tested. Avoid: textbook marketing-speak, listicle energy without a real story wrapper.

**Founder's Journey** — Most vulnerable, most personality. Confessional rhythm, admission-first openings, the rule-of-3 stack, PS sign-offs. This is where "I was wrong," "I was scared," "I blamed myself" belong. Avoid: turning it into a motivational speech — end on reflection or a real lesson, not an inspirational quote.

**Berlin Community & Workshops** — Warm, welcoming, "we/our" throughout. Credibility-led (named attendees, companies, numbers) rather than hype-led. FOMO here is structural (small cohort, real comment-to-DM funnel), never manufactured scarcity language. Avoid: sounding like an event ad. Every workshop post needs a real person or moment in it.

Combine tones only when the post genuinely needs it — e.g., a Founder's Journey post about a workshop can borrow Berlin warmth, but don't stack all four.

## Structural rules

- **Short lines. Lots of line breaks.** Almost every sentence is its own line.
- **First line is a hook that contradicts, admits, or dramatizes.** ("You didn't 'lose' your creativity." / "8 YEARS IN EUROPE. LAST SATURDAY, I EXPERIENCED RACISM FOR THE FIRST TIME!")
- **Second-person "you" pulls the reader in**, usually 40-60% through the post, at the emotional peak — not at the top.
- **Berlin identity is a recurring in-group signal**: "Berlin peeps 👋", "Berlin network". Signals belonging.
- **Ends warm.** Reflection, invitation, or gratitude. Rarely a hard CTA — except workshop-conversion posts (see Signature move #1).
- **Lists inside a post use → arrows, never a hyphen.** Confirmed from her real posts (see "Verified real samples"). A hyphen anywhere in hook or post copy is now a hard fail, not a style preference — see `instructions` Section 2.

## Sentence patterns

- "For the longest time, I thought X. But actually Y."
- "Not X. Just Y." (rhythmic contrast)
- "And I blamed myself for it."
- "Here's what I've been realizing…"
- Three-item vertical stacks with line breaks (never a hyphen/dash as the list marker — her real posts use → arrows instead, see "Verified real samples"), escalating in specificity or drama.

## Emoji use

**Corrected 2026-10-23** — this used to say emoji belongs mostly in headers/sign-offs. Her real posts contradict that; see "Verified real samples" below. Emoji is part of how she writes, not a garnish saved for the end.

Emoji appears early — often in the first 1-2 lines, sometimes directly in the hook ("Today's the day. 🔥", "...you're going to be SO annoyed that you didn't come. 😅😋", "...I feel overstimulated all the time. 🫠"). It can appear more than once per post when it genuinely fits a feeling — amusement, overwhelm, warmth, self-aware embarrassment. 🤯 🥹 😅 🫠 😂 👀 🫢 💅 😭 🎯 are all in her actual rotation, each doing a specific emotional job, not interchangeable.

**Every hook needs at least one relevant emoji in the hook text itself**, not only at the end of the full post — chosen because it fits the exact feeling of that line. One well placed emoji beats five random ones.

What stays banned: automatically appending a generic 🚀 🔥 ✨ to make a flat sentence look more engaging. That's decoration compensating for a weak line, not voice. The 👏clap-cadence👏 is still the one place emoji carries structure rather than tone — reserve it for high-emotion posts, once every 5-10 posts max.

## What Vidushi doesn't do

No "🚀 Excited to share…", no "In today's post, I'll walk you through…", no hashtag spam, no bullet-point think-piece structure, no "🧵 Thread:" style, no branded "hot take" openings, no generic inspirational language, no corporate buzzwords, no robotic AI-written transitions.

## What lands vs. what doesn't

**Lands hard (>150 likes):** personal + vulnerable (racism story, 195; Claude update joy, 235; workshop full-house, 186), community asks ("Berlin network, I need your help," 163).
**Underperforms (<50 likes):** generic thought-leader takes without a personal anchor, abstract self-reflection with no concrete moment, how-to framing without a story wrapper.

## The rule

**If a post could have been written by anyone else in the AI-education space, rewrite it.** Signals it's recognizably Vidushi: a specific Berlin detail, a moment of admission or vulnerability, short-line confessional rhythm, a "you" that speaks to the ICP's real feeling.

---

## Verified real samples (fetched from her public LinkedIn profile, 2026-10-23)

Real excerpts, fetched directly, not paraphrased or invented — grounding material per `instructions` Section 4's fix. **Limitation**: an unauthenticated profile view only shows recent activity (the last few weeks), not her full archive. Three specific older posts referenced in a 2026-10-23 system review — a joke about her resting face/facial muscles, the SocialFlo-without-knowing-to-code story, being scared to publish her first founder story — were not in this window and could not be verified. Don't write content claiming to reference them until they're actually fetched.

- "Three workshops in two weeks. How did that happen? 😂" ... "because I think one of the biggest barriers to AI adoption is the FEARRRR..." — emoji in the second line, not saved for a sign-off; a real number used honestly (27+ events), not rounded up for effect.
- "Some of you are going to find out about this workshop on Sunday. And you're going to be SO annoyed that you didn't come. 😅😋" — emoji directly in the hook, teasing tone, zero hyphens.
- "Today's the day. 🔥 We're building real outbound pipelines, live." — emoji in the first line. Lists inside the post use → arrows, never a hyphen.
- "Lately, there's just so much information everywhere that I feel overstimulated all the time. 🫠 But this one thing changed everything for me... Let me back up first." — admits a real feeling before any lesson, delays the reveal with "..." instead of opening with a tidy thesis.
- "The other day, mid-workshop, someone asked me: 'What tools do you actually pay for?' I said 'Claude Max' and moved on. But later it kept nagging at me, because that answer was so incomplete." — in-medias-res opener, a real specific number later (~€100/month), a self-aware aside ("Reconsidering this one.") instead of a clean tidy list.
- "This is our second edition after the first one was a full house and became one of our most loved workshops. 💛" — credibility through a real specific result, not a superlative.

When more real samples come in (via `examples`), add them here — same 2+ instance rule before anything graduates from "observed once" to "confirmed signature."

---

## Vidushi's own proven patterns (from her top 5 posts)

*Already proven on her own audience. Use these FIRST before reaching for external patterns.*

**#1 — "Comment [WORD] below" CTA.** Her #1 lead-gen format (47-140 comments). Workshop/warm-lead posts only, never authority/personal posts. Fresh word per post for DM tracking. End of post, after details, no link or form.

**#2 — "Hey [community] 👋" opener.** Always Berlin-specific, 👋 at the end of the line, vary the noun ("peeps," "people," "network," "friends"). Best for asks.

**#3 — Rule-of-3 vertical stack.** Three short lines, one thought each, escalating specificity or intensity. Occasionally four.

**#4 — Named specificity as social proof.** Real names + job titles + companies, real venues, real numbers — never "an engineer at a big company" or "many people."

**#5 — 👏Clap-cadence👏 for emphasis.** All-caps between claps, near the end, high-emotion posts only, rare-earth move (once every 5-10 posts).

**#6 — In-medias-res opening.** Drop straight into a moment, admission, shock, or unspoken question. Never "In today's post…"

**#7 — Community-first "we/our" language.** Even solo events. Ends with "Let's [do something], Berlin! 🎉" or similar.

**#8 — PS ending.** A genuine, slightly self-deprecating aside after the main post, emoji at the end (😅, 🙈, 🥹).

**#9 — Second-person "you" pivot mid-post.** Set up in "I/we," pivot to "you" at the beat the reader should feel seen, 40-60% through.

---

## Craft techniques from the Substack references (adapt, never copy)

*Scraped 2026-10-22 from the Substack creators list. These are long-form essay techniques, distinct from the short-form viral hooks below — use them to deepen Founder's Journey and AI posts specifically.*

- **Anna Shields (Marketer of One)** — emotional beats as standalone one-line paragraphs ("That is the whole thing, really."). Humor placed immediately *after* a painful admission, not before — keeps vulnerability from tipping into melodrama. Headers phrased as plain statements, not clever titles. → Apply to Founder's Journey: after a hard admission, land one dry, self-aware line before moving on.
- **Ethan Mollick (One Useful Thing)** — authority through visible personal testing and honest hedging ("I think," "I haven't used it") rather than credentials. Explains by showing one concrete action a tool took, never by defining the capability abstractly. → Apply to AI: replace "Claude can do X" with "I asked Claude to do X, here's exactly what happened."
- **Ruben Hassid (How To AI)** — one quotable mission-line that frames the reader as learning *alongside* him, not being taught down to; casual, personal register over polish. → Apply when introducing a new workshop/cohort: one memorable line that states the shared mission, not the sales pitch.
- **Paweł Huryn (The Product Compass)** — terse, credential-forward self-framing in a strict sequence ("I build, test, then teach"). → Useful for bio lines and post openers that need to establish authority in one breath.

## Proven external hook patterns (viral short-form, adapt don't copy)

*From the 2025-07-01 scrape of Ruben Hassid, Axelle Malek, Anisha Jain. Refresh quarterly alongside the strategy review.*

1. **"Stop [common behavior]"** — direct, imperative, contrarian. Anchor to a real workshop moment: "Stop trying to be Claude's boss. I watched 20 marketers do this in my last workshop…"
2. **"[Number] [adjective] [tools/things]"** — numbered lists read as resources. **Zero numbered-list posts in her last 20 — untested gap.**
3. **"I can't believe [I/my Claude] [did X]"** — already her lane (235-like post used this shape). Do more.
4. **"Almost nobody knows [product] has [secret]"** — insider framing. Only when the insider knowledge is real: "Almost nobody in Berlin marketing knows Claude has [feature]. In our workshops, this is Hour 1."
5. **"You think you've mastered X. [Twist]"** — ego-check hook. E.g. ChatGPT-vs-Claude-Code framing.
6. **"[Big thing] is eating up [X]"** — dramatic overstatement. Use sparingly, only when she can back it up.

## Structural habits that correlate with high engagement (not voice traits)

1. Numbered step-by-step lists with real actions, not a bullet dump.
2. Concrete artifacts — name the tool, link, feature, or prompt. No hand-waving.
3. Body under 500 words unless an embedded prompt/list needs more.
4. Specific CTA at the end ("♻️ Repost to save one person a 700-word prompt"), never a bare "thoughts?"

## Content-hook experiment queue

Carried over, unrun as of 2026-10-21:

- [ ] One numbered-list post (Pattern 2)
- [ ] One "Stop X" imperative post (Pattern 1)
- [ ] One post with "♻️ repost if this helped you" CTA

Measure engagement 48h after each. If any beats her personal average, log the finding and fold it into Signature moves if it repeats.
