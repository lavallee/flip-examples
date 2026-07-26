# flip-examples

Real, browsable [flip](https://github.com/lavallee/flip) notebooks —
research corpora with custody, grading, and corroboration discipline. Each
is a conformant OKF v0.2 knowledge bundle: plain markdown + YAML on disk,
readable here on GitHub, in any editor, or as an Obsidian vault.

**No human typed the flip commands in these notebooks.** That's the point.
Each was built by an AI agent inside an ordinary working conversation: the
human asked a question and directed follow-ups the way they normally would;
flip is the system that guided the agent to capture sources before citing
them, record judgments, gate claims behind a corroboration bar, and log its
own sessions. What you're browsing is the durable record that conversation
left behind — reusable, remixable, and auditable in a way a chat transcript
or a one-shot research PDF is not.

## nj-schools — "did NJ school enrollment actually dip?"

The whole notebook came from an exchange like this:

> **Human:** People keep saying NJ school enrollment dipped in the
> pandemic. Did it? Did it come back?
>
> **Agent:** *captures four NJ DOE fall-enrollment files (hashed at
> capture), grades them, computes statewide totals two independent ways,
> and answers:* The dip was real but modest — down 0.98% in fall 2020 —
> and it fully recovered by 2023-24. The story nobody quotes: enrollment
> has fallen 1.63% since 2023-24, a bigger decline than the pandemic dip.
> Three claims verified by recomputation; one question answered; a new one
> opened — what's driving the recent decline?

The findings now live at
[njschooldata.fyi/reports/statewide-enrollment/](https://njschooldata.fyi/reports/statewide-enrollment/)
— a public page that cites the upstream NJ DOE files and links back to this
notebook as its provenance trail. The notebook is canonical; the page is a
render.

What that left on disk, in [`nj-schools/`](nj-schools/):

- [`notebook.md`](nj-schools/notebook.md) — the tip, hypotheses with named
  falsifiers (one survived weakened, one falsified, one emerged), gaps.
- [`references/`](nj-schools/references/) — five graded sources; the four
  NJ DOE workbooks are grade-A originals with their raw bytes under
  [`sources/raw/`](nj-schools/sources/raw/) and SHA-256 fixity in the
  capture ledger.
- [`claims/`](nj-schools/claims/) — three load-bearing claims, each
  footnote-cited to sources and carrying a recomputation verification
  event. flip refuses `verified` status until the bar is met.
- [`questions/`](nj-schools/questions/), [`decisions/`](nj-schools/decisions/),
  [`sessions/`](nj-schools/sessions/), [`log.md`](nj-schools/log.md) — the
  answered and open questions, the era-selection decision, the agent's
  session record, and the work log (including two file oddities the state
  won't tell you about: a stale intro sheet, and silent revision of a
  published ZIP).

## rag-hallucination-lit — "review the literature on retrieval and hallucination"

The first notebook built with an **outcome kind**: `flip new
rag-hallucination-lit --kind "literature review"` — the plain-language
phrase resolves to the `lit-review` kind, whose collection contract the
doctor enforces from day one. What that discipline produced, in
[`rag-hallucination-lit/`](rag-hallucination-lit/):

- [`criteria.md`](rag-hallucination-lit/criteria.md) — inclusion/exclusion
  **frozen before the first search** (the contract's
  unrecoverable-by-construction entry, done prospectively).
- [`search-log.md`](rag-hallucination-lit/search-log.md) and
  [`flow.md`](rag-hallucination-lit/flow.md) — the denominator: 2,600+
  identified, 31 examined, 7 advanced, 4 excluded with typed reasons,
  3 included. The canonical Shuster 2021 paper is excluded **on license
  alone** (this notebook redistributes its captured PDFs, so only
  CC-licensed papers can be included) — recorded as negative evidence,
  not erased.
- [`review.md`](rag-hallucination-lit/review.md) — edition e1: the effect
  is consistent (retrieval improved every reported metric, including a
  2.7B model beating vanilla GPT-3 175B on long-tail QA), the construct
  is not (three papers, three different operationalizations of
  "hallucination"), and retrieval hurt on ~10% of questions.
- Every included source: hashed CC-BY PDF, support tuple (independent ·
  measured · base-defined), screening decision and extraction fields in
  frontmatter. The synthesis claim is verified through the corroboration
  bar at 3; the claim ledger also shows ten burned claim ids from the
  agent's own YAML mistakes — ids are never reused, and the record keeps
  the stumbles.

## nj-enrollment-forward — "what should we watch?"

The companion to nj-schools, built with the `forward-set` kind (flip
0.13's Forecast class): the backward notebook proved what enrollment
*did*; this one commits to what the same watched surface will show next.
Three dated forecasts with probabilities, confidence, annulment
conditions, and resolver ladders — including one that resolves by
re-fetching the state's ZIP and comparing bytes against nj-schools'
captured hash. The [naive baseline](nj-enrollment-forward/baseline.md) is
declared before anything resolves; the record starts honestly at zero.
Claims carry grades, never probabilities; forecasts carry probabilities,
never grades — and `flip doctor` enforces it.

Also featured: [flip's own website notebook](https://github.com/lavallee/flip/tree/main/website/notebook)
— the notebook backing every claim on the flip site, including a superseded
claim kept on the record when OKF moved from v0.1 to v0.2.

## Rights

Featured notebooks ship their captured bytes, so every capture here is
redistributable: NJ DOE enrollment files are New Jersey public records
published for reuse; the njschooldata.fyi explainer is the maintainer's own
work. Notebook prose and structure: MIT, like flip itself.

## Exploring

```bash
uv tool install flip-notebook
cd nj-schools
flip show      # open questions, claims needing work, recent activity
flip doctor    # audit custody, grading, and the verification bar
```

Or skip the CLI entirely — every entity is one markdown page with its
metadata in frontmatter. Start at [`nj-schools/index.md`](nj-schools/index.md).
