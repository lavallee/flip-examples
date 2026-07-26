---
type: Reference
title: Search strategy log
---

# Search log — edition e1

All searches run 2026-07-26 against the arXiv API
(`export.arxiv.org/api/query`), relevance-sorted, top 15 examined at
title/abstract level per query. Totals are the API's own totalResults —
the denominator's denominator.

| # | query | total | examined |
|---|---|---|---|
| Q1 | `all:"retrieval augmented" AND all:hallucination` | 1,086 | 15 |
| Q2 | `all:"retrieval augmentation" AND (all:hallucination OR all:factuality)` | 1,527 | 15 |
| Q3 | `ti:"retrieval augmentation reduces hallucination"` (targeted: the known canonical paper) | 1 | 1 |

## Title/abstract screening notes (candidates not advanced to capture)

Most Q1/Q2 hits are **mitigation frameworks or detectors** (MultiRAG,
FAIR-RAG, Rowen, ReDeEP, FilterRAG, REFIND, FACTOID, InterpDetect …):
no non-retrieval baseline of the same model → **E1**, or retrieval stacked
with other interventions → **E3**. Not captured; listed here as the
screened denominator. Full-text screening decisions for advanced
candidates live on their references/ pages (`screening:` frontmatter);
rights-excluded papers are also in `log/passed.jsonl`.

Advanced to license check + capture decision: 2104.07567, 2311.01307,
2307.11019, 2404.08189, 2212.10511, 2401.00396, 2410.15667.
