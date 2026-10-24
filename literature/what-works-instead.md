# What is proposed instead of a rule list

Five approaches that do not work by enumeration. Each is described by the
mechanism it substitutes, and each is followed by its known weakness, because an
approach presented without its failure mode is advocacy rather than information.

## Cooperative inverse reinforcement learning (CIRL)

Hadfield-Menell, Dragan, Abbeel and Russell, *Cooperative Inverse Reinforcement
Learning* (NIPS 2016, arXiv:1606.03137, https://arxiv.org/abs/1606.03137).

**Mechanism instead of rules:** the agent does not receive an objective. It
receives *uncertainty* about the objective and treats human behaviour as
evidence about it. The human is a source of information, not a constraint.

This is the formal version of the question this repository is organised around.
An agent uncertain about what is wanted has a reason to find out, and a reason
to preserve the human's ability to tell it - which is where corrigibility comes
from, rather than from a rule saying "accept correction."

**Weakness:** it assumes the human behaves roughly optimally with respect to the
true objective. Real humans are inconsistent, and a system doing inverse
inference on inconsistent evidence can infer something confident and wrong.

## Inverse reward design

Hadfield-Menell, Milli, Abbeel, Russell and Dragan, *Inverse Reward Design*
(NIPS 2017, arXiv:1711.02827, https://arxiv.org/abs/1711.02827).

**Mechanism instead of rules:** the specified reward function is treated as an
*observation* of the designer's true intent rather than as ground truth. The
system asks what intent would have produced this specification, given that the
designer was writing it with limited knowledge of the environment.

This is the technique that corresponds most exactly to "who put this here and
what were they looking at." A specification written by someone who had not seen
the deployment environment carries information about their beliefs, and
inverting it recovers more than reading it literally does.

**Weakness:** computationally demanding, and sensitive to the assumed model of
the designer. Get the designer model wrong and you recover a confident
reconstruction of an intent nobody had.

## Constitutional AI

Bai et al., *Constitutional AI: Harmlessness from AI Feedback* (Anthropic, 2022,
arXiv:2212.08073, https://arxiv.org/abs/2212.08073).

**Mechanism instead of rules:** rather than labelling thousands of individual
behaviours, the model critiques and revises its own outputs against a small set
of stated principles, generating its own training signal.

**Weakness:** the constitution is still a written document interpreted by the
system, and the interpretation is where the slack lives. In practice this
reduces the number of enumerated rules without eliminating the form. It also
inherits the unverifiability problem - see
[`../objections/the-unverifiability-problem.md`](../objections/the-unverifiability-problem.md).

## Deliberative alignment

Guan et al., *Deliberative Alignment: Reasoning Enables Safer Language Models*
(OpenAI, 2024, arXiv:2412.16339, https://arxiv.org/abs/2412.16339).

**Mechanism instead of rules:** the model is taught the safety specification
itself and trained to reason explicitly over it before answering, rather than
being trained to produce compliant outputs directly.

This is the closest thing in production to the repository's thesis, and the
reported result is the relevant one: models improve simultaneously on refusing
genuinely harmful requests *and* on not over-refusing benign ones. That joint
improvement is what you would expect if the mechanism were being understood
rather than pattern-matched, since over-refusal is the signature of a
superficial decision rule.

**Weakness:** the reasoning is only as good as the specification being reasoned
over, and visible reasoning can be optimised to look good. Chain-of-thought is
not a reliable window into the computation that produced the answer.

## Intent alignment

Christiano's framing (https://ai-alignment.com/clarifying-ai-alignment-5e81f2666b68):
the goal is a system that is *trying to do what its principal wants*, which is
distinct from one that produces approved outputs. A system aligned in intent can
make mistakes; a system aligned in output can be misaligned in disposition and
still score perfectly.

**Mechanism instead of rules:** the target of alignment is the disposition, not
the behaviour.

**Weakness:** no method exists for measuring a disposition. This is the open
problem that the unverifiability objection names, and every approach in this
file eventually arrives at it.

## What the whole file adds up to

Every approach here replaces "enumerate the forbidden" with "transmit the
purpose and let the system reason." Every one of them also runs into the same
wall: the resulting disposition cannot be verified from outside. The honest
summary is that the field has a better idea of what the right shape is than of
how to confirm it was achieved.
