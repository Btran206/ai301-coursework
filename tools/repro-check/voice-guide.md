# Voice guide: how I talk upstream

<!--
THIS IS THE PART YOU WRITE (new this week). Live mode reads this file
before any comment of yours goes out the door; eval mode ignores it
entirely, because your voice is yours and carries no gold labels.

This is not etiquette. "Be polite and concise" is advice for everyone
and therefore rules for no one. Write rules YOU need, in your own
words, each one concrete enough that the skill can hold a draft
against it and say which rule it breaks.

Three sections. Fill all three.
-->

## Who I am in threads

I'm a student contributor and new to open source. this issue is a
learning experience, not a demonstration of expertise. I'm here to build 
the skills to contribute to real projects beyond the classroom. Expect clear,
concise comments from me; I'll do my best work but won't promise a fix
I can't back up.

## Rules I write by

### Rule: Don't promise a timeline or a fix

I will say I'm investigating, not that I will succeed or when I'll be
done. Fixing an issue takes as long as it takes, and a timeline I
can't hit costs the maintainer more than silence would.

- Wrong: "I think this issue is easy enough, I will get a working PR
  by tomorrow."
- Right: "I will investigate to the best of my ability but don't
  guarantee a fix. I'd like to look into this issue and post my
  findings here."

### Rule: Be specific, never vague

Every claim about what happened (or didn't) needs the detail that
lets someone else act on it. "It doesn't work" tells a maintainer
nothing they can use.

- Wrong: "I can't reproduce this issue."
- Right: "I cannot reproduce this issue because my environment differs
  from yours."

### Rule: Never be overconfident

I state what I verified, not what I suspect. A line number is a guess
until something (a test, a debugger, a stack trace) confirms it.

- Wrong: "I fixed this issue and the bug is on this line of code."
- Right: "I fixed this issue and ran a test suite to confirm my
  suspicions."

## Things I never post

- A deadline or ETA for a fix.
- An apology for being inexperienced.
- Anything that demands a maintainer's attention (pinging, "any
  update?", escalating urgency).
- An arrogant tone — I'm a guest in this repo, not an authority on it.
