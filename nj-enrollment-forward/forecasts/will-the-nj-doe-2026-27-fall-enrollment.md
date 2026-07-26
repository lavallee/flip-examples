---
type: Forecast
id: FC1
aliases:
- FC1
description: Will the NJ DOE 2026-27 fall-enrollment file report statewide All Grades enrollment
  below 1,350,000?
question: Will the NJ DOE 2026-27 fall-enrollment file report statewide All Grades enrollment
  below 1,350,000?
resolves_by: '2027-06-30'
resolves_via:
- njdoe-enr-index
resolution_source_ladder:
- https://www.nj.gov/education/doedata/enr/ -> enr27 ZIP -> State sheet All Grades row
- 'if the modern format is discontinued: District sheet Total Enrollment sum, per the recomputation
  method proven in nj-schools'
probability: 0.55
confidence: 0.6
base_rate: 2 of 4 captured years moved >0.5% year-over-year; recent drift -0.8%/yr from 1,357,449.5
  implies ~1,346,600 for 2026-27 — under the line, but one strong pre-K expansion year (like
  2023-24's +1.29%) clears it
predictability: gray-light
annul_if: NJ DOE stops publishing the fall file, changes the counting convention (e.g. drops
  half-count shared-time students), or redefines All Grades scope
bears_on:
- claim:nj-schools:C3
horizon: '2027'
opened: '2026-07-26'
freeze: '2026-07-26'
status: open
updates: []
generated:
  by: agent:claude
  at: '2026-07-26T01:01:11Z'
---

Will the NJ DOE 2026-27 fall-enrollment file report statewide All Grades enrollment below 1,350,000?
