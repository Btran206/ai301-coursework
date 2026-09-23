# Unit 1 — Issue Selection

Path: `beat-1-sandbox/unit-1/selection.md`

Record of the issue carried into Unit 2, and of the evaluation runs that produced
`eval-run.txt`. This file is graded at the path above; a copy kept anywhere else in
the repository is not read.

Complete every labelled field below. Each is graded on its own; content placed under the
wrong label is not graded.

---

## Selected issue

**Issue link**

https://github.com/codepath/pathreview-ai301-fa26-s1/issues/55

**Verdict output**

```
 #55 — Skill extractor fails to detect JS/TS: unassigned, 0 comments, no linked PR, no umbrella/splitting language or
  unresolved design debate in the body — it's one stated goal (fix detection logic) touching multiple functions, which
  the rubric treats as one deliverable, not an umbrella issue. Lacks the good first issue label (preferred check only).
  All required checks pass. Accept.

{
      "item": "https://github.com/codepath/pathreview-ai301-fa26-s1/issues/55",
      "checks": [
        {"name": "Maintainer alive", "grade": "pass", "evidence": "most recent default-branch commit 2026-09-16, 6 days
  before capture"},
        {"name": "Repo not abandoned", "grade": "pass", "evidence": "archived: false, pushed_at 2026-09-16T21:48:27Z,
  within 90 days"},
        {"name": "Unclaimed", "grade": "pass", "evidence": "assignees: [], comments: 0, no linked PR found via search"},
        {"name": "AI Contribution policy", "grade": "pass", "evidence": "no CONTRIBUTING/AI policy files found —
  silence"},
        {"name": "Good-first-issue label", "grade": "fail", "evidence": "labels are only bug, ingestion, tier-1 — no
  'good first issue' label"},
        {"name": "Scope fits a newcomer", "grade": "pass", "evidence": "one stated goal (fix detection in
  skill_extractor.py) spanning several functions/tests, but no explicit umbrella/split-into-separate-PRs language or
  unresolved design debate in the body"}
      ],
      "verdict": "accept"
}
```

---

## Eval iterations

Quote source text directly in each field below. Paraphrase does not satisfy them.

**Run history**

[The agreement score of each run you did, in order. A single run is a complete answer if
only one run occurred. **The last score in your list must match the agreement line in the
`eval-run.txt` you committed** — that file is the record of your final run.]

agreement: 17/20 scored items  (bar: 18/20: below the bar)

agreement: 16/20 scored items  (bar: 18/20: below the bar)

agreement: 19/20 scored items  (bar: 18/20: PASS)

**Issue analysis**

issue-19: gold label: accept, verdict: reject. This issue kept getting identified as an umbrella issue when it was one bug with several candidate causes.

**Check rationale**

[One check from the `rubric.md` uploaded to `tools/issue-select/`, quoted as it is
currently written, with the reasoning behind its current form.]

| Check | Evidence | Pass condition | Weight |
|---|---|---|---|
| Scope fits a newcomer | Issue body and comment thread text | Fails if: the issue's own text designates its listed items as separate work meant to be split into multiple tracked issues/PRs (an umbrella/tracking issue — e.g. a checklist of links to distinct sub-issues, or wording like "each of these should get its own PR"); the issue is a pure usage/support question ("how do I get this to work?") rather than a request for a change; for a feature request, the design or acceptance criteria are still an open question the issue or thread itself flags as unresolved (untried alternatives, placeholder/TBD details, a pending roadmap or maintainer decision); or 2 or more closed/unmerged PRs, or 3 or more separate claim-then-abandon cycles, already exist against this issue. A single fix or feature that happens to touch several files, functions, or root causes in service of one stated goal is NOT an umbrella issue, even if the writeup is long or multi-part — it is still one deliverable, meant to land as one PR. A terse or short body is not itself a scope failure either — grade the size of the work being asked for, not the polish of the writeup. Otherwise pass | required |

**Trade-offs**

I re-ran issue-19 in isolation after rewording the pass condition specific to that failure. So there is some ambiguity with the wording specific to the boundary for this check. It might not be a catch all check because scope fits a newcomer is very broad.

---

## Selection rationale

**Selection rationale**

1. This issue fits my interest because it's with a language I am comfortable with and I am open to new languages/frameworks that I haven't worked with before. It's also not too challenging since it's a tier 1 which should fit the newcomer scope.
2. The verdict identified all of my checks besides the newcomer scope but since this is a tier 1 issue, It should be ok. 
3. I shouldn't have any issue claiming this issue because there are 0 comments and no linked PR and doesn't seem to be claimed.

---

Related paths: `eval-run.txt` in this directory; your skill's files in
`tools/issue-select/`.
