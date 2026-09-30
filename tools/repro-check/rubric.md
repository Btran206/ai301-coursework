# Rubric: is this reproduction package ready to post?

<!--
THIS IS THE PART YOU WRITE. The skill in SKILL.md executes whatever
checks you define here. It ships empty on purpose: the judgment is your
work.

A filled rubric must contain:

1. At least one row in the checks table. Each row needs all four
   columns:
   - Check: a short name (used in the output JSON).
   - Evidence: exactly what to look at, and where in the package. Name
     the part (the claim comment, the repro report's environment
     record, the artifacts read against the issue's description, the
     repo-facts block) or a location from your
     references/evidence-guide.md. "The report" is not a source; "the
     output excerpt read against the error the issue describes" is.
   - Pass condition: a decision rule about the OUTCOME that someone
     else could apply and get your answer. Judge the thing itself (does
     the artifact show the issue's behavior?), never the write-up's
     shape (how many steps it has, how long it is, whether it uses a
     template's headings). Structure-shaped checks are what make
     graders disagree with themselves.
   - Weight: `required` (a fail here holds the package) or `preferred`
     (never changes the verdict).

2. A verdict rule below the table: how the check grades combine into
   accept (ready) or reject (hold), including how `unclear` is
   treated. The verdict space is binary. If you write no rule for
   `unclear`, the skill treats it as fail.

Cover what actually gets bad packages posted. The lecture named the
proof families: the environment is recorded, the steps are complete
and followable, the behavior shown matches the issue (not an adjacent
one), the outcome is stated honestly (an evidenced cannot-reproduce is
a pass, a confident wrong-target is not), and the words respect the
repo's conventions. A rubric that ignores a family will fail eval
packages designed around that family.
-->

## Checks

| Check | Evidence | Pass condition | Weight |
|---|---|---|---|
| issue matches environment | the runtime/environment specifications provided in the repro report's environment record evaluated against the dependency and system requirements specified in the issue's description | The environment record lists software versions, runtime flags, and system parameters that match or reproduce the environment conditions where the issue was reported to occur. | required |
| steps are complete and followable | the numbered reproduction steps in the report, read against the artifacts (command output, logs, screenshots) attached to each step | Each step includes the exact command or action taken, and every step has a corresponding artifact showing its result; someone repeating the steps in order, with no other information, would land on the same outcome. | required |
| outcome is stated honestly | the report's stated conclusion (reproduced / could not reproduce / reproduced a different issue) read against the artifacts it cites as support | The stated conclusion matches what the cited artifacts actually show; a "could not reproduce" backed by a genuine attempt and its output is a pass, but a "reproduced" claim whose artifacts show a different or absent failure is a fail. | required |
| words respect repo conventions | the report's terminology, labels, and formatting compared against the repo-facts block (issue labels, templates, contribution guide wording) | The report uses the repo's own terms for components, labels, and severity, and follows any reproduction-report template the repo's contribution guide specifies, rather than introducing outside terminology or a different structure. | preferred |
| AI use is disclosed | the report's authorship/methodology section (or explicit absence of one) read against whether the package's steps, wording, or analysis were generated or drafted with AI assistance | If any part of the report (investigation, step drafting, log analysis, write-up) was produced with AI assistance and the repo's stated policy requires AI-use disclosure, fail only if no disclosure was provided otherwise pass. | required |
## Verdict rule

<!-- State how the grades above combine into accept or reject, and how
unclear is treated. Example shape (write your own): "accept if every
required check passes; preferred checks never change the verdict;
unclear counts as fail." -->
Ready if when every required check passes. Hold it if any required check fails or is unclear. Preferred checks never change an accept or reject verdict; they are used only to rank accepted issues. An unclear preferred check counts as not preferred but does not reject the issue.