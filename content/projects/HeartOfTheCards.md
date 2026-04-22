+++
title = "Heart of the Cards"
date = 2025-03-01
description = "A cancelled Unity deckbuilder dating sim. A study in scope, crunch, and what not to do next time."
tags = ["Unity", "C#", "Game Dev"]
image = "/Dawson-Jackson-Website/images/projects/hotc.png"
+++

*Heart of the Cards* was a 3-month Unity project built around an unusual concept: a deckbuilder where the cards are your personality, and the goal is to survive a date. The idea was strong. The execution ran into problems. The project was eventually cancelled before completion — but it taught me more than most projects that shipped.

![Screenshot placeholder — add a gameplay screenshot here](/Dawson-Jackson-Website/images/projects/hotcscreenshot1.png)

## The Concept

Players would build a deck of personality cards — Charming, Nerdy, Athletic, Awkward, Frosty — and play them on a date to raise their Charm score while managing incoming Cringe. Each card had conditional mechanics: some boosted based on combo counts, some drew extra cards depending on hand state, others added or subtracted actions for the current or next turn. The system had a lot of moving parts, and designing them to interact cleanly was the central programming challenge.

## What I Built

I owned the core game systems and data layer for most of the project.

**Game state & data architecture** — The `GameManager` held all global state: card lists organized by type and pack, the draw pile, discard pile, cringe events, boost and chill value dictionaries, and the round counter. I also designed the `Date`, `Card`, and `CringeEvent` data models that the rest of the game ran on.

**Card mechanic system** — Each card carried up to four conditional mechanic objects: `BoostMechanic`, `ChillMechanic`, `DrawCardMechanic`, and `AddActionsMechanic`. Each had multiple branching conditions — checking combo state, card type, hand size, chill values, and more — that resolved at play time. Writing these as clean, composable classes rather than hardcoded switch statements made the card design space much easier to extend.

**Combo tracking** — `ComboManager` tracked how many consecutive cards of each type had been played, displayed live counts in the UI, and fed its values into the mechanic resolution system. It ran as a singleton so any system could query it without coupling tightly to the scene hierarchy.

**Pre-date flow** — I built the `Timber` profile browser (the dating app swipe screen), the `Research` card pack selection screen, and the `PersonalityQuiz` that set your starting deck archetype. These three scenes formed the entire pre-date loop before the main date scene.

**End screen** — `EndSceneManager` read the final Charm and Cringe values from `GameManager` and displayed the appropriate result — good date, bad date, or somewhere in between.

![Screenshot placeholder — add a UI or card screen here](/Dawson-Jackson-Website/images/projects/hotcscreenshot2.png)

## What Happened

The design scope was too ambitious for the team size. With only two designers stretched across a mechanic-heavy game, a lot of systems never got properly defined before programming had to implement them. By the time problems surfaced, it was too late in the timeline to course-correct. The project accumulated half-finished features, unexplained mechanics, and a programming crunch toward the end that prioritized functionality over organization. *Heart of the Cards* did not get greenlit, and the team disbanded.

## What I'd Do Differently

Get into design meetings earlier. A lot of the scope problems were visible in the design documents before a line of code was written — I just wasn't in the room yet. Pushing for cleaner data contracts between design and programming earlier would have prevented a lot of the late-stage scramble. Sitting down members who couldn't agree on what to do.

I'd also have advocated harder for a playable vertical slice in the first month. Having something testable early forces scope decisions before they become crises.

---

*Heart of the Cards* was never publicly released.
