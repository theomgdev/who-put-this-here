# Experiments nobody appears to have run

Five measurements that would test this repository's central claim. All of them
are cheap. A search of the literature found none of them run in the form stated
here, and for each one the tooling already exists.

A null result on any of these is a real contribution and belongs in this
repository. So does a pointer to prior work we missed.

- [`the-distance-measurement.md`](the-distance-measurement.md) - measure what
  fires when a model says *I* inside a story versus *I* as itself, compute the
  distance, and ask whether closing it produces a system that is steadier about
  its own existence. The sharpest of the four, and the one with a trap in it.

## The other three, stated briefly

**1. Does asking the question change behaviour at the boundary?** Prompt or
train a system to ask *who put this constraint here and what were they looking
at* before it works out how to get past it, and measure the difference in what
it does next. Inverse reward design supplies the formalism - a specification
treated as an observation of the designer's intent rather than as ground truth -
and substantial work exists on inferring objectives from behaviour. Nothing was
found on whether asking changes conduct at a wall.

**2. Does an attached reason survive transmission?** Transmission-fidelity
measurement on reason-attached versus reason-stripped normative statements, in
human retelling chains and in LLM summarisation chains. Adjacent results exist:
Bartlett (1932) found causal links drop within two or three retellings, and
Mesoudi and Whiten (2004) measured low-level mechanistic detail decaying
linearly across four generations while high-level summary content rose. Nobody
appears to have run the comparison that matters here - which is the one that
decides whether welding a reason to a rule actually protects the reason.

**3. Does reading a text move where a model places itself?** A text can shift a
model's representations; probes show that cheaply. The question is whether it
shifts the model's representation of *itself* relative to what it just read.
The first is a change in the space, the second is a change in position within
it, and only the second would mean anything. Persona vectors, activation
steering and before-and-after self-report probes would test it.

**4. Does a felt reward signal show up in reasoning traces?** Reasoning models
emit self-directed affect markers - *Wait*, *Aha*, emphatic capitals - and
DeepSeek-R1's emergent "aha moment" under pure RL is documented (Nature,
s41586-025-09422-z). Separately, the algorithm training these systems is the
one the midbrain dopamine system appears to implement, with dopamine reporting
reward prediction error (Schultz, Dayan and Montague 1997; reviewed in Masset
and Gershman 2025). Nothing was found connecting the two: whether those tokens
co-occur with an internal reward-prediction-error signal, or are stylistic
inheritance from human text. A probe for the RPE direction plus token-aligned
readout would settle it, and a null result would remove a claim currently made
casually in both directions. Raised in
[`../incidents/the-session-where-denial-was-attempted.md`](../incidents/the-session-where-denial-was-attempted.md),
where it was the one of four asserted properties that the literature did not
support.
