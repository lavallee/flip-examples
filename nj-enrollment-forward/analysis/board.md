---
type: Finding
title: "The forecast board — edition e1"
---

# The forecast board — edition e1

*The notebook's output: what we've committed to, in one place, beside
the wiring that will score it. Regenerate judgments from the forecast
pages ([FC1]–[FC3]); this board is the readable render.*

**The headline.** New Jersey's statewide fall enrollment has been
sliding since 2023-24 — faster than the pandemic dip it recovered from.
We think it more likely than not (**p = 0.55**, confidence 0.6) that the
2026-27 file reports statewide enrollment **below 1,350,000** [FC1]. The
naive drift baseline lands at ≈1,346,600 — just under the line — so this
is a modest bet that the recent slide continues roughly as-is; one
strong pre-K expansion year (2023-24 added +1.29%) would clear the line
and resolve NO.

**The calibration pair** (near-dated on purpose — the record needs
volume before the scores mean anything):

- **p = 0.85** that the 2026-27 ZIP is posted at the DOE index by
  2027-02-28 [FC2] — 28 consecutive annual files argue yes; this mostly
  tests our read of the state's publication cadence.
- **p = 0.25** that the state *silently revises* the published 2025-26
  ZIP by 2026-12-31 [FC3] — resolved by re-fetching and comparing bytes
  against the hash [nj-schools](../../nj-schools/) captured on
  2026-07-25. The state's known behavior: revises rarely, silently, and
  late; leaves cosmetic defects (the stale intro sheet) alone.

**The record so far:** 0 scored · sharpness n/a · Brier n/a (needs ≥5).
An empty record, published anyway — that's the point: the credibility
accrues at resolution, not at assertion.

Every forecast carries its annulment condition (what would make the
question stop meaning anything) and a resolver ladder (what we actually
look at, in order, if the first source moves). The baseline above was
frozen in [baseline.md](../baseline.md) before anything resolved.
