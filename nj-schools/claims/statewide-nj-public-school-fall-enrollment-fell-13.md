---
type: Claim
id: C1
aliases:
- C1
description: Statewide NJ public school fall enrollment fell 13,428.5 (0.98 percent) from
  2019-20 (1,375,828.5) to 2020-21 (1,362,400.0), the pandemic-year dip
status: verified
load_bearing: true
sources:
- id: A1
  resource: /references/njdoe-fall-enrollment-2019-20.md
  title: www.nj.gov/education/doedata/enr/enr20/enrollment_1920.zip
- id: A2
  resource: /references/njdoe-fall-enrollment-2020-21.md
  title: www.nj.gov/education/doedata/enr/enr21/enrollment_2021.zip
independent_corroboration: 2
first_asserted: '2026-07-25'
generated:
  by: agent:claude
  at: '2026-07-25T16:59:47Z'
verified:
- by: agent:claude
  at: '2026-07-25T16:59:58Z'
  method: recomputation
  against:
  - A1
  note: 'Statewide total re-derived two independent ways from the captured bytes: the State
    sheet''s All Grades row, and a from-scratch sum of the District sheet''s Total Enrollment
    column. Both agree to the half-student for every year involved.'
---

Statewide NJ public school fall enrollment fell 13,428.5 (0.98 percent) from 2019-20 (1,375,828.5) to 2020-21 (1,362,400.0), the pandemic-year dip[^A1][^A2]

[^A1]: [www.nj.gov/education/doedata/enr/enr20/enrollment_1920.zip](../references/njdoe-fall-enrollment-2019-20.md)
[^A2]: [www.nj.gov/education/doedata/enr/enr21/enrollment_2021.zip](../references/njdoe-fall-enrollment-2020-21.md)
