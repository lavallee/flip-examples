---
type: Forecast
id: FC3
aliases:
- FC3
description: Will the state silently revise the published 2025-26 enrollment ZIP (bytes differ
  from our 2026-07-25 capture, SHA-256 compared) by 2026-12-31?
question: Will the state silently revise the published 2025-26 enrollment ZIP (bytes differ
  from our 2026-07-25 capture, SHA-256 compared) by 2026-12-31?
resolves_by: '2026-12-31'
resolves_via:
- njdoe-enr-index
resolution_source_ladder:
- re-fetch https://www.nj.gov/education/doedata/enr/enr26/Enrollment_2526.zip and compare
  against nj-schools A4 fixity (sha in sources/_provenance.jsonl)
probability: 0.25
confidence: 0.5
base_rate: 1 of 4 captured files (2019-20) shows post-publication revision, made ~2 years
  after posting — mid-cycle revision within 5 months is rarer; the stale intro sheet is exactly
  the kind of defect the state historically leaves
predictability: gray-light
annul_if: the ZIP URL is retired or replaced rather than revised in place
bears_on:
- question:nj-schools:Q2
horizon: '2026'
opened: '2026-07-26'
freeze: '2026-07-26'
status: open
updates: []
generated:
  by: agent:claude
  at: '2026-07-26T01:01:28Z'
---

Will the state silently revise the published 2025-26 enrollment ZIP (bytes differ from our 2026-07-25 capture, SHA-256 compared) by 2026-12-31?
