---
type: Reference
title: "Selection flow (edition e1)"
edition: e1
---

# Selection flow — edition e1

The denominator, made visible. Counts from [search-log.md](search-log.md)
and the screening record; excluded-with-reasons are in each source page's
`screening:` frontmatter and `log/passed.jsonl`.

```
identified by search        Q1: 1,086 · Q2: 1,527 · Q3: 1   (API totals)
examined (title/abstract)   31   (top-15 per query + 1 targeted)
  └─ not advanced           24   (E1 no baseline / E3 mitigation-stacked:
                                  detectors and framework papers)
advanced to full screening   7
  └─ excluded               4
       rights only (E4/I4)  3   (2104.07567*, 2307.11019, 2404.08189)
       corpus not compare   1   (2401.00396 — E1, also E4)
included                     3   (2311.01307 → A1 · 2212.10511 → A2 ·
                                  2410.15667 → A3; all CC BY 4.0)
```

\* Substantively I1-qualifying — excluded on license alone; recorded as
negative evidence so no future pass re-chases it unknowingly.

Honesty note: "identified" counts are API totals for the queries, not a
deduplicated corpus census; only the top-15 relevance window per query
was examined. A fuller edition would page deeper — that is a scope
choice, stated rather than hidden.
