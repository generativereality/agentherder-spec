# AH-8 Away from the desk

**Status:** draft · **Since:** v0.1

**Why.** The point of a herd is that it keeps moving while the herder is not watching. That only works
if the herder can review and steer from wherever they are, which is usually a phone, in short moments.

## Rules

1. Everything needed to answer a card (the card, its note, its review page) MUST work on a phone.
   Nothing on it may require a desktop, a terminal or a sign-in to another tool.
2. The herder SHOULD be able to answer by voice, and to give a new instruction by voice (rules 7 to 9).
3. Notifications MUST be for cards only: something that needs a decision. Progress, finished work and
   routine reports MUST NOT notify; they are there when the herder looks.
4. The herd keeps running on the host (AH-0) while the herder is away. When the host cannot be
   reached, the app MUST say so plainly, and MUST NOT show stale states as current.
5. An answer given away from the desk MUST be acted on exactly as an answer given at the desk (AH-5).
6. The app SHOULD let the herder see the goals view (AH-2) and the whole herd (AH-1) from the phone,
   not only the open cards.

## Voice

7. Whatever the herder says to the herd, an answer to a card or a new instruction, is recorded on the
   device they speak into (a phone of any kind, a tablet, a watch) and the recording is sent to the
   host. The host turns it into text. The app MUST NOT rely on the device's own speech recognition:
   today, on phones, it is not accurate enough to act on. This rule is about today's phones, and a
   later version may relax it.
8. The recording SHOULD reach no service other than the host, unless the herder chooses one for
   turning speech into text.
9. While the host cannot be reached, the device MUST keep the recording and show it as waiting to be
   turned into text. Nothing is acted on until it has been. A recording MUST NOT be lost because the
   device or the host went offline on the way.

## One herd, many screens

10. The host holds the herd's state. Every screen the herder uses (a phone, a second phone, a tablet,
    the desktop) MUST show the same open cards, and a card answered on one MUST show as answered on all,
    so the same decision is never made twice.
11. The herder SHOULD be able to send the coordinator a new instruction from the phone, typed or
    spoken, not only answer cards.

## Adopting AH-8

means a herder can do all of their deciding from a phone, and is interrupted only when a decision is
needed.

## Open questions

Not decided yet. Proposals welcome, as an issue or a pull request.

- When the host is the herder's own laptop and it sleeps, what should the phone show, and should the
  herd move to a machine in the cloud on its own?
- Which devices' own speech recognition, if any, is good enough to rely on (rule 7), and how would an
  app know?
- Should the herder be able to answer while both the phone and the host are offline, and how is that
  answer carried later?

## Changes

- v0.3: the goals view on the phone too (rule 6).
- v0.2: one state on every screen (rule 10); new instructions from the phone (rule 11); open questions.
- v0.2: spoken input, answers and new instructions alike, is recorded on the device and turned into
  text on the host, not by the phone's own speech recognition (rules 2, 7 to 9); rule 4 names the host.
- v0.1: first draft.
