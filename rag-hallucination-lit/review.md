---
type: Reference
title: "Review — does retrieval augmentation reduce hallucination? (edition e1)"
edition: e1
---

# Does retrieval augmentation reduce hallucination? — edition e1

*A small living review, built under flip's `lit-review` kind: criteria
frozen before searching ([criteria.md](criteria.md)), denominator in
[flow.md](flow.md), search trail in [search-log.md](search-log.md). Three
included studies — every number below traces to a hashed, redistributable
capture.*

## Methods

Criteria were frozen 2026-07-26 before the first query (criteria.md).
Three arXiv API searches (search-log.md) yielded 30 examined
titles/abstracts plus one targeted lookup; seven candidates advanced to
full screening; four were excluded — three solely on rights (I4: this
notebook redistributes its captured PDFs, so only CC-licensed papers can
be *included*; their existence is recorded, not erased) and one as a
corpus rather than a comparison (E1). Three CC-BY studies were included,
captured, graded, and extracted (the extraction table lives on each
source page's `extraction:` frontmatter).

## What the included studies show

**The effect is consistent.** All three studies find retrieval
interventions improving their hallucination-adjacent metric against
non-retrieval baselines [C15]:

- On long-tail factual QA (PopQA), a 2.7B-parameter model with retrieval
  outperformed vanilla GPT-3 at 175B [C11] — parametric scale does not
  substitute for looking things up, on the facts the parameters never
  absorbed ([A2]).
- On factual *consistency* (stable answers across paraphrases),
  retrieval augmentation — not scale — was the main contributor to
  Atlas's advantage over closed-book LLaMA; scaling alone bought roughly
  1–3% per size step [C12] ([A1]).
- Applied post-hoc, retrieval-augmented correction improved long-form
  factuality by up to 30% over prior correction methods [C13] ([A3]).

**The construct is not.** "Hallucination" is operationalized three
different ways here — paraphrase consistency ([A1]), long-tail QA
accuracy ([A2]), atomic-fact support in long-form generation ([A3]).
The shared headline ("retrieval helps") papers over genuinely different
measured quantities; anyone citing "retrieval reduces hallucination by
X%" should say which X they mean [C15].

**And it is not free.** On roughly 10% of PopQA questions, retrieval
*hurt* — the retrieved text was worse than the parametric answer [C14]
([A2]); the same paper's adaptive-retrieval result (46.5%, +5.3pp) is a
direct measure of how much deciding *when* to retrieve is worth.

## Limits of this edition

- Three studies, all pre-2025 models: whether these gains persist for
  post-2024 frontier models with far stronger parametric knowledge is
  the open question this review watches ([Q1], resolves via arXiv).
- The rights criterion (I4) excluded the canonical Shuster et al. 2021
  conversation study on license alone — its absence here is custody
  policy, not editorial judgment (see log/passed.jsonl).
- Correction-stage retrieval ([A3]) and generation-stage retrieval
  ([A1], [A2]) are different interventions; e1 groups them deliberately
  and flags it here.

*Living mode: scheduled re-search every 180 days; a retraction or
standing change on any included source triggers a targeted re-screen and
a new edition. This edition is immutable — corrections issue e2.*
