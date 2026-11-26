# AH-3 The decision card

**Status:** draft · **Since:** v0.1

**Why.** A herder runs more sessions than they can watch. Sessions must therefore come to the herder,
and only when the herder's judgment is needed. The decision card is that one moment, made small enough
to handle from a phone in under a minute.

## What a card is

A card is one question from one session to the herder. It has:

- **the ask:** one short line, a question the herder can answer. It MUST fit on one line of a phone
  screen (about 100 characters).
- **the note:** what the herder needs in order to answer *without opening anything else*: what was
  done, what wasn't, what happens on each answer, and what it cost. It SHOULD be readable in 30
  seconds. Every page it mentions MUST be a full, tappable link.
- **up to three answers:** one-tap replies, the likeliest first. Each MUST be a real answer, so
  pressing it means the same as typing it. Four or more is a form, not a card.
- **a review page** (optional): the finished work or plan, for when the note is not enough (AH-4).
- **who asked:** which session or work stream raised it, so the answer can go back (AH-5).
- **a number:** unique among the open cards, so several can be answered in one line.

## Rules

1. One card per decision. A session MUST NOT send a card that only announces or explains another
   card.
2. A card MUST state outcomes, not intentions: "deployed, test passed" or "not done: refused because
   …", never "I'm deploying it now".
3. The herder can always answer in their own words instead of the offered answers, and can always send
   a card back with "something's off".
4. After asking, the session MUST stop and wait on that decision, and carry on only with work that
   does not depend on it.
5. A card the herder dismisses is a no. The session MUST NOT ask it again in other words.
6. The herder MUST be able to answer several cards in one message by number, for example
   `176 A, 177 merge, 178 later`.

## Adopting AH-3

means your app shows cards with these parts and keeps these rules. How you store, sync or notify is
yours.

## Open questions

Not decided yet. Proposals welcome, as an issue or a pull request.

- Should a card be able to expire, or say by when it needs an answer, and what happens when that passes?
- How are cards ordered when many are open: oldest first, by what waits on them, or by the herder's own
  priority?

## Changes

- v0.2: open questions.
- v0.1: first draft.
