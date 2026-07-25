---
type: Notebook
description: NJ enrollment dip
---

# Reporter's notebook — NJ enrollment dip

## The tip

"NJ enrollment dipped in the pandemic" is repeated as settled background in
school-budget and facilities conversations. Did it, by how much, and — the
part nobody quotes — did it come back? The reader should leave able to say
what the statewide fall headcount actually did from 2019-20 to 2025-26,
with every number traceable to a hashed copy of the state's own file.

## Frame

Decision the reader should be able to make: whether "pandemic enrollment
loss" is still the right frame for NJ statewide planning arguments in 2026.
Headline claim, stated before building: the dip was real but modest, and
the interesting story is more recent. Counter-narrative to rule out: a
large, unrecovered pandemic collapse. Audience: anyone citing NJ enrollment
in a policy argument; no statistics background assumed.

## Hypotheses & falsifiers

- **H1** — Enrollment fell sharply in fall 2020. *Falsifier: the 2020-21
  All-Grades total is within noise of 2019-20.* → Survived only in
  weakened form: the drop was 0.98% [C1] — real, but "sharply" was wrong.
- **H2** — Enrollment has not recovered to pre-pandemic levels. *Falsifier:
  any later year at or above the 2019-20 total.* → **Falsified**: 2023-24
  came in 0.30% above 2019-20 [C2].
- **H3** (emerged during the work) — The current decline is a post-2023
  phenomenon, not a pandemic hangover. → Supported: 2025-26 is 1.63% below
  2023-24, a bigger fall than the pandemic dip itself [C3]. Drivers are the
  open thread [Q2].

## Sources & provenance

Four NJ DOE fall-enrollment workbooks (2019-20, 2020-21, 2023-24, 2025-26),
captured as published ZIPs from `nj.gov/education/doedata/enr/` — grade A
originals, bytes hashed at capture ([A1]–[A4], `sources/_provenance.jsonl`)
— plus the njschooldata.fyi dataset explainer for format-era and category
caveats ([A6], grade B, derivative). Totals were computed from the captured
bytes with openpyxl, two independent ways per year (State-sheet All-Grades
row; from-scratch District-sheet sum); the work log records the run and the
numbers. NJ DOE counts shared-time vocational students as 0.5, so totals
carry half-students — that is the file, not an error.

## Decisions

- [D1] Era-C workbooks only (2019-20 onward). Earlier files use two older
  container formats with shifted race/ethnicity categories; mixing eras can
  read a definitional change as a demographic swing (per [A6]).

## Renders

The public representation of these findings is
[njschooldata.fyi/reports/statewide-enrollment/](https://njschooldata.fyi/reports/statewide-enrollment/)
— a draft report presenting [C1]–[C3] with the year table, citing the four
upstream NJ DOE ZIPs inline and linking back here as the provenance trail.
The notebook is canonical; the page is a render. Corrections land here
first, then re-render.

## Gaps & self-critique

- Statewide totals hide composition: the post-2023 decline could be pre-K
  policy, kindergarten cohort size, migration, or nonpublic shift — [Q2] is
  open precisely because this notebook doesn't yet know.
- All four captures are one publisher (NJ DOE). Corroboration here is
  internal consistency and recomputation, not a second collector; NCES CCD
  would be the independent-pipeline check if the claims graduate beyond
  scout use.
- Fall snapshot only (15th school day of October); says nothing about
  within-year churn.
- The state silently revises published files (the 2019-20 ZIP's members
  were modified in 2022, per the work log) — our hashes pin what we
  analyzed; a re-capture may not match.
