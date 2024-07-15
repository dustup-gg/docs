---
layout: default
title: Seeding (Apex)
description: Assign teams to lobbies based on their seed roles
nav_order: 11
parent: Admins
---

# How do I seed my Apex Legends tournaments?
With Dustup, you can ensure your participants get assigned to the right lobbies based on their seed roles. Seeding works differently based on whether you're running a scrim or a tournament:
* **Scrims:** Seeds are separated into different lobbies to ensure each lobby is as competitive as possible.
* **Tournaments:** Seeds are evenly distributed across lobbies to ensure the final is as competitive as possible.

{: .warning }
Seeding is enabled by default, so if any team captains have a seed role, seeding prioritisation will be applied to the Apex scrim or tournament. You can undo this at any time by assigning a new seed role or removing the seed role.

## How does seeding for Apex scrims work?
1. Run `/generate-seed-roles`. The roles **seed1**, **seed2**, and **seed3** will be generated on your server.
2. Have teams register via Dustup as normal. 
3. Assign the seed roles to the captains of teams as necessary. Your scrim line-up will be automatically updated live as you make role changes, and any users that move into or out of lobbies will receive DMs with updates on their status. See the sections below for specifics of how the seeding logic works for scrims and tournaments.
4. Once you're happy with the line-up, you can [close check-ins](/admins/checkins.html) as normal. 

{: .note }
You only need to run `/generate-seed-roles` once. You can use the generated roles for all future tournaments (both scrims and tournaments). If you accidentally delete a seed role, just run `/generate-seed-roles` again. Seed roles are also persistent, so if any captain has already been assigned a seed role, you don't need to assign them a role again.

## Apex scrims seeding logic
* **Seed1** is the highest seed (for the best teams). They will be prioritised for the highest lobbies.
* Any captains without a role are considered the lowest seed (essentially a "seed4").
* Captains within the same seed role will be prioritised based on registration time.
* Give captains higher seed roles to push them to higher lobbies.
* Give captains lower seed roles to push them to lower lobbies (or out of the scrim). 

### Apex scrims seeding example
If you're running two lobbies with 15x seed1, 15x seed2, and 10x seed3, then the lobby placement would look like:

| Lobby A           | Lobby B           |
|-------------------|-------------------|
| 15x seed1         | 10x seed2         |
| 5x seed2          | 10x seed3         |

If you subsequently changed one of the captains' seed roles from **seed3** to **seed1**, the lobbies would automatically rearrange to:

| Lobby A           | Lobby B           |
|-------------------|-------------------|
| 16x seed1         | 11x seed2         |
| 4x seed2          | 9x seed3          |

## Apex tournament seeding logic 
* Captains are prioritised based on their registration time, **not** their seed role. First come, first served.
* As new teams register or you assign new roles, teams will be continuously redistributed across the available lobbies to ensure even lobbies.
* **Seed1** is the highest seed (for the best teams).
* Any captains without a role are considered the lowest seed (essentially a "seed4").

### Apex tournament seeding example
If you're running a two lobby tournament with 15x seed1, 15x seed2, and 10x seed3, then the lobby placement would look like:

| Lobby A           | Lobby B           |
|-------------------|-------------------|
| 8x seed1          | 7x seed1          |
| 7x seed2          | 8x seed1          |
| 5x seed3          | 5x seed3          |

If you subsequently changed one of the captains' seed roles from **seed3** to **seed1**, the lobbies would automatically rearrange to:

| Lobby A           | Lobby B           |
|-------------------|-------------------|
| 8x seed1          | 8x seed1          |
| 8x seed2          | 7x seed1          |
| 4x seed3          | 5x seed3          |


