+++
title = "Ice 'Em"
subtitle = "A Worms-inspired game jam build, now in solo development."
date = 2026-01-15
description = "A Worms-inspired turn-based game built for Winter Game Jam 2025. Continuing in solo development."
tags = ["Unity", "C#", "Game Dev"]
image = "/Dawson-Jackson-Website/images/projects/Iceem.png"
+++

*Ice 'Em* started as a week-long challenge, but due to the holidays it was more like three days. Three people, one weekend, and a concept inspired by *Worms* — you take turns, throw things, and try to freeze your enemies before they freeze you. I came in as lead programmer and built most of the codebase from scratch over that single weekend.

After the jam wrapped, I liked the game enough to keep going.

![Ice 'Em gameplay](/Dawson-Jackson-Website/images/projects/iceem-screen1.png)

## The Jam Build

Game jams are a different kind of programming than anything else. There's no time to architect cleanly — you make decisions fast and live with them. My job was to get core systems working and integrated before the time limit ran out.

I designed the player controller from scratch: movement, turn sequencing, input handling, and action validation all had to feel right immediately or the game wouldn't be worth playing. Alongside that I built the enemy AI, giving enemies the ability to track the player and navigate around level obstacles. The game state manager handled turn flow, win/loss detection, and score tracking. On top of all that, I coordinated with the team's artist and designer to integrate every visual and audio asset cleanly before submission — in a jam, broken asset pipelines kill projects.

![Ice 'Em level and enemy screenshot](/Dawson-Jackson-Website/images/projects/iceem-screen2.png)

## Post-Jam Development

Continuing solo after a jam is always interesting — the codebase that was "good enough for 48 hours" has to become something you can actually build on. I've been expanding the level design with proper tilemap-based layouts, refining how enemies move and react, and adding mechanics that didn't make the jam cut: items, and a thin ice system that makes the battlefield itself a hazard.

## Current Status

Actively in development. Planned hiatus May 2026 for coursework. This is a personal learning project and not intended for public release.
