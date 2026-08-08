# Changelog

All notable changes to this skill. Format follows [Keep a Changelog](https://keepachangelog.com/en/1.1.0/); versions follow [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [3.0.0] — 2026-08-08

First release of this fork.

### Added

- **`references/ai-vocabulary.md`** — the flagged word and phrase list, moved out of `SKILL.md` and expanded, tiered by strength of evidence:
  - Tier 1: 21 terms with measured overrepresentation, from Juzek and Ward (2024).
  - Tier 2: ~50 widely reported words, grouped by part of speech.
  - Tier 3: stock phrases.
  - Tier 4: assistant residue.
  - Includes a warning against replacing flagged words with fancier synonyms, and a note that word lists need re-checking roughly twice a year.
- **Pattern 26, over-complex vocabulary** — conversion table, plus an exception for genuine technical terminology.
- **Pattern 27, over-complex sentence construction** — hard limits: at most two clauses before the main verb, break sentences over ~35 words, promote nested parentheticals.
- **Pattern 28, over-polished grammar** — contractions, sentence-initial conjunctions, fragments. Explicitly: add informality, not errors.
- **Pattern 29, mechanical rhythm** — burstiness as a countable check, with per-paragraph targets for sentence-length variation.
- **Pattern 30, statistically predictable phrasing** — perplexity as a stop-before-the-last-word test, fixed with specific content rather than unusual words.
- **Fact and Reference Verification section** — a required pass covering statistics, quotes, names, and URLs, with primary-source preference, link-resolution checks, and an absolute prohibition on inventing citations.
- `WebSearch` and `WebFetch` added to `allowed-tools`, needed for verification.
- Verification note added to the required output format.
- Register exception for legal, medical, and academic writing: simplify structure, not terminology.

### Changed

- Task list expanded from five steps to six; process expanded from five to seven.
- Pattern 7 now points to the reference file instead of inlining the list.
- Description rewritten to cover the new checks and improve trigger accuracy.

### Notes

- Patterns 29 and 30 carry an explicit caveat that perplexity and burstiness are editing heuristics, not detector scores. GPTZero, which popularised them, moved off both in autumn 2023 and states there is no absolute scale for either. The skill is instructed never to promise a detector pass.
- **All before/after examples in this fork are original.** They were reconstructed from the upstream skill's structure rather than copied, so they illustrate the same patterns with different text.

## [2.3.0] — upstream

The version this fork started from: [YKehinde/humaniser](https://github.com/YKehinde/humaniser). 25 patterns in five groups, the personality-and-soul section, and the two-step audit process. MIT licensed.
