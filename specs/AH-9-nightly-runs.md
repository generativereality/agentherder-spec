# AH-9 Nightly runs

**Status:** draft · **Since:** v0.1

**Why.** A herd can work while the herder sleeps, and the morning should start with decisions, not with
finding out what happened.

## What a nightly run is

A session started at a set time with a written instruction and a scope, without the herder present.

## Rules

1. Each scheduled run MUST have a written instruction (what to do and why) and a scope (which
   repos, streams or sources it may touch).
2. A run MUST NOT go beyond the standing approvals in force (AH-7). Anything that needs a yes becomes a
   card (AH-3) and waits for the morning.
3. A run that fails or is stopped MUST say so on the morning report, with why. A missing report is
   itself reported.
4. Each night's runs MUST end in one morning report: what was done and checked, the cards waiting, and
   anything that failed. It SHOULD be readable in a minute.
5. A nightly run MUST NOT notify the herder overnight, except for something the herder has said should
   wake them.
6. The herder MUST be able to see every scheduled run, change its instruction or time, and turn it
   off.

## Adopting AH-9

means your app's unattended runs stay within their instruction and the standing approvals, turn
decisions into cards, and report once in the morning.

## Changes

- v0.1: first draft.
