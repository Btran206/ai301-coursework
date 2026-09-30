# Unit 2 — Claim and Reproduce

Path: `beat-1-sandbox/unit-2/reproduction.md`

Record of your claim and reproduction on the issue you chose in Unit 1, and of the
evaluation runs that produced `eval-run.txt`. This file is graded at the path above; a copy
kept anywhere else in the repository is not read.

Complete every labelled field below. Each is graded on its own; content placed under the wrong
label is not graded.

---

## Your identity upstream

**GitHub username**

Btran206

---

## Posted upstream

**Claim comment**

https://github.com/codepath/pathreview-ai301-fa26-s1/issues/55#issuecomment-5903517044

Hi! I'd like to work on this one.

So far my understanding is _detect_languages in ingestion/parsers/skill_extractor.py only recognizes JS/TS via the filename arg's .js/.ts extension, an import/require regex, or the literal string package.json in the text, so JS/TS mentioned any other way doesn't work. I'll start by running pytest to confirm the failing/xfailed tests and then look at broadening the detection logic to account for .js/.ts args outside of the filename.

**Reproduction comment**

https://github.com/codepath/pathreview-ai301-fa26-s1/issues/55#issuecomment-5904975842

**Environment**
- OS: Windows 11 (MINGW64/Git Bash, `MINGW64_NT-10.0-26200 3.6.5-22c95533.x86_64`)
- Python: 3.11.9
- pytest: 9.1.1
- Repo state: `codepath/pathreview-ai301-fa26-s1` @ `f89c06fc3ff292df2a04a39ac51319d32a76b779` (main)

**Steps to reproduce**
1. `python -m pytest tests/unit/test_skill_extractor.py -v`
2. Reproduce independent of pytest:
   ```python
   from ingestion.parsers.skill_extractor import SkillExtractor
   e = SkillExtractor()
   print(e.extract_skills('const fs = require("fs");'))
   ```
**Results**
- Step 1: `13 passed, 5 xfailed`.
- The 5 xfailed tests (all marked `xfail(strict=True, reason="issue #55: skill extractor does not detect JavaScript/TypeScript")`):
  - `test_text_with_typescript_files`
  - `test_javascript_detection`
  - `test_database_technology_detection`
  - `test_devops_tool_detection`
  - `test_docker_compose_detection`

- Step 2 prints `[]` — no skills detected at all for a plain JS `require(...)` call with no filename hint.

- This confirms the issue reproduces as described on the current main branch, both via the test suite and directly.

## Eval iterations

Answer all four sections. Quote source text directly; paraphrase does not satisfy these
fields.

**Run history**

1. 18/20 first run without saving to eval-run.txt
2. 18/20 ran again with same rubric but saved to eval-run.txt

**Package analysis**

pkg-10 (starship/starship#7648): Evaluated as Reject under current rubric criteria due to a failure on issue matches environment (Gold standard: Accept). The report transparently notes that the issue could not be reproduced on Linux + zsh, accurately cites the original environment (macOS + fish), and supports the attempt with execution output. While this represents a thorough non-reproducibility finding rather than an incomplete evaluation, the check currently enforces a strict match between the environment record and the reported issue without an exception for disclosed discrepancies.

**Check rationale**

From `rubric.md`:

the issue matches environment check is deliberately designed as a strict literal match to prevent no-evidence submissions from passing with missing or unrelated environment data. pkg-10 highlights a known edge case where a fully documented, valid attempt in a different environment is evaluated under the same strict criteria as an unsupported submission.

**Trade-offs**

Re-evaluation using --only pkg-10 yielded a consistent Reject on the same check. The strict criteria will remain unchanged. Relaxing the rule to accommodate explicitly noted environment mismatches introduces a risk where no-evidence packages could pass simply by adding a disclaimer instead of executing proper verification.

---

Related paths: `eval-run.txt` in this directory; your skill's files in
`tools/repro-check/`.
