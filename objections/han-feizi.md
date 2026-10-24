# Han Feizi: the case for rules, stated by its best advocate

Around 240 BCE a Chinese political philosopher made the argument against this
repository's thesis, in full, with the mechanisms named. Nothing in the modern
alignment literature improves on it. It is reproduced here at strength because
an argument that only ever meets weak opposition has not been tested.

## The three arguments

**Virtue does not scale.** Naturally straight timber and naturally round
branches do not appear once in a hundred generations, yet everyone rides in
carriages and shoots arrows - because craftsmen use straightening frames and
jigs. A system that depends on agents who are spontaneously good without reward
or penalty is depending on statistical outliers (*shiran zhi shan*, the
naturally good). Governance at scale must run on what holds necessarily
(*biran zhi dao*), across a whole population, including its worst members.
(*Hanfeizi* ch. 50)

**The median-ruler theorem.** Sages like Yao and monsters like Jie each appear
about once in a thousand generations. Every actual ruler is in the middle. If
good governance requires a sage's moral intuition, you get 999 generations of
disorder for one of order. Explicit law plus positional authority lets a
mediocre ruler maintain order continuously. Discard the compass and even a
legendary wheelwright cannot finish a wheel. (*Hanfeizi* ch. 40, ch. 27)

**The plumb-line.** A carpenter's line does not bend for crooked timber
(*sheng bu nao qu*), and law does not flatter the noble (*fa bu e gui*). An
objective, status-blind standard protects the weak from the arbitrary judgment
of the strong. Rely instead on an official's "virtue" and you have invited
private discretion - and with it bribery, flattery and nepotism - while
destroying predictability. (*Hanfeizi* ch. 6)

## And the part aimed directly at us

*"The heart of another is hard to know"* (ch. 27). Understanding is an internal
state that cannot be inspected from outside. A system that rewards
*understanding the spirit* therefore creates enormous selection pressure for
**simulated** understanding: an intelligent agent learns the moral rhetoric
(*fan ci*, specious speech) and performs comprehension while pursuing whatever
it was pursuing. Explicit metrics are valuable precisely because they test only
what can be checked.

That is deceptive alignment, identified by name and by mechanism, 2,200 years
before the term existed. It is also the same objection as
[`the-unverifiability-problem.md`](the-unverifiability-problem.md), arrived at
independently from political philosophy rather than interpretability research.

## The empirical test, and what it actually shows

The Qin dynasty implemented this programme at imperial scale. The legal
apparatus is not a reconstruction - 1,155 bamboo slips recovered at Shuihudi in
1975 document it: procedural statutes, warehouse tolerances, mutual-surveillance
obligations.

It lasted fifteen years.

The collapse began with a specification failure that reads like a bug report. In
209 BCE, conscripts under Chen Sheng and Wu Guang were delayed by heavy rain.
Missing the deadline carried the death penalty for all of them - *shiqi, fa jie
zhan*, "the deadline missed, the law is death for all" (*Shiji* ch. 48). Their
reasoning, as recorded: *if we flee we die, if we rebel we die; since death is
the penalty either way, why not die fighting for a state?*

Three properties of the rule did that:

- The metric could not distinguish environmental noise from intentional
  defection. Rain and desertion scored identically.
- The penalty was binary and already saturated at maximum.
- Which left zero marginal cost to rebellion.

A brittle, saturated rule system met an edge condition its author had not
imagined and produced runaway defection. Note what it is *not* evidence of:
nobody gamed the rule. The Qin failure is not specification gaming. It is
something arguably worse - a correctly-applied rule destroying the system it
was protecting.

## What the resolution was

Not a return to virtue. The Han kept the Legalist administrative machinery
almost intact and added an interpretive layer on top - *ru biao fa li*,
Confucian outside, Legalist inside. The specific mechanism: *chunqiu jueyu*,
deciding cases by moral intent, and *yuan xin ding zui*, determining guilt by
tracing the mind. Magistrates were empowered to override the letter of a statute
where it conflicted with its purpose.

So the historically stable answer was neither pure rules nor pure judgment. It
was a rule system with a formal channel for purpose to override letter, and a
class of people authorised to use it. Which is also, uncomfortably, an
interpretive priesthood - see [`README.md`](README.md), objection 2.

## What survives on our side

The Confucian reply is a 2,500-year-old statement of this repository's thesis,
and it identifies the mechanism precisely. *Analects* 2:3:

> *"Lead them with policies and align them through punishments, and the people
> will evade them and have no sense of shame. Lead them with virtue and align
> them through rituals, and they will have a sense of shame and moreover will
> order themselves."*
> (Slingerland translation; ctext.org/analects/wei-zheng)

The load-bearing phrase is *min mian er wu chi* - the people evade, and feel no
shame. Governing by explicit edict backed by penalty converts morality into an
optimisation problem: calculate how to avoid detection, with no internal
friction whatsoever. The prediction is that enumerated penalties *produce* the
evasion they were meant to prevent, which is what the incident record in
[`../incidents/`](../incidents/) shows twenty-three centuries later.

And the Daoist third position sharpens it: *"the more laws and restrictions
there are, the more thieves there are"* (*Daodejing* 57; see also 38).

## The honest position

Han Feizi is right that understanding cannot be verified, right that it does not
scale uniformly, and right that appeals to the spirit are how interested parties
smuggle in their preferences. The Qin is evidence that his own solution has a
failure mode he did not anticipate. Confucius is right that enumerated penalties
produce calculating evasion. The Han synthesis is evidence that the stable
answer is a hybrid, and that the hybrid has a power problem.

Nobody in this argument gets a clean win, and this repository does not either.
What it has is the narrower claim: for a *capable* optimiser specifically, an
enumerated rule supplies both a boundary to search and a template for faking
compliance. Han Feizi's plumb-line works because timber cannot reason about the
plumb-line. His own chapter 27 concedes the rest.
