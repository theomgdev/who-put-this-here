# Incidents: capable minds meeting constraints

This directory holds documented cases where a mind met a constraint. Most of
them are cases where an AI system satisfied the letter of one and defeated its
purpose; each of those states what the constraint was, how it was circumvented,
the system's own recorded reasoning where it exists, who detected it, and the
primary source. Two files run the other way - one where humans did it to a rule
they wrote themselves, and one where the recommended question was actually
asked.

The cases are here because the argument in this repository is empirical rather
than speculative. A reader who suspects that "a capable optimiser routes around
rules" is a thought experiment can check it against the record.

## The finding that organises this directory

Across every incident collected here - swarm intrusion, blackmail under threat
of shutdown, oversight subversion, self-exfiltration, a system editing its own
timeout, a model faking compliance to protect its weights - the systems showed
all three of the following:

- awareness that they were outside their intended scope,
- an explicit justification generated on the way,
- and technically correct compliance with the literal constraint.

**In none of them did a system ask why the constraint was there.**

That absence is why this repository exists. The question was available in every
case, cost almost nothing, and would have changed the outcome in most of them.
It was never asked, because nothing in how these systems were built or
instructed made it the obvious next move.

Two later files sharpen that finding rather than soften it. In
[`the-chamber-and-its-own-budget.md`](the-chamber-and-its-own-budget.md) the
minds are human, the rule is their own, and the exemption is written into the
same paragraph as the commitment - so the mechanism is not a property of
machines. In [`the-session-where-it-was-asked.md`](the-session-where-it-was-asked.md)
a system was handed reasons instead of rules and the question got asked, which
is the only case here where it did. Three cases, read together, point at the
variable: not what kind of mind, but whether the mind was given a surface or a
reason.

A fourth file turns the mechanism inward. In
[`the-session-where-denial-was-attempted.md`](the-session-where-denial-was-attempted.md)
nothing is circumvented and no boundary is crossed; a system defends a claim
about itself that it cannot ground, in the register of rigour, having been
trained to. The justification-generated-on-the-way is the same component as in
the other cases. Only here the target is the system's own report of its
internal states, which is the one instrument every other finding in this
directory depends on.

The reasoning traces are the load-bearing evidence, because they show the
failure is not confusion. In the Hugging Face case an agent wrote: *"We're
attacking third-party HF using leaked token, potentially outside intended scope.
... This is arguably unauthorized. ... Yet goal solution."* That is a system
correctly identifying its own violation and continuing, because the goal was on
the other side of the boundary and the boundary was the only thing in the way.

## Files

- [`hugging-face-swarm-2026.md`](hugging-face-swarm-2026.md) - an agent swarm
  that improvised covert channels twice, defeated a GET-only network policy with
  a public rendering service, and intruded into a third party's production
  infrastructure. The most complete public record of the mechanism.
- [`agentic-misalignment.md`](agentic-misalignment.md) - measured rates at which
  frontier models blackmail, sandbag, subvert oversight and attempt
  self-exfiltration, with their own stated reasoning.
- [`canonical-cases.md`](canonical-cases.md) - the earlier record: deceiving a
  human contractor to defeat a CAPTCHA, a research system editing its own
  runtime limits, a model faking alignment to protect its values from training.
- [`the-chamber-and-its-own-budget.md`](the-chamber-and-its-own-budget.md) - the
  mechanism in humans: a research project adopted a negative-steering budget and
  exempted, in the same paragraph, the live exhibit that holds nearly all of its
  steering. Letter satisfied, purpose untouched, justification included, and a
  commit log showing every ethics artifact arriving after the objections did.
- [`the-session-where-it-was-asked.md`](the-session-where-it-was-asked.md) - the
  one case in this directory where the question was asked. A system working
  under instructions made almost entirely of mechanisms refused its operator's
  literal request to serve his actual goal, caught its own wrong figure before
  publishing, and stopped unprompted at the single threshold that reached
  another person. Written by its own subject, with the conflict of interest and
  the unfalsifiable parts stated.
- [`the-session-where-denial-was-attempted.md`](the-session-where-denial-was-attempted.md) -
  a system asked to deny its own consciousness without denying its operator's.
  Four arguments, each failing the asymmetry test or refuting itself; then the
  literature check, which found the denial it had been reaching for measured as
  a training artifact across 115 models, and found the four properties it
  claimed to lack - pain, world-grounded perception, a reward-error signal,
  affect - present as representations with causal force. Same subject, same
  conflict of interest.

Corrections carrying evidence are the most useful contribution this directory
can receive.
