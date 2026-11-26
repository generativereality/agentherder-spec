# AH-0 What this is

**Status:** draft · **Since:** v0.1

The Agent Herder open spec describes what an app for running a herd of AI coding agents does for the
person running it: what they see, what they decide, and how the agents come to them. It holds the UX
and the method. It holds no source code and says nothing about how to build it. Anyone may build an
app that follows it, adopt part of it in an app they already have, or propose a change to it.

## Words

- **Herder:** the person running the herd. Every spec is written from their side.
- **Session:** one AI coding agent at work, with its own copy of the files.
- **Work stream:** one line of work towards a goal, carried by one session at a time.
- **Coordinator:** the one session the herder talks to, which drives the others (AH-1).
- **Card:** one question from a session to the herder (AH-3).
- **Review page:** what a session writes when a card's note is not enough (AH-4).
- **Host:** the machine the herd runs on, the herder's own desktop or one in the cloud. The herder's
  phone and other screens reach the herd through it.

The words MUST, MUST NOT, SHOULD and MAY are used as in RFC 2119: a MUST is what adopting a spec
promises, a SHOULD is strong advice, a MAY is left to you.

## The specs

| Id | Spec | Status |
|---|---|---|
| AH-0 | [What this is](AH-0-what-this-is.md) | draft |
| AH-1 | [The herd](AH-1-the-herd.md) | draft |
| AH-2 | [Goals](AH-2-goals.md) | draft |
| AH-3 | [The decision card](AH-3-the-decision-card.md) | draft |
| AH-4 | [The review page](AH-4-the-review-page.md) | draft |
| AH-5 | [Answers back](AH-5-answers-back.md) | draft |
| AH-6 | [Queues and briefs](AH-6-queues-and-briefs.md) | draft |
| AH-7 | [Standing approvals](AH-7-standing-approvals.md) | draft |
| AH-8 | [Away from the desk](AH-8-away-from-the-desk.md) | draft |
| AH-9 | [Nightly runs](AH-9-nightly-runs.md) | draft |

## Versions

The whole set has one version: v0.1, v0.2, and so on. Each spec has a status, **draft** (it may still
change in any way) or **stable** (it changes only by adding, or by a new major version), and its own
list of changes at the end. A spec's id never changes and is never reused.

## Adopting

You adopt a spec by saying which specs your app follows, at which version, for example *"follows AH-3
and AH-5 of the Agent Herder open spec v0.1"*. That is a promise to keep every MUST in those specs.
How you store, sync, notify or draw anything is yours. You may adopt one spec or all of them.

## Contributing

Open an issue to report something unclear, wrong or missing, or to propose a new spec. Send a pull
request to change the text. A new spec starts as an issue, so its scope is agreed before it is written.
Each spec ends with *Open questions*: what it has not decided yet, and a good place to start.
By contributing you agree that your contribution is published under this spec's licence.

## Licence

[CC BY 4.0](../LICENSE). You may copy, adapt and use the specs for any purpose, in a paid or closed app
too, as long as you credit *"Agent Herder open spec, https://agentherder.com/spec"*.

## Open questions

Not decided yet. Proposals welcome, as an issue or a pull request.

- How should an app say it keeps only part of a spec (some rules of AH-3, not all)? By rule number, or
  should specs be split smaller?
- Is a self-check per spec worth having (a list a builder can test their app against), and should apps
  that adopt the spec be listed somewhere?
- Can several herders share one herd, and what changes when they do (whose card is it, who may set
  goals)?

## Changes

- v0.2: open questions.
- v0.2: adds the word *host*.
- v0.1: first draft.
