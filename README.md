# ai-content-humaniser

A Claude skill that rewrites text so it stops reading like a machine wrote it.

It works in three passes. First it strips the statistical tells — 30 catalogued patterns, from `delve` and em dash overuse to the rule of three. Then it puts a human back in: opinions, uneven rhythm, specific detail. Then it fact-checks every statistic, quote, and reference in the draft, because a more persuasive document with wrong numbers in it is worse than an obviously robotic one.

## Install

Drop it in your skills directory:

```bash
git clone https://github.com/area51prog/ai-content-humaniser.git
mkdir -p ~/.claude/skills
cp -r ai-content-humaniser/skill ~/.claude/skills/humaniser
```

Or copy `skill/SKILL.md` and `skill/references/` into `~/.claude/skills/humaniser/` by hand. For a project-local install, use `.claude/skills/` inside the repo instead.

The `humaniser.skill` file in releases is the same content zipped, for clients that install from a bundle.

## Use

It triggers on its own when you ask for the obvious things:

> Humanise this draft.
> Does this sound AI-generated?
> Make this read like a person wrote it.
> Edit this so it doesn't get flagged as AI.

You get back a draft, an honest audit of what still reads as generated, a final version, and a verification note listing what was checked and what couldn't be confirmed.

See [EXAMPLE.md](EXAMPLE.md) for a full worked run.

## What it checks

**Content** — inflated significance, hollow notability claims, superficial `-ing` analyses, promotional language, vague attributions, bolted-on "challenges" sections.

**Language** — overused AI vocabulary, copula avoidance (`serves as` for `is`), negative parallelisms (`not just X, it's Y`), rule-of-three padding, elegant variation, false ranges.

**Style** — em dashes, boldface, inline-header bullet lists, Title Case headings, emojis, curly quotes.

**Communication** — assistant residue (`I hope this helps`), knowledge-cutoff disclaimers, sycophantic tone.

**Filler** — stock filler phrases, stacked hedges, generic upbeat conclusions, hyphenated compound overuse.

**Register and rhythm** — over-complex vocabulary, over-complex sentence construction, over-polished grammar, mechanical sentence rhythm (burstiness), statistically predictable phrasing (perplexity).

**Facts** — every figure, date, quote, name, and URL, checked against primary sources before delivery.

## The vocabulary list

`skill/references/ai-vocabulary.md` holds the flagged words, tiered by how good the evidence actually is.

Tier 1 is the only research-backed set. Juzek and Ward measured ChatGPT's word frequencies against human-written scientific abstracts and isolated 21 overrepresented terms — `delve`, `showcase`, `boasts`, `underscore`, `intricacies`, `realm`, `garnered`, `groundbreaking`, `advancements`, `aligns` and their inflections. A hit there is close to conclusive.

Tier 2 is roughly fifty widely reported words with weaker evidence behind them. Tier 3 is stock phrases. Tier 4 is assistant residue that should never survive into a finished document.

Nothing on the list is banned. Each entry is a flag meaning *check whether a plainer word works*. The list also warns about the obvious trap: swapping `delve into` for `plumb the depths of` fails the plain-vocabulary check instead of passing it.

Word lists rot. The tells that gave a model away in 2024 are partly trained out by now. Re-check the sources every six months or so.

## On perplexity and burstiness

Two of the checks use these, and the skill is deliberately honest about their limits.

Perplexity is how predictable the word choices are. Burstiness is how much sentence construction varies across a document. Both make decent editing heuristics — "count the words in each sentence and read the numbers" catches flat rhythm fast.

They are not detector scores. GPTZero, which popularised the pair, moved off them to a deep-learning model in autumn 2023 and states there is no absolute scale for either. The skill uses them as writing tools and explicitly refuses to promise that a rewrite will pass any detector. Treat anything claiming otherwise with suspicion.

## Repo layout

```
skill/
  SKILL.md                      the skill itself
  references/
    ai-vocabulary.md            tiered word and phrase lists, with sources
EXAMPLE.md                      a full worked before/after run
CHANGELOG.md
LICENSE
```

## Credit

Forked in spirit from [YKehinde/humaniser](https://github.com/YKehinde/humaniser), MIT licensed. This version keeps the original's structure — the pattern catalogue, the two-step audit, the "personality and soul" idea — and adds the tiered vocabulary reference, the four register-and-rhythm checks, and the fact-verification pass.

Be aware: **the before/after examples here are rewritten, not copied from upstream.** They were reconstructed from the original's structure rather than lifted, so they illustrate the same patterns with different text. If you want the originals, go read the source repo.

The pattern catalogue ultimately comes from Wikipedia's [Signs of AI writing](https://en.wikipedia.org/wiki/Wikipedia:Signs_of_AI_writing), maintained by WikiProject AI Cleanup. They did the documentation work that everything downstream, including this, is built on.

Research behind the vocabulary tiers: Juzek, T. S. and Ward, Z. B. (2024), *Why Does ChatGPT "Delve" So Much? Exploring the Sources of Lexical Overrepresentation in Large Language Models*, [arXiv:2412.11385](https://arxiv.org/abs/2412.11385).

## Contributing

Useful contributions, roughly in order of value:

1. Words that should be added to or removed from Tier 2, with frequency evidence attached.
2. Patterns from newer models that aren't catalogued yet.
3. Before/after pairs that are better than the ones in here. Several are serviceable rather than good.

Open an issue before a large restructure.

## License

MIT. See [LICENSE](LICENSE).
