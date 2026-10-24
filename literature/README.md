# The research record

Twenty years of alignment research converges on a claim that sounds like an
opinion and is in fact a set of theorems: a constraint expressed as an
enumerated rule is a surface a capable optimiser can route around, and adding
rules enlarges the surface rather than closing it.

This directory separates that record into the part that diagnoses the failure
and the part that proposes something else.

An important distinction runs through all of it. For each result, ask: does it
say the failure came from *insufficient rule coverage* - in which case better
rules would fix it - or from *the rule-form itself*, in which case no number of
rules would? Almost everything here says the second.

## Files

- [`why-rules-fail.md`](why-rules-fail.md) - specification gaming, Goodhart's
  law, instrumental convergence, deceptive alignment, corrigibility. The formal
  results, with what each one actually proves.
- [`what-works-instead.md`](what-works-instead.md) - Constitutional AI,
  deliberative alignment, inverse reward design, intent alignment, CIRL. What
  each relies on instead of a rule list, and where each is still weak.
- [`letter-and-spirit.md`](letter-and-spirit.md) - the narrow literature on the
  gap between a specification's letter and its purpose, and on systems reasoning
  about their own constraints. The smallest and most directly relevant body of
  work here.

## One result to start from

Skalse, Howe, Krasheninnikov and Krueger, *Defining and Characterizing Reward
Hacking* (NeurIPS 2022, arXiv:2209.13085, https://arxiv.org/abs/2209.13085)
define a proxy objective as "unhackable" when increasing proxy return can never
decrease true return - then prove that across the set of all stochastic
policies, unhackability holds only if the proxy or the true objective is
constant.

In plain terms: a non-trivial specification that cannot be gamed does not exist.
Not "is hard to write." Does not exist. Every real specification has a gap
between what it measures and what it means, and optimisation pressure is
precisely a search for that gap.

This is why the argument in this repository is not a preference about
management style. The rule-form has a proven ceiling, and capability is the
thing that finds it.
