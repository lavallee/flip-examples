---
type: Source
id: A1
aliases:
- A1
title: arxiv.org/pdf/2311.01307
description: arXiv 2311.01307, CC BY 4.0 (license verified on abs page 2026-07-26)
resource: https://arxiv.org/pdf/2311.01307
local: sources/raw/A1/capture.pdf
grade: A
status: captured
generated:
  by: agent:claude
  at: '2026-07-26T00:11:22Z'
support:
  basis: measured
  n: ParaRel* paraphrase sets; LLaMA 7B-65B and Atlas 11B evaluated
  method: factual consistency (agreement of predictions across paraphrases) on ParaRel*, closed-book
    LLMs vs retrieval-augmented Atlas
  vintage: 2023-11
  base_defined: true
independence: independent
screening:
  decision: include
  criterion: I1
  reason: closed-book LLaMA vs retrieval-augmented Atlas, consistency quantified
extraction:
  method: paraphrase-consistency on ParaRel*
  magnitude: retrieval augmentation the main contributor to Atlas's superior consistency; scaling alone ~1% (LLaMA) to 3% (Atlas) per size step
  population: LLaMA 7B-65B, Atlas 11B
  operationalization: "consistency, not truth: agreement across paraphrases"
---

# arxiv.org/pdf/2311.01307

arXiv 2311.01307, CC BY 4.0 (license verified on abs page 2026-07-26)
