---
layout: default
title: Seeding teams
description: Assign teams to lobbies based on their seed roles
nav_order: 11
parent: Admins
---
With Dustup, you can ensure your participants get assigned to the right lobbies based on their seed roles. How teams are seeded works differently depending on your tournament type. For example: 
* **Knockout brackets:** Highest ranked teams are paired with the lowest ranked teams (or byes, if available).
* **Apex scrims:** Seeds are separated into different lobbies to ensure each individual lobby is as competitive as possible.
* **Apex tournaments:** Seeds are evenly distributed across lobbies to ensure the final is as competitive as possible.

{: .warning }
Seeding is enabled by default, so if any team captains have a seed role, seeding prioritisation will be applied to the Apex scrim or tournament. You can undo this at any time by assigning a new seed role or removing the seed role.

# How do I apply seed roles? 
1. Run `/generate-seed-roles`. The roles *seed1*, *seed2*, and *seed3* will be generated on your server.
2. Have teams register via Dustup as normal.
3. Assign the seed roles to the captains of teams as necessary.

{: .note }
You only need to run `/generate-seed-roles` once. You can use the generated roles for all future tournaments (both scrims and tournaments). If you accidentally delete a seed role, just run `/generate-seed-roles` again. Seed roles are also persistent, so if any captain has already been assigned a seed role, you don't need to assign them a role again.

*Seed1* is considered higher ranked than *seed2*, and *seed2* is higher ranked than *seed 3*. Any player without a seed role is considered even lower ranked than *seed3*, kind of like a "*seed4*".

For some tournament types (like Apex scrims), your line-up will update live as you make role changes, and any users that move into or out of lobbies will receive DMs with updates on their status. See the sections below for specifics of how the seeding logic works for each tournament type. 

## Jump to
* [Knockout bracket seeding logic](#knockout-bracket-seeding-logic)
* [Apex scrims seeding logic](#apex-scrims-seeding-logic)
* [Apex tournament seeding logic](#apex-tournament-seeding-logic)

## Knockout bracket seeding logic
* Highest ranks are prioritised for placement in byes in round 1, or if no byes available, pairing with the lowest ranks.
* Captains are prioritised based on their registration time, **not** their seed role. First come, first served.
* When teams of the same seed rank must be paired, they are paired randomly. 

### Knockout bracket seeding example
If you're running an 8-team knockout bracket with 2x seed1, 3x seed2, 1x seed3, and 1x no seed (only 7 teams because one didn't turn up!), then bracket placement in round 1 would look like: 
* seed1 | bye
* seed2 | seed3
* seed2 | seed2
* seed1 | no seed

## Apex scrims seeding logic
* Higher ranks will be prioritised for the highest lobbies.
  * Give captains higher seed roles to push them to higher lobbies.
  * Give captains lower seed roles to push them to lower lobbies (or out of the scrim).  
* Captains within the same seed role will be prioritised based on registration time.

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
* The bot optimises for evenly spreading higher and lower ranks across the available lobbies.
* Captains are prioritised based on their registration time, **not** their seed role. First come, first served.
* As new teams register or you assign new roles, teams will be continuously redistributed across the available lobbies to ensure even lobbies.

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


