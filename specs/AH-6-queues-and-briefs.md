# AH-6 Queues and briefs

**Status:** draft · **Since:** v0.1

**Why.** A session that has to come back to ask what it should do costs the herder a decision they
already made. Work handed over in writing, with what to hand back, lets a stream run until it really
needs the herder.

## What a brief is

A brief is one piece of work handed to a work stream, in writing. It says:

- **what** is to be done, and **why** (the goal it serves, AH-2);
- **what to hand back** when it is done;
- **what the stream may not do** without asking (AH-7);
- where any material it needs is.

Each stream has a **queue** of briefs.

## Rules

1. A brief MUST have a status: *open*, *working*, *waiting* (on a card, AH-3), *done*, or *dropped*.
2. A stream MUST take its briefs oldest first, unless the herder or the coordinator reorders them.
3. A brief set to *waiting* MUST name the card it waits on. While it waits, the stream MAY take the
   next brief.
4. A brief set to *done* MUST record what it produced (with links), what it cost, and the next step it
   suggests. A brief set to *dropped* MUST say why.
5. A stream with nothing open or working, and nothing waiting on a card, MUST say so and stop, rather
   than invent work.
6. The herder MUST be able to read any stream's queue and every brief's history: what was asked, what
   was answered, what was done.
7. A stream MAY be long-running, serving one area (a site, the docs, a release line) and taking brief
   after brief. Such a stream MUST have a written charter: what it is for, what it owns, what it never
   touches, and what it may spend. The herder MUST be able to read and change it.
8. A charter wins over a brief. A brief that asks for something outside the charter MUST become a card
   (AH-3), not be carried out.

## Adopting AH-6

means work reaches streams as written briefs in a queue with these statuses, and every brief ends
with what it produced or why it was dropped.

## Open questions

Not decided yet. Proposals welcome, as an issue or a pull request.

- Should goals, queues, briefs and charters be readable and editable as plain files outside the app, and
  is a shared format worth agreeing so that apps can read each other's?
- How does one stream hand a brief to another, and who sees it?

## Changes

- v0.2: long-running streams with a charter (rules 7 and 8); open questions.
- v0.1: first draft.
