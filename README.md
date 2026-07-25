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
