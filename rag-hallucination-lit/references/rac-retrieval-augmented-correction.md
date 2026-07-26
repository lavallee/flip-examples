---
type: Source
id: A3
aliases:
- A3
title: arxiv.org/pdf/2410.15667
description: arXiv 2410.15667, CC BY 4.0 (license verified on abs page 2026-07-26)
resource: https://arxiv.org/pdf/2410.15667
local: sources/raw/A3/capture.pdf
grade: A
status: captured
generated:
  by: agent:claude
  at: '2026-07-26T00:11:28Z'
support:
  basis: measured
  n: two factuality datasets (FActScore-style long-form eval)
  method: retrieval-augmented correction applied post-generation; factuality deltas vs baseline
    and prior correction methods
  vintage: 2024-10
  base_defined: true
independence: independent
screening:
  decision: include
  criterion: I1
  reason: "baseline generations vs retrieval-based correction, factuality quantified; note: correction-stage retrieval, not generation-stage"
extraction:
  method: post-hoc retrieval-augmented correction; FActScore-style factuality
  magnitude: up to 30% factuality improvement over prior methods; ~31-35% over instruction-tuned baseline with/without generation-RAG
  population: two long-form factuality datasets
  operationalization: atomic-fact support rate in long-form generation
---

# arxiv.org/pdf/2410.15667

arXiv 2410.15667, CC BY 4.0 (license verified on abs page 2026-07-26)
