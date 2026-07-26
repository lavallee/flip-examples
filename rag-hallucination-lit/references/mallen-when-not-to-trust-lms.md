---
type: Source
id: A2
aliases:
- A2
title: arxiv.org/pdf/2212.10511
description: arXiv 2212.10511, CC BY 4.0 (license verified on abs page 2026-07-26)
resource: https://arxiv.org/pdf/2212.10511
local: sources/raw/A2/capture.pdf
grade: A
status: captured
generated:
  by: agent:claude
  at: '2026-07-26T00:11:25Z'
support:
  basis: measured
  n: 'PopQA: 14k long-tail entity questions'
  method: QA accuracy on long-tail facts, vanilla LMs vs retrieval-augmented (Contriever/BM25/GenRead),
    adaptive-retrieval variant
  vintage: 2022-12
  base_defined: true
independence: independent
screening:
  decision: include
  criterion: I1
  reason: vanilla LMs vs retrieval-augmented across scales on PopQA
extraction:
  method: long-tail QA accuracy on PopQA
  magnitude: GPT-Neo 2.7B + Contriever outperforms vanilla GPT-3 175B; adaptive retrieval 46.5% (+5.3pp); retrieval harmful on ~10% of questions
  population: 14k PopQA questions, 10 LMs
  operationalization: parametric-knowledge failure proxied by long-tail QA accuracy
---

# arxiv.org/pdf/2212.10511

arXiv 2212.10511, CC BY 4.0 (license verified on abs page 2026-07-26)
