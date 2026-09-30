# Evidence guide: where proof lives in a reproduction package

## Environment

Where it lives: the environment line in the repro report, checked
against the version/OS the issue targets (stated directly, or implied
by the repo facts' latest-release line).

What good looks like: specific versions and OS/arch actually used, not
"latest"; any gap from the issue's target is called out and explained.

## Steps

Where it lives: the step-by-step sequence in the repro report, checked
against the issue's own minimal-repro steps and starting-state
assumptions.

What good looks like: each step names the exact command or action, in
order, from a stated starting point — a stranger with only the report
could run it and land in the same state.

## Behavior shown

Where it lives: the output/log excerpt in the repro report, checked
against the "current" vs. "expected" behavior the issue describes.
Thread highlights are context, not proof.

What good looks like: the captured output shows the same symptom at the
same trigger condition as the issue, not an adjacent or similar-looking
failure.

## Honesty

Where it lives: the report's stated conclusion (reproduced / cannot
reproduce / different issue), checked against the artifact it cites as
backing.

What good looks like: the conclusion claims no more than the evidence
shows — an honest cannot-reproduce with a real attempt attached is a
pass; a confident claim resting on hearsay or restated issue text
instead of independent output is a fail.

## Comms

Where it lives: the claim comment, checked against the repo's bug
report template and any AI-use or contribution policy in the repo
facts.

What good looks like: the comment claims only what the attached report
actually backs up, and discloses AI assistance if the repo's policy
requires it.
