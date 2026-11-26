# AH-7 Standing approvals

**Status:** draft · **Since:** v0.1

**Why.** Asking about everything floods the herder; asking about nothing lets a session merge, send or
spend what the herder never saw. Standing approvals are how the herder decides once, narrowly, so the
same question is not asked fifty times.

## The default

Anything that leaves the herder's own machine or cannot easily be undone needs a yes on a card
(AH-3): merging to the main branch, deploying to production, sending a message, publishing, deleting
what cannot be restored, and spending money.

## Rules

1. A standing approval MUST name one kind of action and its scope, for example *"merge dependency
   updates that pass the tests, in this repo"*. "Do what you think is best" is not a standing approval.
2. Every standing approval MUST be written down with when it was given and the herder's own words.
3. The herder MUST be able to see every standing approval in one place and withdraw or narrow any of
   them; the change takes effect at once.
4. Actions taken under a standing approval MUST be logged, and SHOULD be listed to the herder at the
   next review.
5. Some actions are never standing: spending money, contacting someone for the first time, and
   anything done in the herder's name to people who have not heard from them before. Each needs its
   own yes.
6. When unsure whether an action falls inside a standing approval, a session MUST ask.
7. When a session is refused a step it needs, by the app, the system or another tool, it MUST turn
   that into a card asking for that one step by name, with what it is for. A card MUST NOT ask the
   herder to run a command, handle a key or password, or carry out the step themselves. Signing in and
   paying stay the herder's, and the card says so in plain words.

## Adopting AH-7

means your app asks before anything leaves the machine or can't be undone, unless the herder wrote a
narrow standing approval for it, and shows the herder every such approval and what was done under it.

## Open questions

Not decided yet. Proposals welcome, as an issue or a pull request.

- How far should one approval reach: one session, one stream, every session in the herd?
- What may a session do in a service the herder is signed in to, and how does the herder see what it did
  there?

## Changes

- v0.2: a refused step becomes a card asking for that step, never a command for the herder to run (rule
  7); open questions.
- v0.1: first draft.
