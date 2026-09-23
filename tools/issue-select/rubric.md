# Rubric: is this a good first issue?

<!--
THIS IS THE PART YOU WRITE. The skill in SKILL.md executes whatever checks
you define here. It ships empty on purpose: the judgment is your work.

A filled rubric must contain:

1. At least one row in the checks table. Each row needs all four columns:
   - Check: a short name (used in the output JSON).
   - Evidence: exactly what to look at, and where. Name the source
     (repo-facts block, issue body, comment thread, or the locations in
     references/evidence-guide.md). "The repo" is not a source; "the last
     5 default-branch commit dates" is.
   - Pass condition: a condition someone else could apply and get your
     answer. Prefer thresholds with numbers ("a maintainer commented
     within 30 days") over adjectives ("maintainer is responsive").
   - Weight: `required` (a fail here rejects the issue) or `preferred`
     (never changes the verdict; a nice-to-have that helps rank the
     issues you accept).

2. A verdict rule below the table: how the check grades combine into
   accept or reject, including how `unclear` is treated. The verdict
   space is binary. If you write no rule for `unclear`, the skill treats
   it as fail.

Cover what actually kills first contributions. The lecture named four
families: the maintainer is alive, the repo is in use, the scope fits a
newcomer, and nobody else is already on it. A rubric that ignores a family
will fail eval issues designed around that family.
-->

## Checks

| Check | Evidence | Pass condition | Weight |
|---|---|---|---|
| Maintainer alive | last 5 default-branch commit dates | At least one commit in the last 60 days | required |
| Repo not abandoned | archived: flag and "last push to any branch" | `archived` is false, and the last push (any branch) is within 90 days of the capture date | required |
| Unclaimed | this issue: assignees: and linked PRs: with state, plus Comments section | No assignee, and no open linked PR, and no unanswered "I'll take this" style comment from another contributor in the last 90 days | required |
| AI Contribution policy | contribution policy line (CONTRIBUTING.md / AI policy files / templates) | No outright ban on AI-generated contributions; conditions (disclosure, testing, human review) are fine | required |
| Good-first-issue label | issue's labels | Issue has a `good first issue` (or equivalent) label | preferred |
| Scope fits a newcomer | Issue body and comment thread text | Fails if: the issue's own text designates its listed items as separate work meant to be split into multiple tracked issues/PRs (an umbrella/tracking issue — e.g. a checklist of links to distinct sub-issues, or wording like "each of these should get its own PR"); the issue is a pure usage/support question ("how do I get this to work?") rather than a request for a change; for a feature request, the design or acceptance criteria are still an open question the issue or thread itself flags as unresolved (untried alternatives, placeholder/TBD details, a pending roadmap or maintainer decision); or 2 or more closed/unmerged PRs, or 3 or more separate claim-then-abandon cycles, already exist against this issue. A single fix or feature that happens to touch several files, functions, or root causes in service of one stated goal is NOT an umbrella issue, even if the writeup is long or multi-part — it is still one deliverable, meant to land as one PR. A terse or short body is not itself a scope failure either — grade the size of the work being asked for, not the polish of the writeup. Otherwise pass | required |

## Verdict rule

Accept an issue only when every required check passes. Reject it if any required check fails or is unclear. Preferred checks never change an accept or reject verdict; they are used only to rank accepted issues. An unclear preferred check counts as not preferred but does not reject the issue.
