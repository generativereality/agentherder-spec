# AH-1 The herd

**Status:** draft · **Since:** v0.1

**Why.** Past a handful of sessions, a herder who goes from one session to the next, reading and
nudging each one, becomes the slowest part of the system: the work moves only as fast as they go
round. A herder looks at the whole herd and decides; the moving along is done by something else.

## The parts

- **Work streams.** Each stream has one goal it serves (AH-2), or is marked as upkeep. One session
  carries it at a time, in its own copy of the files, so two streams never edit the same checkout.
- **The coordinator.** One session over all the streams. It checks each stream and whatever else the
  goals depend on (builds, open pull requests, replies), compares where things are against the goals,
  decides each stream's next step, and sends it there. It is the session the herder talks to.
- **Hands-on streams.** A few streams need the herder in front of them: a dev server they are clicking
  through, a browser run they are watching, a problem they are working through in conversation.

## Rules

1. The app MUST show every work stream at a glance with: its goal, its state (*working*, *waiting on
   you*, *done*, *stopped*), the last thing it did, and what it is waiting on, if anything.
2. *Waiting on you* MUST mean a card is open for it (AH-3). A stream that is only quiet is not waiting
   on the herder.
3. The herder MUST be able to mark a stream hands-on. The coordinator MUST NOT send a hands-on stream
   steps of its own; it MAY report on it.
4. The coordinator MUST NOT decide what only the herder may decide (AH-7); it turns those into cards.
5. The herder SHOULD be able to start, stop and hand a stream to a new session without losing its
   history: the brief, what was done, and the answers given (AH-6).
6. A stream whose session stopped without finishing, or will not start, MUST show as *stopped* with
   the reason, never as *working*. The app SHOULD start it again from its history (rule 5). It MUST NOT
   leave starting it to the herder by hand: a stream that cannot be started is a fault the app reports.

## Adopting AH-1

means your app shows the herd as streams with these states, keeps hands-on streams out of the
coordinator's hands, and lets the coordinator ask rather than decide.

## Open questions

Not decided yet. Proposals welcome, as an issue or a pull request.

- When the host sleeps or restarts, should streams that were working pick up on their own, and how many
  failed restarts before the herder is asked?
- How does the coordinator tell a stream that is stuck from one that is slow?

## Changes

- v0.2: a stopped or failed stream shows as stopped, with the reason, and is restarted by the app (rule
  6); open questions.
- v0.1: first draft.
