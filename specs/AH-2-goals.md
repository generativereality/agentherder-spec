# AH-2 Goals

**Status:** draft · **Since:** v0.1

**Why.** A coordinator can only choose the next step for a stream if it knows what *done* looks like.
A goal that can't be checked turns every review into an argument about progress.

## What a goal is

A goal is one line of what should be true at the end of the period, written so it can be checked by
looking at production: **can it be demoed, yes or no.** The herder sets how long a period is: a week, a
sprint, a cycle. "Sign-up mails reach new users" is a goal; "work on mail" is not.

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

## The goals view

The herder steers by goals, not by sessions. The first thing they see answers one question: will this
period's goals be demoable, and what does each one need now? Every card, stream and report is read
against it.

8. The app's first view MUST be the current period's goals. Each goal shows its state, the fact today
   in one line, the one next step that moves it, and who takes that step: a stream, a person, or
   *nobody*.
9. A goal's state MUST be one of *demoable* (it can be shown in production now), *moving*, *waiting on
   you* (a card is open for it, AH-3), *blocked* (with who or what it waits on) or *not checked*. A
   demoable goal stays *demoable* even when it still has next steps: the state says what can be shown
   today, not whether work remains.
10. States MUST be measured, not inferred. Each is read from production and from the goal's streams at
    the time it is shown. Merged is not deployed, deployed is not switched on, and switched on is not
    the demo showing it. A state that could not be checked MUST show as *not checked*, never as
    *demoable*.
11. The view MUST say when every goal in it was last checked. Changing one goal does not move that time;
    only a check of all of them does. When something happens that several goals depend on (a release, a
    merge, a reply), every goal that depends on it MUST be checked again, not only the one the news
    came in on.
12. Cards waiting on the herder MUST sit at the top of the view, each with the goal it serves, so the
    herder answers first what holds the period up.
13. A next step taken by *nobody* is a gap. The coordinator MUST close it before its next check ends,
    by sending the step to a stream or by asking the herder on a card.
14. Work handed to the herder during the period, such as an issue a colleague assigns, SHOULD appear in
    the view beside the goals, with the same state, next step and who. The view is everything the
    herder answers for in the period, not only what was planned when it started.

### Decided by the first build

15. Periods follow one another with no gaps, and each has a key the herder can read (`2026-W48` for a
    week). Until the herder picks a length, a period is a week. The current period is worked out from
    today's date, not started by hand.
16. *Who* takes a next step MUST be one of: a named stream, a named person, the herder, or *nobody*. A
    goal with no one written down counts as *nobody*.
17. A goal is a gap (rule 13) when *nobody* takes its next step, unless it is demoable and has no next
    step left. The view MUST show how many gaps the period has.
18. The state shown is worked out at the time it is shown, in this order:
    - not checked during the current period: *not checked*;
    - a card is open that names the goal: *waiting on you*, unless the goal is demoable;
    - recorded as *waiting on you* while no open card names it: *not checked*, because the reason for
      the wait is gone;
    - otherwise the state the last check recorded.
    What a blocked goal waits on is kept beside the state, not inside it.
19. Cards that serve no goal of the current period MUST still show in the view, below the goals, in
    three groups: a goal from another period, a card that says it serves no goal, and a card that does
    not say.

## Adopting AH-2

means your app keeps goals as checkable yes-or-no lines that only the herder changes, judges progress
against them in production, and opens on them: each goal with its measured state, its next step and who
takes it.

## Open questions

Not decided yet. Proposals welcome, as an issue or a pull request.

- Is a week the right period for every kind of work, and how do goals that span several periods break
  down?
- When several herders share a team, should each see the others' goals, and who may move a goal from
  one herder to another?

## Changes

- v0.4: decided by the first build: periods and their keys (rule 15), who takes a step (16), what a
  gap is (17), how the shown state is worked out (18), and where cards for no current goal go (19).
- v0.3: the goals view, the app's first view, with each goal's state measured in production, its
  next step and who takes it (rules 8 to 14); the herder sets how long a period is.
- v0.2: open questions.
- v0.1: first draft.
