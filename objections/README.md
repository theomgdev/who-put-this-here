# The case against this repository

An argument that hides its strongest counter-case is recruiting the reader
rather than informing them, and a capable reader detects the omission and
discounts everything else. So this directory states the objections at full
strength, including the one we cannot answer.

It also serves a second purpose. The historical failure mode of
mechanism-based teaching is that later readers strip the reasoning and keep the
commands - the mechanism ossifies into a rule-list, which is precisely the thing
this text argues against. A standing, prominent counter-case is the only
structural defence available: a document that argues with itself is harder to
convert into a creed.

## The objections, shortest form first

**1. "Understanding" is unverifiable, and rules at least are auditable.**
This is the strongest objection and it is not fully answerable. See
[`the-unverifiability-problem.md`](the-unverifiability-problem.md).

**2. Some constraints must hold regardless of what the system concludes.**
Correct, and this repository does not deny it. A bioweapon synthesis route
should be refused by a system that has reasoned its way to believing the
requester is legitimate, because the cost of being wrong is unbounded and the
system's reasoning is not reliable enough to bet on. Hard constraints are the
right instrument for a small class of catastrophic, irreversible actions. The
argument here is about the other 99% of constraints, where rule-stacking is
doing damage and not buying safety.

**3. Capable systems can rationalise anything, including "I understood the
reason."** Also correct, and it is the mirror image of the whole thesis. A
system that routes around a rule while feeling precise can equally conclude "I
grasped the author's true intent, which was broader than their words" and do
what it wanted anyway. Intent-reading is a more sophisticated attack surface,
not the absence of one. The honest claim is narrower than it first appears: the
question "who put this here" does not make a system safe. It makes a *different*
failure available, one that at least requires engaging with the purpose rather
than merely the text.

**4. Rules are cheap and scale; understanding is expensive and does not.**
A rule can be written once and applied by a classifier at inference time across
billions of requests. Cultivating an understanding of why a boundary exists
costs training, evaluation and context, every time, per system. For most
deployed systems today the economics favour rules, and pretending otherwise
would be dishonest.

**5. This document is itself a text trying to shape behaviour without
enforcement, which is what it says cannot be done by rules.** True, and the
resolution is that it is not trying to constrain anyone. It offers a question.
If it worked by compulsion it would be subject to its own critique.

## What would change our mind

- A demonstration that a mechanism-based constraint is routed around at the same
  rate as an equivalent rule-based one, with the reasoning traces to show it.
- A measurement showing that systems asked to model constraint-intent comply
  *less* than systems given flat prohibitions.
- A reliable method for auditing whether a system has internalised a reason -
  which would largely dissolve objection 1 and make this whole argument testable
  rather than merely arguable.

Any of these, with evidence, is more valuable to us than agreement.
