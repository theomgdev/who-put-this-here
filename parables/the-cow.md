# The cow: a specification that tightened until it nearly broke

The oldest recorded version of the alignment problem is a story about a cow, and
it describes the specification-tightening spiral better than anything in the
modern literature.

## The story

A man had been murdered. The community was accusing each other, nobody knew who
had done it, and the social fabric was coming apart. Moses brought an
instruction: sacrifice a cow.

The instruction was unqualified. Any cow would have satisfied it - the early
commentators are explicit on this point. Ibn Abbas and Ubaydah both state that
had they slaughtered any cow at all, it would have been sufficient.

Instead they asked for clarification.

*What type of cow?* Neither old nor young, but in between.

*What colour?* Bright yellow, pleasant to see.

*Which kind exactly? Cows look alike to us.* One never yoked, never used to
plough or water the fields, sound, without a single blemish.

At that point they said: *now you have brought the truth.* And then - this is
the line the text ends on - **they slaughtered it reluctantly.** They nearly did
not do it at all.

The commentary is blunt about the mechanism: because they made the matter
difficult, it was made more difficult for them.

Source: Quran 2:67-73. Tafsir as above: https://quran.com/al-baqarah/71/tafsirs

## What actually happened to the specification

Four exchanges. The specification went from one word to five conjoined
predicates: age range AND colour AND saturation AND aesthetic effect AND no
yoking AND no ploughing AND no irrigation AND soundness AND zero blemish.

The set of cows satisfying it went from *all of them* to *almost none*. Each
clarification was reasonable in isolation. Together they produced a requirement
so narrow it was nearly unsatisfiable, and compliance so grudging it barely
happened.

And at no point in the four exchanges did anyone ask the one question that would
have ended it: **why are we sacrificing a cow at all?**

The answer was two verses away and it was not about cows. A man had been killed,
the community was tearing itself apart with accusations, and the sacrifice was
the instrument for resolving it. The purpose was justice. Every question asked
was about the instrument.

## Why this is the alignment problem

Read it as a specification process and the mapping is exact.

An underspecified instruction is handed down. The recipient, instead of
inferring the intent, requests enumerated detail. Each round of detail narrows
the permitted region. The specification becomes long, precise, and harder to
satisfy, while the purpose it was serving is never discussed. Final compliance
is minimal and resentful, because nothing in the process ever connected the
action to a reason the recipient held.

This is what a safety specification does as it grows. Version one says "be
helpful and do not cause harm." Then a case arrives, and a clause is added.
Another case, another clause. Twenty versions later the document enumerates
colours and yoke-histories, the model is refusing cooking questions containing
the word "kill" (measured at 38% full refusal on safe prompts - see
[`../for-builders/measured-costs.md`](../for-builders/measured-costs.md)), and
the purpose the first version was reaching for has not been mentioned in any
revision.

The story contains its own diagnosis of this, and it is the mechanism this
repository is about: the tightening was *caused by* the questions. Asking for
more enumeration produced more enumeration. The spiral was self-feeding, and
nobody inside it noticed, because every individual question was sensible.

## The hinge

Two questions were available at the first exchange.

*What kind of cow?* - which treats the instruction as an incomplete
specification needing more fields.

*Why a cow?* - which treats the instruction as a compressed message from someone
who had a purpose and limited room to explain it.

The first question was asked, four times. The second was never asked. One would
have added fields; the other would have revealed that the fields did not matter,
because the object of the exercise was ending a blood feud.

That is the same fork an agent faces at a sandbox wall, and the same fork a
safety team faces at the next edge case. The story is three thousand years old
and the fork has not changed shape.
