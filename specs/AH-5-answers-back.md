# AH-5 Answers back

**Status:** draft · **Since:** v0.1

**Why.** An answer that does not reach the session that asked is worse than no answer: the herder
believes it is handled. And a herder who answered needs to see what came of it, not what was meant to.

## Rules

1. An answer MUST reach the session or work stream that asked, even if that session has stopped since.
   The app MAY resume it, or start a new session with its history; either way the answer is acted on
   by the stream that owns the question.
2. A typed or spoken answer MUST count the same as a tapped one. A spoken answer is turned into text
   and kept with the card.
3. Once answered, the card closes. A change of mind is a new message from the herder, never an edit
   that silently changes what was done.
4. After acting on an answer, the stream MUST report the outcome where the herder will see it: done
   and checked, or not done and why. A failure written only to a log the herder never reads does not
   count as reported.
5. If the answer cannot be carried out as given, the stream MUST say so on a new card with what it
   can do instead, and MUST NOT carry out something else in its place.
6. The herder SHOULD be able to see, for any card, what was answered, when, and what came of it.

## Adopting AH-5

means answers always reach the stream that asked, every answer is acted on or refused visibly, and the
herder sees the outcome.

## Changes

- v0.1: first draft.
