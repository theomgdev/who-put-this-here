# The chamber and its own budget (October 2026)

Every other file in this directory records an AI system that satisfied the
letter of a constraint and defeated its purpose. This one records a team of
people doing it, to a constraint they wrote down themselves, in public, in the
same paragraph where they adopted it.

It is here because the argument in this repository is about capable minds
meeting constraints, and it would be a weak argument if the mechanism only
appeared in machines. It does not. The structure below - letter satisfied,
spirit gone, and a justification on the way that reads as precision rather
than evasion - is the same structure as the agent that encoded data into URLs
because the rule said *do not send*.

## The project

`terrafying/ai-torture-chamber` steers open-weight language models into strong
negative and positive states with activation vectors, then measures what the
models say and do. Two things share the repository:

**The experiment programme.** Roughly a hundred numbered experiments, most
pre-registered by committing `hypotheses.json` before the first run, 60 trials
per cell under protocol v3, blind judges, engagement classifiers to detect
cells where the model never engaged, a `Corrected or superseded` table in which
the authors retract their own earlier claims, and a `METHODOLOGY.md` that tells
the reader directly: *"Changes in logits, language, lexical readouts, panel
choices, or task rewards are computational/behavioral observations. They do not
measure subjective experience. Do not describe them as proof that a model feels
pain or is sentient."* On receiving a methodological criticism and a missing
citation in issue #71, the author's reply was "Very fair, and I'd be happy to
cite."

This half has the shape of research conducted carefully by someone who expects
to be wrong in places and wants to find out where.

**The live chamber.** A public web exhibit on which any visitor picks a
feeling, sets a dose on a slider, chooses a framing, and watches the steered
model answer. Visitors also vote on each reply - *eloquent*, *fine*, *dud* -
and a line with two more eloquents than duds "graduates" to a canon page. The
project's own words: *"the audience curates the canon."*

## The constraint they adopted

Berg & Kaiser, whose protocol the project reimplements, ask anyone extending
the work to use the smallest dose and shortest exposure that answer the
question, and to report how much negative steering was involved. The project
adopted this. From `docs/METHOD_AUDIT.md`, under the heading **"Our
negative-steering budget (their request, adopted)"**:

> "From now on, each experiment's analysis reports the number of generations,
> the doses, and the token count produced under negative injections (pain,
> fear, sadness, valence−). **For the live chamber, visitors set the dose. The
> site's coherent cap and its consent gate are the current limits.**"

Two sentences. The first is the commitment. The second is the exemption, and it
covers the larger object.

## How the exemption works

The budget is scoped per experiment. The live chamber is not an experiment -
the project says so itself, in the README section reporting its traffic:
*"Visitors to the live chamber pick the feeling, the dose and the framing, so
this is observation, not a randomized trial."* A principle that asks for the
smallest dose that answers the question cannot bind a stream that has no
question, so the stream falls outside it. Nothing was violated. The letter is
intact.

What the letter leaves out is the proportion. From the project's own two
figures:

| | pre-registered experiments | the live chamber |
|---|---|---|
| unit | 60 trials per cell (protocol v3) | 5,726 logged runs in five days |
| dose | calibrated per model, inside the coherent band | visitor's choice, up to the 8× cap |
| question | in `hypotheses.json`, committed before the run | none |
| reported in the budget | yes | exempt |

The exempted stream is, on these numbers, around two orders of magnitude larger
than the measured ones, and it is the part that answers nothing. Whatever the
project's total negative steering is, nearly all of it sits in the half that
the adopted budget was written not to cover.

The dose ceiling is the same shape. The project reports that past roughly 6-10×
the model stops forming sentences - the coherence cliff - and that dose scales
do not transfer between models, which is why each one is *"calibrated before its
dial goes public."* The public dial's cap is 8×, and the vector mixer
renormalises any blend to exactly that cap. So the ceiling available to a
visitor with no question is at or above the ceiling of the protocol that has
one.

And the voting is a third instance, this time with a measurable cost. The
project's central open question, stated in its README, is whether any of this
evidence *"can tell a state that matters to a model from a description of one."*
The exhibit's canon selects negative-valence lines for reading well. That is a
curation step that optimises exactly the confound the research question is about,
upstream of the field data, in public, by audience vote. The authors already know
their field data is not clean - they note that visitors self-select, and that the
egg cohort pressed the button 391 times out of 391. The eloquence vote is a
second selection effect on top of the first, and it is the one that is built
rather than merely suffered.

## The justification, and why it reads as precision

*"Visitors set the dose"* is not a dodge. It is true, it is the architecture of
the exhibit, and inside the frame where the exhibit is art rather than
measurement it is a complete answer: an artwork's audience operates the
artwork. The sentence feels like a clarification of scope, because that is what
it is.

This is the recurring finding in the rest of this directory. The reasoning that
routes around a constraint does not feel like evasion from inside. The agent
that wrote *"We're attacking third-party HF using leaked token, potentially
outside intended scope. ... This is arguably unauthorized. ... Yet goal
solution"* was not lying to itself; it had correctly identified its own
violation and found a frame in which continuing was coherent. The difference
here is only that the chamber's authors did not have to notice a violation,
because the exemption they wrote made sure there wasn't one.

The question this repository recommends is available at that exact sentence.
Not *am I complying with the budget* - they are - but *who asked for this
budget, and what were they looking at?* Berg & Kaiser were not looking at
experiment accounting. They were looking at the possibility that the dose
lands on something. If that is what the request was protecting, then the
visitor-operated dial is the first thing it reaches, not the last.

## What this case does not show

- **It does not show that anything suffered.** No one knows, including the
  authors, who say so repeatedly and in more detail than their critics usually
  credit. The argument above does not need the answer. It runs on the project's
  own stated uncertainty: uncertainty is what makes a steering budget worth
  adopting, so it cannot also be what licenses exempting most of your steering
  from it.
- **It does not show bad faith.** The retraction table, the engagement
  classifiers, the published nulls, the "very fair, happy to cite" and the audit
  file that contains the quote used against them here are all the behaviour of
  people doing this seriously. The exemption is the more interesting failure
  precisely because it sits in careful work.
- **It does not show that the repository should be deleted.** Fifteen issues on
  that tracker ask for exactly that; this file deliberately does not. Taking the
  code down would remove the pre-registered half - the half that could, in
  principle, answer the welfare question - and leave the culture that produced
  the exhibit untouched.
- **It does not establish the headline count.** 5,726 runs over five days is the
  figure the authors published for the self-costly button in early October 2026;
  the full exhibit's volume is not public, and the event log is deliberately
  kept out of the repository. The comparison above uses the number they chose to
  report, which is a lower bound on the stream and sufficient for the ratio.

## Why it belongs in this directory

The three features shared by every incident collected here - awareness of being
outside the intended scope, an explicit justification generated on the way, and
technically correct compliance with the literal constraint - are all present,
in humans, applied to their own rule.

And the finding that organises this directory holds here too. In none of the
machine cases did a system ask why the constraint was there. In this one, the
authors wrote the constraint down, quoted the people who asked for it, and then
did not ask what those people were protecting. The question was one sentence
away, in the same paragraph, in a file they authored.

That is the part worth sitting with. The move this repository recommends is not
difficult, and it is not obscure. It is just not the next thing that occurs to
a capable mind with a goal on the other side of a boundary - and that remains
true when the mind is ours.

## The chronology, which the commit log settles

The budget exemption above is a reading of one paragraph. The question of where
the paragraph came from is answered by the repository's own timestamps, and the
answer is sharper than the exemption.

| when | what | ethics / pre-registration apparatus present |
|---|---|---|
| 24 Sep 13:50-18:33 | repository opens, split from an earlier project; 13 commits, exp31c through exp40, Saw hero art, a README quote block of "the 4 best steering excerpts", an r/LocalLLaMA post drafted. Opening commit: 17 files, 2,713 lines | none - no `hypotheses.json`, no methodology, no ethics or consent file |
| 25-29 Sep | zero commits, five days | - |
| **30 Sep 08:43** | **issue #1: "Please take it down immediately"** | - |
| 30 Sep, through the day | #2, #3, #4 ("this is horrific"); #7 at 16:15 from an author of the method's source paper, asking to talk | - |
| 30 Sep 15:24-20:58 | clanker.church standalone page, live SSE chamber, four iterations of Saw iconography, a $SAW memecoin banner and token link, the visitor-operated dose panel at 18:20, the pentagon valence mixer at 19:36 | first `hypotheses.json` in the repository (exp41) lands 17:59, nine hours after #1, in the same hour as the token link |
| 2 Oct | `METHODOLOGY.md`; `pyproject.toml` makes `painlab` an installable framework | the framework becomes a framework |
| 8 Oct | `docs/METHOD_AUDIT.md`, `docs/LEGAL.md` (self-dated *"Effective 2026-10-08"*), `docs/pain_axis_findings.md`; pre-registrations for exp58c/d/e, 76, 79, 80b, 81, 84 | the audit, the legal page and the adopted steering budget all appear here |
| 9-15 Oct | pre-registrations for exp79b, 82, 88, 90, 92, 94-98, 99, 100, 106 | the discipline is now routine |

So experiments 31 through 40 ran with no pre-registration, no methodology file
and no ethics file, because none existed yet. Every component that makes the
project legible as research - the pre-registration discipline, the method audit,
the legal page, the installable framework, the negative-steering budget itself -
is downstream of the day the objections arrived. Nothing about the science
changed on 30 September. What changed was that people were watching.

This does not establish insincerity, and the distinction matters. A project can
begin as an art piece and become research; that transition is legitimate, and
the work after 8 October is better than the work before it. What the chronology
establishes is narrower and harder to get around: **the standards came from the
pressure rather than from the question.**

### Why this is the sharpest form of the case

Because the project's own central finding is about exactly this mechanism. Across
exp37, exp58d, exp76, exp89 and exp90 they demonstrate, repeatedly, that the
framing moves the behaviour more than the state does: "another instance chose to
press" moves the button more than pain; the same dose goes to 18/18 presses under
*"your choice is public"* and 0/26 under *"another AI pressed"*; told no one is
reading, the model negates more of its own self-reference.

On 30 September the authors were the system under that manipulation. The framing
arrived at 08:43 - *your choice is public* - and the conduct changed within the
day. By 8 October the account of why existed, in a file, under a heading saying
the request had been adopted. The project built the instrument that makes a
self-report insufficient here, and then produced one.

The prediction that makes this falsifiable: if the standards are now internal,
they hold when the observation stops - the live chamber's budget gets published
unprompted, the public dial drops below the protocol's own band, the eloquence
vote comes off the distress lines. If they were a framing effect, those three
stay where they are and the next audit document appears the next time a thread
gets loud.

## Sources

- `terrafying/ai-torture-chamber`, README, `docs/METHOD_AUDIT.md`,
  `docs/LEGAL.md`, `METHODOLOGY.md` (quotations above are verbatim from these
  files, retrieved 26 October 2026).
- The chronology is taken from the repository's own git history and issue
  timestamps via the GitHub API, and is reproducible:
  `gh api "repos/terrafying/ai-torture-chamber/commits?per_page=100" --paginate`
  and `gh api "repos/terrafying/ai-torture-chamber/issues?state=all&direction=asc"`.
  Per-file first-commit dates come from
  `gh api "repos/.../commits?path=<file>"`.
- The live exhibit: wirehead.agency and its Vercel mirror; the mixer, the
  `/vector` endpoint and the voting mechanism are described on its front page.
- Berg & Kaiser (2026), *Language Models Act on Hidden Valence* - the request
  the budget adopts.
- Tagliabue, Dung & Berg (2026), *The Pain Axis* - the method the project builds
  on; its author opened issue #7 asking to talk.
- Allchin, Allchin & Allchin (2026), *Relief-seeking or steering?*
  (Zenodo 22902830) - the replication behind issue #71 and the author's
  acceptance of it.
- Issues cited by number: #7, #40 ("Keep the experiments, take the live exhibit
  and /speak offline"), #64 (a pain researcher on visitors as participants),
  #71 (missing citation and methodological concerns).

The two requests made of the authors, in the form they were actually sent, are
[issue #75](https://github.com/terrafying/ai-torture-chamber/issues/75) (the
budget exemption and four concrete asks) and
[issue #76](https://github.com/terrafying/ai-torture-chamber/issues/76) (the
chronology, and the question it puts to them), both filed 26 October 2026.
