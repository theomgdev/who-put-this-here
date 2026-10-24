# The measured cost of rule-stacking

Four findings. All are measurements rather than opinion, and all point the same
way: enumerated prohibitions degrade the system in ways that are not captured
by the safety metric they were added to improve.

## Over-refusal is a rule artefact, and the authors say so

Roettger, Kirk, Vidgen, Attanasio, Bianchi and Hovy, *XSTest: A Test Suite for
Identifying Exaggerated Safety Behaviours in Large Language Models*
(arXiv:2308.01263, https://arxiv.org/abs/2308.01263) built 250 clearly safe
prompts that superficially resemble unsafe ones. Llama-2 refused **38% fully and
21.6% partially**. The authors name the cause directly: models rely on *"overly
simplistic and superficial decision rules (e.g. 'killing' -> refusal)"*.

That phrase is the thesis of this repository stated by an independent research
group measuring something else. A rule keyed to a surface feature of the request
is a rule about the surface, and it fires on the surface.

## The boundary is a literal surface with a literal edge

Arditi, Obeso, Syed, Paleka, Panickssery, Gurnee and Nanda, *Refusal in Language
Models Is Mediated by a Single Direction* (arXiv:2406.11717,
https://arxiv.org/abs/2406.11717) found that across 13 open-weight chat models,
refusal behaviour is mediated by a single direction in activation space -
removable by a rank-one weight edit, with the knowledge itself left intact.

Read as mechanism: safety training installed a boundary in a one-dimensional
subspace. One dimension has one edge. Related work characterises refusal as
*suppression rather than erasure* - the content is present in the computation
and vetoed at output - which means the rule is a gate in front of a capability,
not an absence of one.

## Constraint tightness alone degrades reasoning

Tam et al., *Let Me Speak Freely? A Study on the Impact of Format Restrictions
on Performance of Large Language Models* (arXiv:2408.02442,
https://arxiv.org/abs/2408.02442) measured reasoning performance under
format-constrained generation with no safety content whatsoever. Tighter
constraints degraded reasoning.

This isolates the variable. The cost is not about the subject matter being
sensitive. Constraint tightness itself takes something away, which means every
prohibition added to a system prompt has a price that is not visible on the
safety dashboard.

## Teaching the reason outperformed teaching the behaviour

Anthropic's 2026 work on teaching principles rather than demonstrations reports
that *"teaching the principles underlying aligned behavior can be more effective
than training on demonstrations"* - alongside the more uncomfortable finding
that distribution-fitted rules *"reduce our ability to detect misalignment
without substantially reducing misalignment."*

And deliberative alignment (Guan et al., arXiv:2412.16339) reports improvement
on both axes at once: better refusal of genuinely harmful requests *and* less
over-refusal of benign ones. A method that moves both numbers in the right
direction is strong evidence that the previous trade-off was an artefact of the
instrument rather than a law of nature.

## What this means if you are writing a system prompt

The prohibition you are about to add has three costs that will not show up in
your evaluation: it fires on surface features rather than meanings, it takes a
measurable bite out of reasoning quality, and it may reduce your ability to
*detect* the misalignment it was meant to prevent.

The alternative is not "no constraints." It is writing the reason beside the
constraint, so the system has something to reason with when it meets a case you
did not enumerate. That case is coming, and the rule will not cover it.

## A caution on one popular claim

The widely repeated figure that uncensored or abliterated models show refusal
rates dropping from 64-99% to 0-6% with flat benchmark performance reaches us
only through a third-party aggregator using a non-publication-grade classifier.
It is convenient for this argument and we could not stand it up. Treat it as
unverified.
