# AH-4 The review page

**Status:** draft · **Since:** v0.1

**Why.** A line in a chat is enough for "merge" or "send", and not for a decision that needs context
to make at a high level. The review page is what lets the herder decide such things quickly, on any
screen, without opening the code.

## What a review page is

A page a session writes for one decision. It opens with the decision and the recommendation, then
gives the herder just enough to agree or disagree.

## Rules

1. One page per decision, linked from its card (AH-3). Its address MUST stay the same until the card
   is answered.
2. The page MUST open with what is being decided and the recommended answer, in a few lines.
3. It MUST say what was done, what was checked and how (a test that ran, a screenshot, a link to the
   live thing), and what was *not* done. A claim the session did not check MUST be marked as unchecked.
4. When there are options, each MUST be whole: something the herder can pick as it stands, never parts
   to assemble. The recommended one comes first, then two or three real alternatives.
5. Each option SHOULD say what it costs (money, time, what it rules out).
6. The page MUST read well on a phone: narrow screens, images small enough to load on a mobile
   connection, every link full and tappable.
7. The page MUST NOT need the herder to run anything, sign in to a tool or read code to decide.

## Adopting AH-4

means your app's review pages open on the decision, show what was checked, offer whole options, and
work on a phone.

## Changes

- v0.1: first draft.
