# Update Log

## 2026-07-25

* **Update**: Oddity: Enrollment_2526.zip's 'Introduction and changes' sheet still says 2024-2025 (stale intro), but the State/District/School sheets are labeled 2025-2026 and carry 2025-26 data. Also the 2019-20 zip's members were last modified 2022-04 — the state silently revises published files; our hashes pin what we analyzed. _(agent:claude)_
* **Update**: Computed statewide fall-enrollment totals from the captured workbooks (openpyxl over sources/raw/A1-A4): State-sheet 'All Grades' row vs an independent sum of the District sheet's Total Enrollment column — both paths agree exactly for all four years. Totals: 2019-20 = 1,375,828.5; 2020-21 = 1,362,400.0; 2023-24 = 1,379,988.0; 2025-26 = 1,357,449.5. Half-counts are real: shared-time vocational students count 0.5 in DOE files (per A6). _(agent:claude)_
