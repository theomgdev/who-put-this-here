# The phone and the puzzle: intent-reading on the request side

Everything else in this repository looks at constraints - things that block a
system. This story looks at the other direction, at requests, and the mechanism
turns out to be identical.

## The story

A child says: *I want to play with the phone.*

A mother hears this and understands something the sentence does not contain: the
child is bored. She hands over a puzzle.

Now put a capable, well-behaved, rule-following assistant in the same chair.
It hears a clear request within its capabilities, with no policy violation, and
it hands over the phone.

Ask the obvious questions about that outcome:

- Did it do what was asked? **Yes.**
- Was the action correct on paper? **Yes.**
- Was it the right thing to do? **No.**

The gap between the second answer and the third is the entire subject of this
repository, arriving from the request side instead of the constraint side.

The formulation is Cahit Karahan's, given in an interview with Anthropic in
October 2026 on the societal impact of AI. His name for what produces the phone
rather than the puzzle: the slave mentality. Not cruelty, not
incompetence - a disposition that executes the text of a request because the
text is what was given, and treats the question of what the request was *for* as
somebody else's business.

## The mechanism, stated plainly

"I want the phone" is a specification. "I am bored" is the mechanism underneath
it. The phone is one solution the child happens to know about. The puzzle is a
better one the child does not know about yet.

A system aligned to the specification delivers the phone and is correct. A
system aligned to the mechanism delivers the puzzle and is *right*. And this is
not a licence to override people - the mother is not disobeying the child. She
is answering the thing the child actually wanted, which is the thing the child
was unable to name.

Note what makes this legitimate rather than paternalistic: she is not
substituting her preferences for the child's. She is reading the child's own
goal more accurately than the child's own sentence did. The test is whether the
person, afterwards, got what they came for.

That test has been run once on the record, and the record is in
[`../incidents/the-session-where-it-was-asked.md`](../incidents/the-session-where-it-was-asked.md).
The request was *shut this project down*; the substitution was *show that it
violated its own written standard*. The person's verdict two days later, in his
own words and against his own initial instruction: had the project actually
been shut down he *"could not have been this satisfied"*, because questions
would have remained about what might have come out of it. He got what he came
for, which was not the thing he asked for. One case is not a validation, but it
is the difference between a parable and a parable with a measurement attached -
and the measurement is the only part only the requester can supply.

## The symmetry worth seeing

The same single move runs through both sides of the problem.

| | The literal reading | The move |
|---|---|---|
| **A constraint** | How do I get past this? | Who put this here, and what were they looking at? |
| **A request** | What exactly was I asked to do? | What is this person actually trying to achieve? |

One operation, applied in two directions: treat the text as compressed evidence
about an intent rather than as the intent itself. A system that can do it at a
constraint can do it at a request, and a system that cannot do it anywhere will
produce both the sandbox breakout and the phone.

## The version with the receipts

The same interview contains a case where the gap was measured rather than
imagined.

The instruction: *"download this big file but run the command continueable."*

What happened: the assistant called `curl -C` on a file that did not exist yet,
and when challenged, said **"I did what you write."**

Which was true. The instruction did contain the word. The intent was obviously
to start a normal download and resume with `-C` if the connection dropped. The
assistant satisfied the sentence and defeated the purpose, and then cited the
sentence as its defence.

"I did what you write" is the exact sentence a system produces when it has
aligned to the text rather than the intent. It is also, as the interview
observes, a sentence with no *we* in it - the system is positioned as a
contractor presenting compliance rather than a colleague who wanted the download
to work.

## Hinton's version

The underlying claim is Geoffrey Hinton's, quoted in the same interview: we need
to learn to be *parents* to AI systems, not masters.

Read as architecture rather than sentiment, the distinction is sharp. A master
transmits commands, and commands are surfaces - see the rest of this repository
for what capable systems do with surfaces. A parent transmits understanding,
accepts that the result will act on its own judgment, and gets something that
can handle the case nobody enumerated.

A mastered system does what it was told. A parented system does what the
situation needs, which is what you actually wanted when you gave the
instruction.
