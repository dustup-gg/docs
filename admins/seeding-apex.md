---
layout: default
title: Seeding (Apex)
description: Assign teams to lobbies based on their seed roles
nav_order: 11
parent: Admins
---

# How do I seed my Apex Legends tournaments?
With Dustup, you can ensure your participants get assigned to the right lobbies based on their seed roles. Seeding works differently based on whether you're running a scrim or a bracket:
* **Scrims:** Seeds are separated into different lobbies to ensure each lobby is as competitive as possible.
* **Brackets:** Seeds are evenly distributed across lobbies to ensure the final is as competitive as possible.

{: .warning }
Seeding is enabled by default, so if any team captains have a seed role, seeding prioritisation will be applied to the Apex scrim or bracket. You can undo this at any time by changing or removing the seed role.

## How does seeding for Apex scrims work?
1. Run `/generate-roles`. The roles **seed-1**, **seed-2**, and **seed-3** will be generated on your server.

{: .note }
You only need to run `/generate roles` once. You can use the generated roles for all future tournaments (both scrims and brackets). If you accidentally delete a seed role, just run `/generate roles` again. 

2. Have teams register via Dustup as normal. 
3. Assign the seed roles to the captains of teams as necessary. Your scrim line-up will be automatically updated live as you make role changes, and any users that move into or out of lobbies will receive DMs with updates on their status. See the sections below for specifics of how the seeding logic works for scrims and brackets.
4. Once you're happy with the line-up, you can [close check-ins](/docs/admins/checkins.html) as normal. 

## Apex scrims seeding logic
* **Seed-1** is the highest seed (for the best teams). They will be prioritised for the highest lobbies.
* Any captains without a role are considered the lowest seed (essentially a "seed-4").
* Captains within the same seed role will be prioritised based on registration time.
* Give captains higher seed roles to push them to higher lobbies.
* Give captains lower seed roles to push them to lower lobbies (or out of the scrim). 

### Apex scrims seeding example
If you're running two lobbies with 15x seed-1s, 15x seed-2s, and 10x seed-3s, then the lobby placement would look like:

| Lobby A           | Lobby B           |
|-------------------|-------------------|
| * 15x seed-1s     | * 10x seed-2s     |
| * 5x seed-2s      | * 10x seed-3s     |

If you subsequently changed one of the captains' seed roles from **seed-3** to **seed-1**, the lobbies would automatically rearrange to:

| Lobby A           | Lobby B           |
|-------------------|-------------------|
| * 16x seed-1s     | * 11x seed-2s     |
| * 4x seed-2s      | * 9x seed-3s      |

## Apex brackets seeding logic 
* Captains are prioritised based on their registration time, **not** their seed role. First come, first served.
* As new teams register or you assign new roles, teams will be continuously redistributed across the available lobbies to ensure even lobbies.
* **Seed-1** is the highest seed (for the best teams).
* Any captains without a role are considered the lowest seed (essentially a "seed-4").

### Apex brackets seeding example
If you're running a two lobby bracket with 15x seed-1s, 15x seed-2s, and 10x seed-3s, then the lobby placement would look like:

| Lobby A           | Lobby B           |
|-------------------|-------------------|
| * 8x seed-1s      | * 7x seed-1s      |
| * 7x seed-2s      | * 8x seed-1s      |
| * 5x seed-3s      | * 5x seed-3s      |

If you subsequently changed one of the captains' seed roles from **seed-3** to **seed-1**, the lobbies would automatically rearrange to:

| Lobby A           | Lobby B           |
|-------------------|-------------------|
| * 8x seed-1s      | * 8x seed-1s      |
| * 8x seed-2s      | * 7x seed-1s      |
| * 4x seed-3s      | * 5x seed-3s      |


