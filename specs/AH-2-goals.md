# AH-2 Goals

**Status:** draft · **Since:** v0.1

**Why.** A coordinator can only choose the next step for a stream if it knows what *done* looks like.
A goal that can't be checked turns every review into an argument about progress.

## What a goal is

A goal is one line of what should be true at the end of the period (usually a week), written so it
can be checked by looking at production: **can it be demoed, yes or no.** "Sign-up mails reach new
users" is a goal; "work on mail" is not.

## Rules

1. Goals MUST live where every session reads them, in plain text, before the period starts.
2. Each goal MUST be checkable as yes or no in production. A goal that can't be MUST be rewritten
   before a stream is started for it.
3. Only the herder sets, changes or drops a goal. A session MAY propose a change, as a card (AH-3).
4. A goal is done only when it can be demoed in production. Merged, built or "ready" is not done.
5. The coordinator MUST compare each stream with its goal at every check, and for each goal not yet
   done, name the next step that gets it closer, and which stream takes it.
6. The context sessions need to work without asking (how the code is laid out, how to test, what not
   to touch) SHOULD sit beside the goals, so a new session starts from it, not from the herder.
7. At the end of the period, the app SHOULD show each goal as done or not, with what is left.

## Adopting AH-2

means your app keeps goals as checkable yes-or-no lines that only the herder changes, and judges
progress against them, in production.

## Open questions

Not decided yet. Proposals welcome, as an issue or a pull request.

- Is a week the right period for every kind of work, and how do goals that span several periods break
  down?

## Changes

- v0.2: open questions.
- v0.1: first draft.
