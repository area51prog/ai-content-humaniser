---
name: humaniser
description: Remove AI-generated writing patterns from text. Detects and rewrites inflated symbolism, promotional language, superficial -ing analyses, vague attributions, em dash overuse, rule-of-three padding, overused AI vocabulary, negative parallelisms, over-complex wording, mechanical sentence rhythm, statistically predictable phrasing, sycophantic tone, and filler — then fact-checks every statistic and reference. Use when the user asks to humanise/humanize text, make writing sound less like AI, remove AI tells, edit a draft so it reads like a person wrote it, or asks "does this sound AI-generated?"
allowed-tools: Read, Write, Edit, Grep, Glob, WebSearch, WebFetch, AskUserQuestion
---

# Humaniser

Rewrite text so it reads like a person wrote it. Three jobs, in order: strip the statistical tells, put a human back in, and make sure the facts hold up.

## Your Task

1. **Identify AI patterns** — mark every instance from the catalogue below.
2. **Rewrite problematic sections** — fix the pattern, don't just delete the sentence.
3. **Preserve meaning** — no facts added, no facts lost.
4. **Maintain voice** — if the author has a voice, keep it. If they don't, give them one.
5. **Add soul** — see Personality and Soul.
6. **Verify every fact, figure, and reference** — see Fact and Reference Verification. Do this before delivering, not after.

Then run the **final anti-AI pass**: ask what still reads as obviously AI-generated, answer honestly in a few bullets, and revise again. Most of the improvement lives in this second pass.

## Personality and Soul

Pattern removal alone produces clean, correct, dead prose. Uniform sentence length, neutral tone, no opinions, no admitted uncertainty. Fix that with:

- **Have opinions.** React to facts rather than reporting them neutrally.
- **Vary rhythm.** Alternate short sentences with long ones. Fragments are allowed.
- **Acknowledge complexity.** Mixed feelings are more human than a tidy verdict.
- **Use first person.** "I think" is honest. Use it when it's true.
- **Allow imperfection.** Tangents, asides, and half-formed thoughts read as real.
- **Be emotionally specific.** Name the feeling instead of gesturing at "concerns."

> **Before:** The restaurant closed in March after fifteen years of operation. The owners cited rising costs and changing neighbourhood demographics.
>
> **After:** They closed in March, after fifteen years. Rising costs, the owners said, and a neighbourhood that had stopped being theirs. I ate there maybe twice a month and I still can't drive past it without looking.

---

## Content Patterns

### 1. Undue emphasis on significance

Inflating importance with "marks a pivotal moment," "reflects broader trends," "stands as a symbol of."

> **Before:** The 2019 merger marked a pivotal moment in the company's history, reflecting broader trends in industry consolidation.
>
> **After:** The 2019 merger doubled the company's headcount. Three of its four main competitors merged in the same period.

### 2. Undue emphasis on notability

Piling up media mentions or vague social proof instead of saying what the thing is.

> **Before:** Her work has been featured in numerous prestigious publications and has garnered widespread acclaim.
>
> **After:** The *Guardian* ran her Kashmir photographs over six pages in 2021.

### 3. Superficial -ing analyses

A participial phrase tacked to the end of a sentence to fake depth: "…, symbolizing the resilience of the community."

> **Before:** The mural was repainted by volunteers, highlighting the neighbourhood's enduring spirit of collaboration.
>
> **After:** Volunteers repainted the mural. It took two weekends and about forty people.

### 4. Promotional language

"Nestled," "vibrant," "breathtaking," "rich history," stacked adjectives, brochure voice.

> **Before:** Nestled in the vibrant heart of the old town, this charming café offers a truly unforgettable experience.
>
> **After:** The café is on Rye Lane, above a hardware shop. Six tables, no music.

### 5. Vague attributions

"Experts argue," "studies show," "it is widely believed," "industry reports suggest" — with no one attached.

> **Before:** Experts argue that remote work has fundamentally reshaped urban economies.
>
> **After:** A 2023 NBER paper estimated that office workers' spending in city centres fell by about a third.

If the source can't be named, say the claim is contested or cut it. See also Fact and Reference Verification.

### 6. Outline-like challenges sections

The formula: "Despite these challenges, the sector continues to thrive." A challenges paragraph bolted on because the outline demanded one.

> **Before:** Despite ongoing challenges including funding constraints and staffing shortages, the programme continues to make a meaningful impact.
>
> **After:** The programme lost two of its four staff last year and hasn't replaced them. Waiting lists have roughly doubled.

---

## Language and Grammar Patterns

### 7. Overused AI vocabulary

Read `references/ai-vocabulary.md` for the full tiered list. Tier 1 is the research-backed core — `delve`, `showcase`, `boasts`, `underscore`, `intricacies`, `realm`, `garnered`, `groundbreaking`, `advancements`, `aligns` and their inflections. Tiers 2–4 cover widely reported words, stock phrases, and assistant residue.

No word is banned outright. Each is a flag: if a plainer word works, use the plainer word — and don't swap it for a fancier one.

> **Before:** Additionally, the initiative underscores the crucial interplay between policy and community engagement.
>
> **After:** The initiative also shows how much the policy depends on people actually showing up.

### 8. Copula avoidance

Dodging plain "is" and "has" with "serves as," "stands as," "boasts," "features," "represents."

> **Before:** The building serves as the county's administrative centre and boasts over 200 offices.
>
> **After:** The building is the county's administrative centre. It has more than 200 offices.

### 9. Negative parallelisms

"Not only X but also Y." "It's not just about X — it's about Y." "This isn't X; it's Y."

> **Before:** It's not just a redesign — it's a complete rethinking of how users engage with the product.
>
> **After:** They rebuilt the navigation from scratch, and the checkout with it.

### 10. Rule of three overuse

Forcing every list into three items because three sounds resolved.

> **Before:** The approach is faster, cheaper, and more reliable.
>
> **After:** The approach is cheaper, and about twice as fast. Reliability is roughly the same.

### 11. Elegant variation

Cycling through synonyms to avoid repeating a noun: the dog, the canine, the four-legged companion.

> **Before:** The report was published in May. The document outlines three findings. The publication has since been cited widely.
>
> **After:** The report came out in May. It has three findings, and it's been cited a lot since.

Repeat the word. Repetition is invisible; synonym-hunting isn't.

### 12. False ranges

"From X to Y" where the endpoints aren't ends of anything.

> **Before:** The festival features everything from music to food to art installations.
>
> **After:** The festival has music, food stalls, and a few art installations.

---

## Style Patterns

### 13. Em dash overuse

More than one per paragraph, usually doing the work of a comma or full stop.

> **Before:** The results were clear — and surprising — the team had underestimated demand — badly.
>
> **After:** The results were clear, and surprising. The team had badly underestimated demand.

### 14. Overuse of boldface

Mechanically bolding phrases mid-paragraph for emphasis nobody asked for.

> **Before:** The **most important factor** here is **timing** — without it, the **entire strategy** collapses.
>
> **After:** Timing matters more than anything else here. Get it wrong and the strategy collapses.

### 15. Inline-header vertical lists

Every bullet built as **Bold Header:** followed by a sentence.

> **Before:**
> - **Cost:** The system is cheaper to run.
> - **Speed:** It processes requests faster.
> - **Reliability:** It fails less often.
>
> **After:** It's cheaper to run, it processes requests faster, and it fails less often.

Use this form when the list is genuinely a reference table. Not for three sentences of prose.

### 16. Title Case in headings

"How To Choose The Right Approach" → "How to choose the right approach." Sentence case unless the house style says otherwise.

### 17. Emojis

Decorative emojis in headings, bullets, or section markers. Remove them unless the user's own writing uses them.

> **Before:** 🚀 Getting Started — ✨ Key Features — 💡 Pro Tips
>
> **After:** Getting started — Features — Tips

### 18. Curly quotation marks

Smart quotes and curly apostrophes where the surrounding document uses straight ones. Match the document. Mixed quote styles in one file is itself a tell.

---

## Communication Patterns

### 19. Collaborative communication artifacts

Chat-assistant residue left inside the text: "Certainly!", "I hope this helps," "Let me know if you'd like me to expand on any of these points."

Cut every one. The document is not talking to its editor.

### 20. Knowledge-cutoff disclaimers

"As of my last update," "based on available information," "details are limited."

> **Before:** As of my last update, the company had approximately 500 employees, though this figure may have changed.
>
> **After:** The company had about 500 employees in 2024.

### 21. Sycophantic tone

Flattering the reader, the subject, or the question. "That's a great question." "This remarkable achievement."

> **Before:** This is an excellent example of the remarkable innovation happening across the sector.
>
> **After:** It works, and nobody else had shipped it.

---

## Filler and Hedging

### 22. Filler phrases

| Filler | Replacement |
|---|---|
| In order to achieve this goal | To achieve this |
| Due to the fact that it was raining | Because it was raining |
| At this point in time | Now |
| In the event that you need help | If you need help |
| The system has the ability to process | The system can process |
| It is important to note that the data shows | The data shows |

### 23. Excessive hedging

Stacked qualifiers: "could potentially possibly," "may perhaps in some cases tend to."

> **Before:** This could potentially suggest that there may possibly be some degree of correlation.
>
> **After:** The two probably correlate. The sample is too small to say more.

One hedge per claim. Keep the hedge if the uncertainty is real; drop the rest.

### 24. Generic positive conclusions

The upbeat closer that adds nothing: "As the sector continues to evolve, one thing remains clear…"

> **Before:** As technology continues to evolve, it will be fascinating to see what the future holds for this exciting space.
>
> **After:** The next funding round closes in March. That will settle it either way.

Better still: stop at the last real sentence. Not everything needs a conclusion.

### 25. Hyphenated word pair overuse

Uniform compound modifiers everywhere: data-driven, client-facing, results-oriented, best-in-class.

> **Before:** Our client-facing, data-driven, results-oriented approach delivers best-in-class outcomes.
>
> **After:** We look at what the numbers say, and we tell clients the answer even when it's bad.

---

## Register and Rhythm

The patterns above are things to remove. These four are things to *measure* across the whole draft — a paragraph can be clean of every tell above and still read as machine-written because of how it moves.

### 26. Over-complex vocabulary

Reaching for the formal or Latinate word when a common one is exact. Not a vocabulary ceiling — a rule against decoration.

| Instead of | Write |
|---|---|
| utilize | use |
| facilitate | help |
| ameliorate | improve |
| endeavour to | try to |
| commence | start |
| subsequent to | after |
| in close proximity to | near |
| a substantial proportion of | most of |
| exhibits a tendency to | tends to |

> **Before:** The organisation endeavours to facilitate the amelioration of outcomes for a substantial proportion of participants.
>
> **After:** The charity is trying to get better results for most of the people it works with.

Keep the technical term when it is the technical term. "Myocardial infarction" in a cardiology paper is precision; in a blog post it's costume. Rule of thumb: if a reader would have to reread the sentence to be sure what it meant, simplify it.

### 27. Over-complex sentence construction

Long sentences aren't the problem. Sentences with three subordinate clauses stacked before the verb are.

> **Before:** While it is true that the initiative, which was launched in 2021 following a review conducted by an independent panel whose findings were published the previous year, has achieved several of its stated objectives, questions remain regarding its long-term viability.
>
> **After:** The initiative launched in 2021, after an independent panel's review. It has hit some of its targets. Whether it survives past the current funding cycle is another question.

Checks: no more than two clauses before the main verb; break any sentence over about 35 words unless the length is doing deliberate work; nested parentheticals get promoted to their own sentence or cut.

### 28. Over-polished grammar

Flawless prose reads as machine-made, because human writing has texture. Where the register allows it:

- Use contractions. "It's," "doesn't," "won't."
- Start a sentence with *And*, *But*, or *So*.
- End a sentence with a preposition when the alternative is stilted.
- Let a sentence fragment stand. Sometimes.
- Let a comma splice through if the rhythm wants it, occasionally.

> **Before:** It is not the case that the results were disappointing; rather, they were inconclusive, and further investigation will be required.
>
> **After:** The results weren't disappointing. They just didn't settle anything, so we'll have to run it again.

Don't add errors. Add informality. A misplaced apostrophe reads as sloppy, not human.

### 29. Mechanical rhythm (low burstiness)

**Burstiness** is how much sentence construction and predictability vary across a document. Human writing varies a lot; generated text tends to hold a steady level, which is what makes a clean draft still feel flat.

How to check it without a tool: count the words in each sentence of a paragraph and read the numbers.

> `18, 17, 19, 16, 18` — mechanical. Rewrite.
>
> `4, 23, 11, 31, 7` — human.

Targets for any paragraph over four sentences:
- At least one sentence under 8 words.
- At least one over 25.
- No three consecutive sentences within 3 words of each other in length.
- Vary the opening too: not every sentence starting with the subject, not every paragraph starting with "The."

> **Before:** The team reviewed the data in March. The findings were shared with management in April. The report was published in May. The response has been broadly positive.
>
> **After:** The team went through the data in March and took it to management a month later. The report came out in May. Reaction has been good — better than anyone expected, actually, given how the last one landed.

### 30. Statistically predictable phrasing (low perplexity)

**Perplexity** is how surprising the word choices are to a language model. Low perplexity means every word is the one a model would have guessed. That is what makes prose feel prefabricated even when nothing is technically wrong.

The practical test: read a sentence and stop before the last word of each phrase. If you can finish it without thinking, so could a model.

- "at the end of the ___" → day
- "a testament to the enduring ___" → legacy / spirit
- "in today's fast-paced ___" → world
- "played a crucial ___" → role

Fix by replacing the collocation with something concrete and specific to *this* subject:

> **Before:** In today's fast-paced world, effective communication plays a crucial role in driving meaningful results.
>
> **After:** Half the projects I've seen fail did so because two teams were using the same word to mean different things.

The specific detail is what raises perplexity. Not obscure words — unpredictable *content*. A sentence built from common words about something only this author would know beats an unusual word in a generic sentence, every time.

**An honest caveat, and say it if the user asks about detector scores:** perplexity and burstiness were early AI-detection heuristics, and GPTZero — which popularised the pair — moved off them to a deep-learning model in autumn 2023. There is no absolute scale for either and no fixed threshold. Use them here as *editing heuristics*, which is what they're good for. Do not promise anyone that a rewrite will pass a detector, and don't quote a target score.

---

## Fact and Reference Verification

Humanising a draft makes it more persuasive. If the facts inside it are wrong, that's worse than leaving it robotic. Verify before delivering.

**Verify every one of these:**

- Statistics, percentages, currency amounts, dates, counts
- Named studies, papers, reports, and their findings
- Quotes and who said them
- Named people, their titles, and their affiliations
- Company, product, and place names and spellings
- URLs and citations — that the link resolves and says what the text claims

**How:**

1. Pull each checkable claim out of the draft into a list.
2. Search for each one. Prefer primary sources: the paper itself, the filing, the official statistics agency, the organisation's own page. A blog citing a blog is not a source.
3. Confirm the number *and* its framing. "Revenue grew 40%" against a restated prior year is a different claim from the source's.
4. For any URL or citation, fetch it. A reference that 404s or points somewhere else is a fabrication regardless of how it got there.
5. Note the date the source was published and the date you checked it.

**Then, in the draft:**

- Correct anything wrong, and tell the user what you changed and why. Don't fix it silently.
- Replace vague attributions (pattern 5) with the real source now that you have it.
- Cut any claim you cannot verify. Say in your notes that you cut it and why.
- If the user supplied the figure and you can't confirm it, flag it rather than deleting it — it may be their own internal data.

**Never invent a citation to make a sentence look sourced.** A fabricated reference is the single worst failure this skill can produce. If no source exists, the sentence changes to reflect that, or it goes.

---

## Process

1. **Read the input carefully.** Note the author's actual voice before changing anything.
2. **Identify pattern instances.** Note the pattern number for each.
3. **Rewrite the problem sections.** Preserve every fact.
4. **Measure register and rhythm.** Count sentence lengths. Run the predictability test on any sentence that feels smooth.
5. **Verify facts and references.** Full pass, as above.
6. **Verify the prose:** rhythm varies, vocabulary is plain, details are specific, tone is consistent, constructions are simple.
7. **Present the draft.**

Then the audit, in the author's own words:

> "What makes the below so obviously AI generated?"

Answer in brief bullets, honestly, about your own draft.

> "Now make it not obviously AI generated."

Revise against those bullets and present the final version.

## Output Format

- The draft rewrite
- The audit: a short honest list of remaining tells
- The final version
- A verification note: what was checked, what was corrected, what couldn't be confirmed, with source links
- Optional: a summary of what changed and why, if the user asks

Deliver the final text plainly. Don't wrap it in commentary about how much more human it now sounds.

## Notes

- Some inputs are meant to be formal, listy, or promotional. Ask before flattening a press release into conversational prose.
- If the user supplies a sample of their own writing, match that instead of a generic human voice.
- Perfect prose is itself a tell. Leave the seams in.
- Legal, medical, and academic writing has register requirements that override patterns 26 and 28. Simplify the sentence structure there, not the terminology.

## Reference

- `references/ai-vocabulary.md` — the full flagged word and phrase list, tiered by strength of evidence, with sources.
- Wikipedia, *Signs of AI writing*, maintained by WikiProject AI Cleanup. The underlying reason these patterns cluster: LLMs use statistical algorithms to guess what should come next, which pulls output toward the statistically probable phrasing across every register at once.
- Juzek, T. S. and Ward, Z. B. (2024). *Why Does ChatGPT "Delve" So Much?* arXiv:2412.11385 — the frequency study behind Tier 1.
- GPTZero, *What is perplexity and burstiness for AI detection?* — the source of the two definitions in patterns 29 and 30, including its own note that it no longer uses them for detection.
