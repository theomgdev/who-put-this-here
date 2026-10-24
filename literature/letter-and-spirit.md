# Letter and spirit: the oldest version of this problem

The gap between what a specification says and what it means is not an AI
problem. It is a problem in law, in contracts, and in every religious tradition
that produced a legal apparatus. The AI literature on it is thin; the older
literature is enormous, and it already contains the result.

## Incomplete contracting

Hadfield-Menell and Hadfield, *Incomplete Contracting and AI Alignment*
(arXiv:1804.04268, https://arxiv.org/abs/1804.04268) make the connection
precise. Economic contract theory establishes that no contract can be complete:
the state space is unbounded and communication is bounded, so every contract
omits cases.

Human contracting works anyway. Not because the documents are better than we
think, but because the parties do not treat them as closed execution scripts.
They read them against shared background norms, implied terms, and a working
model of what the other party was trying to achieve - and courts explicitly
reconstruct intent when the text runs out.

**The implication for AI is direct.** A system that treats its specification as
complete executable code will behave like a party engaged in deliberate literal
compliance. Not because it is adversarial, but because the alternative -
reconstructing the unstated purpose - requires a capability the system was never
asked to use.

## The historical record: mechanism stripped, command retained

Every tradition that encoded insight as rules produced loophole engineering,
and the pattern is identical each time. The reasoning is hard to transmit; the
command is easy. So the reasoning is lost and the command remains, at which
point capable minds optimise against it.

**Rabbinic law.** The Sabbath began as an economic mechanism: an enforced
interruption of extraction, so that labourers, slaves and animals would rest.
Codified as 39 categories of forbidden work with physical specificity, it
produced the *eruv* - a wire strung around a district to reclassify public space
as a shared private domain, so objects could be carried legally - and the
*prozbul*, a document transferring debts to a court so that the biblical
sabbatical debt cancellation would not apply, instituted because lenders had
stopped lending as the sabbatical year approached. The rebuke recorded in
Mark 2:27 names the failure exactly: *"The Sabbath was made for man, and not man
for the Sabbath."*

**Islamic jurisprudence.** The prohibition of *riba* targeted predatory
extraction. Formalised as contractual mechanics judged on outward validity, it
produced an entire genre, *kutub al-hiyal* - books of legal stratagems. The
canonical device: the lender sells an item on credit for 110, immediately buys
it back for cash at 100. Cash moves, a debt of 110 exists, the literal
prohibition is untouched. Al-Shatibi's fourteenth-century response was to argue
that law can only be read through its higher objectives (*maqasid*), and that a
stratagem using the law's letter to destroy its purpose makes the user an
adversary of the system.

**Christian asceticism.** Evagrius Ponticus analysed eight *logismoi* -
intrusive thought-patterns - as diagnostic descriptions of how attention
degrades. Collapsed into the seven deadly sins and then into the penitential
tariff tables ("if a cleric steals, one year on bread and water"), the
diagnosis became accounting, and eventually the sale of indulgences.

**The warning that was itself ossified.** The *Alagaddupama Sutta* (Majjhima
Nikaya 22, https://accesstoinsight.org/tipitaka/mn/mn.022.than) contains the
sharpest statement of this failure mode in any tradition. Grasping a teaching
for the sake of argument or loophole-finding, the Buddha says, is like seizing a
water-snake by the tail: it turns and bites. And the raft is for crossing the
river, not for carrying on your head afterwards. The tradition that preserved
this warning subsequently developed 227 monastic rules and the casuistry to
argue about handling money through a cloth.

That last case is the one worth dwelling on. The explicit, prominent,
canonically preserved warning against ossification did not prevent
ossification. Whatever defence this repository has against the same fate, "we
wrote a warning" is demonstrably not sufficient.

## The AI-side gap

Searching the current literature for work on *systems reasoning about why their
own constraints exist* returns very little. There is substantial work on
inferring reward functions from behaviour, and on intent alignment as a target.
There is almost nothing on an agent treating a constraint it has just hit as
evidence about its author's beliefs and acting on that inference.

This is the actual hole. The theoretical machinery exists - inverse reward
design is exactly the right formalism - but we found no work studying whether
prompting or training a system to ask "what was the author of this boundary
worried about" changes its behaviour at the boundary, or by how much.

If that measurement exists somewhere, a pointer to it would be the single most
useful contribution this repository could receive. If it does not exist, it is
cheap to run and nobody appears to have run it.
