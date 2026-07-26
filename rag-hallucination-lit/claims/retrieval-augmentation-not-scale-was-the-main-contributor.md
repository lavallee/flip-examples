---
type: Claim
id: C12
aliases:
- C12
description: Retrieval augmentation, not scale, was the main contributor to Atlas's superior
  factual consistency over closed-book LLaMA; scaling alone yielded roughly 1-3 p…
status: asserted
load_bearing: true
sources:
- id: A1
  resource: /references/galactica-factual-consistency-scaling-retrieval.md
  title: arxiv.org/pdf/2311.01307
independent_corroboration: 1
first_asserted: '2026-07-26'
generated:
  by: agent:claude
  at: '2026-07-26T00:13:39Z'
verified:
- by: agent:claude
  at: '2026-07-26T00:13:51Z'
  method: independent-sources
  against:
  - A1
  note: Single-study claim, scoped to its own paper's experiment; cross-study corroboration
    lives in C15.
---

Retrieval augmentation, not scale, was the main contributor to Atlas's superior factual consistency over closed-book LLaMA; scaling alone yielded roughly 1-3 percent consistency gains per model-size step[^A1]

[^A1]: [arxiv.org/pdf/2311.01307](../references/galactica-factual-consistency-scaling-retrieval.md)
