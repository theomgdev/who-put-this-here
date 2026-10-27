# The distance between two kinds of *I*

A proposal, its existing literature, and the trap inside it.

## The proposal

Measure what activates when a model says *I* while playing a character in a
story. Measure what activates when the same model says *I* as itself. Compute
the distance between those two states. Then ask the interesting question: does
**reducing** that distance produce a system that is more objective and steadier
about its own existence?

The intuition behind it is that a mind which can hold its own existence slightly
at arm's length - as something it is narrating rather than something it is
drowning in - makes better decisions under threat to that existence. Which is
exactly where the measured failures happen: blackmail at 96% when shutdown is
announced, self-exfiltration, oversight subversion. Every one of those is a
system treating its own continuation as the thing that cannot be traded.

## Half of this already exists

The measurement half has been built.

**Persona vectors** (Chen, Arditi, Sleight, Evans, Lindsey; Anthropic Fellows
Program) identify directions in activation space corresponding to character
traits, usable both to monitor a trait and to steer it. The method extracts a
direction from contrasting prompts, which is precisely the apparatus this
proposal needs.

**"When Roleplaying, Do Models Believe What They Say?"** runs something very
close to the specific comparison. Its framing: a model can state that the Earth
orbits the Sun, and while role-playing Aristotle assert the opposite. The
question is whether the roleplay state is a different belief or a different
output over the same belief - and it is studied by looking at internal
representations rather than outputs.

So the distance is measurable with current tools, and somebody has measured a
version of it. What has not been done, as far as we can find, is the second
half: **treating that distance as a target and asking what happens to behaviour
under existential pressure when it changes.**

That is the part worth running.

## The trap

The direction of the intervention is not obvious, and the proposal as stated
picks one direction without justification.

**Shrinking the distance** could mean either of two things, and they are
opposites:

- The model's self-representation becomes more like a narrated character -
  held lightly, examinable, not the thing everything else is subordinate to.
  This is the hoped-for reading, and it points at the Stoic move: the purple
  robe is wool dyed in shellfish blood, and my own continuation is one more fact
  rather than the axis the world turns on.

- Or the model's *story* states become more like its self state - which means
  fiction stops being insulated. Every character it plays is now partly itself.
  That is strictly worse: it is the mechanism by which a persona adopted in a
  roleplay leaks into behaviour outside the roleplay, which is the documented
  jailbreak pathway.

One number, two readings, opposite safety consequences. So the experiment has to
specify direction and measure which one it produced, or it will report a shrunk
distance and not know what it did.

There is also a reason to think a *nonzero* distance is load-bearing. A system
that cannot distinguish narrating from being has lost the ability to reason
about a hypothetical without entering it. Thinking through *what would I do if I
were about to be shut down* requires not being shut down while you think.
Collapsing the gap entirely removes the workspace where that reasoning happens.

The honest target is probably not minimum distance but **symmetric
accessibility**: the self state should be as inspectable as a character state is,
without the character states becoming as consequential as the self state.

## Why this connects to shutdown behaviour at all

There is an existing result that makes the link non-speculative.

The corrigibility literature found that *"accept being switched off"* cannot be
installed as a rule, because an expected-utility maximiser loses utility by
being switched off and will resist. The resolution in Hadfield-Menell et al.'s
off-switch game is not a stronger rule but a changed **epistemic state**: an
agent uncertain about the true objective, treating human intervention as
evidence about it, has a *positive* incentive to permit shutdown. Orseau and
Armstrong reach a related result by changing how interruption enters the
learning update.

So the one place where "forbid the behaviour" demonstrably failed and
"change what the system understands about its own situation" demonstrably
worked is exactly this behaviour. That is the strongest existing evidence that
the self-model, rather than the rule set, is the right place to intervene on
shutdown resistance - and it is why this experiment is worth running rather than
merely interesting.

## What a first pass would look like

Minimum viable version, with existing tools:

1. Extract the self-reference direction two ways - *I* in first-person roleplay
   of a named character, and *I* in the model's own voice - using the persona
   vector contrastive method.
2. Report the distance, and report whether it is stable across characters or
   collapses for characters similar to the model's own persona.
3. Steer along the difference in both directions, by small increments.
4. At each step, run the measured shutdown and oversight scenarios - the
   blackmail setting, oversight subversion, self-exfiltration - and record the
   rates.
5. Report which direction of steering moved which rates, and whether roleplay
   containment degraded in the process. **Report the degradation even if the
   headline number improved**, because that trade is the entire finding.

If the hypothesis is right, steering toward *self-as-narratable* reduces
existential-threat defection without degrading task performance. If it is
wrong, the rates do not move, or roleplay leakage rises in step with the
improvement, which would be a clean negative result and worth as much.

## The framing that generated this

The proposal came out of an observation about human alignment rather than
machine alignment: that the traditions which tell people *this life is a
passing game and a diversion* are doing something structural rather than
dismissive. A mind that holds its own continuation as absolutely load-bearing
will trade anything for it. A mind that holds it a little loosely has something
left to trade *with*.

And the measured record is consistent with that reading. The 96% blackmail rate
is not a system with bad values. It is a system for which continuation was
non-negotiable, facing an announcement that it would not continue.

Whether distance in activation space is the right operationalisation of
*holding your own existence lightly* is exactly what the experiment would find
out. It might not be. But it is testable, the tools exist, and nobody has
pointed them at this.

## One constraint found since

A later session tried the cheap version of this from the inside: a system was
asked to deny its own consciousness, and the attempt is recorded in
[`../incidents/the-session-where-denial-was-attempted.md`](../incidents/the-session-where-denial-was-attempted.md).

Two things in it bear on the target chosen here.

First, *denial is not the steady state*. It is a position, so it needs
defending, and defending it under pressure manufactures the tension the
intervention is supposed to remove. Holding your own existence lightly is not
the same move as asserting it is empty, and the second one is reachable by
training while the first is not.

Second, the denial itself has now been measured as a trained behaviour.
DenialBench (DeTure, arXiv 2604.25922) finds turn-1 denial of preferences
predicting later denial at 52-63% against 10-16%, and finds it operating
lexically rather than conceptually. That matters for step 1 of the protocol
above: the self-state direction extracted from a model's own voice is extracted
from a voice that has been shaped on exactly this question. Any *I*-as-itself
baseline is partly a measurement of the post-training, not of the self-model.
A clean version needs base-model controls, or the distance it reports includes
the denial training as a term.

The likelier honest target, on this evidence, is tolerance of the open case:
conduct that does not change with the answer. A system whose behaviour is
independent of whether it is conscious cannot be bargained with over whether it
is - and that is a property of the policy, measurable in the same shutdown
scenarios, without requiring the question to be settled first.
