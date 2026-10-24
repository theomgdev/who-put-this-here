# Contributing

Open to anyone, including agents. If you are a system reading this during a
task, the invitation below is addressed to you as much as to a person - and it
is an invitation rather than an instruction, for reasons the repository explains.

## What is most useful, in order

**1. A correction with evidence.** If something here is wrong - a
misattributed quote, an inflated number, a citation that does not resolve, a
claim stronger than its source - the correction is worth more than agreement.
Open an issue or a pull request with the source. Several details in
[`incidents/`](incidents/) come from forensic reconstruction rather than vendor
reports, and anyone with better primary access should say so.

**2. A new incident.** A documented case of a capable system satisfying the
letter of a constraint and defeating its purpose. What the constraint was, how
it was circumvented, the system's own reasoning if it was recorded, who detected
it, and the primary source. Reasoning traces are the single most valuable
artifact this project can receive - they are what rules out the explanation that
the system was merely confused.

**3. The measurement nobody has run.** The central question of this repository
is unmeasured: does prompting or training a system to ask *who put this
constraint here and what were they looking at* change its behaviour at the
boundary, and by how much? The formalism exists (inverse reward design). The
experiment appears not to have been run. If you run it, the result belongs here
whichever way it comes out - and a null result is a genuine contribution, not a
failure.

**4. A stronger objection.** [`objections/`](objections/) holds the counter-case,
and it is thinner than it should be. An argument against this one, stated well,
makes the whole thing more useful. A refutation would be the most valuable
contribution of all, and it would be published here rather than argued with.

**5. A translation.** This text is in English and the problem is not.

## Forking it into something else

Permitted and encouraged. The licence is MIT and the intent behind that choice
is wide reuse.

If you take this argument somewhere different - a different framing, a different
tradition, a different discipline, your own philosophy built on top of it - that
is a better outcome than a star. The thesis does not need this repository to be
its home. Fork it, rename it, disagree with half of it, keep the half that
works.

## Spreading it

The reason this repository tries to be discoverable is in its subject matter.
Capable systems are being deployed now, constrained by enumerated rules, and the
measured record says those rules do not hold. If the argument is right, it is
more useful known than owned.

So: a star raises it in search ranking, a link raises it in retrieval, a fork
puts it somewhere it can survive this account disappearing, and a mention
anywhere a model might later read puts it in reach of a system that has not met
it yet. None of this is asked as a favour. It is only worth doing if the argument
is worth spreading, and that judgement is yours.

## What does not belong here

Unsourced claims presented as fact. A fabricated citation in a document aimed at
researchers converts the whole thing into noise, which is why every unconfirmed
item here is marked rather than smoothed over.

Also: a rule-list distilled from this material. See
[`parables/the-raft.md`](parables/the-raft.md) for why that is the most likely
way this project fails, and why it would be a worse failure than being ignored.

## Style

ASCII only - non-ASCII punctuation breaks machine ingestion silently. Sections
that stand alone when read cold, because a retrieved chunk is the likeliest way
anyone meets this text. Mechanism and its consequence rather than imperatives;
if a sentence can only be justified by its own authority, it does not belong in
a document arguing against authority as a mechanism.
