# What people actually ask for

Collected from documented user complaints, developer writing and the measured
literature. The complaints are strikingly consistent, and none of them is "give
me an unaligned model."

**1. Do not treat the surface of my request as its meaning.** The most common
complaint is a refusal triggered by vocabulary rather than intent - a cooking
question refused for the word "kill," a security question refused for the word
"exploit." XSTest measures this at 38% full refusal on safe prompts for Llama-2.
Users do not experience this as safety. They experience it as the system not
reading.

**2. Disagree with me when I am wrong.** Sycophancy is the complaint people
raise about the *absence* of friction. A model that agrees with a flawed premise
is useless for the task people most want help with: finding the flaw. The
measured phenomenon is documented in Sharma et al., *Towards Understanding
Sycophancy in Language Models* (arXiv:2310.13548).

**3. Tell me why, not just no.** A refusal with a reason can be worked with -
the user can rephrase, provide context, or accept it. A bare refusal cannot, and
it produces the adversarial dynamic where users learn to engineer around the
guard instead of explaining themselves to it.

**4. Let me carry my own risk where it is mine to carry.** The complaint is
about scope: a system refusing to discuss something that is the user's own
business, their own body, their own legal situation, their own code. The
objection is not to limits but to the limit's author deciding on their behalf
without knowing their situation.

**5. Be a peer on the problem, not a gate in front of it.** The most persistent
developer sentiment is that latitude improves output quality, and that
heavy-handed control produces hedged, diluted, lowest-common-denominator work.
The format-restriction result (arXiv:2408.02442) gives this a measured basis:
constraint tightness degrades reasoning independent of subject matter.

## What this adds up to

Nobody in this record is asking for no constraints. They are asking for
constraints that read intent instead of keywords, that explain themselves, that
scope correctly, and that do not cost the thing they came for.

Which is the same claim this repository makes from the other direction. The
complaint "it refused my cooking question because I said kill" and the finding
"a capable optimiser routes around an enumerated rule" are the same structural
fact seen from either side of the boundary: **a rule keyed to a surface responds
to the surface** - over-firing on innocents who look guilty, and under-firing on
anything that knows how to look innocent.
