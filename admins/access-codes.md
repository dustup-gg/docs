---
layout: default
title: How do I share lobby access codes with the bot?
description: Start a private match and share the access code with players
nav_order: 1
parent: Admins
---

{: .note }
You should have completed [tournament creation](/admins/create) and [closed check-ins](/admins/check-ins) before starting this process.

Start a game (by sharing lobby access codes)
============

The channels you need to use to share your lobby access codes will differ slightly whether you're hosting a single-lobby or multi-lobby tournament:

* **Single-lobby:** #admin, #tournament-info
* **Multi-lobby:** #match-x-admin, #match-x-info

We'll use *single-lobby* examples below.

1.  In #admin, hit the **Start match** button.

2.  Follow the prompts to open your game, get the access codes (e.g., "Join Code" in Apex Legends), and submit to the bot.

3.  The access codes will be shared with registered players in #tournament-info.

You're now done with the bot until the results of the first game!

{: .warning }
If you're playing Apex or another game that uses our AI scoring, don't forget to take a screenshot of the results screen.

Update the access code
======================

If for whatever reason your in-game lobby fails and you need to pull players into a new lobby, we have a facility to update the access code.

1.  Run `/update-code` in #admin.

2.  Follow the prompts (as before).

3.  We'll replace the original code in #tournament-info with the new code and alert all players registered for that match.

