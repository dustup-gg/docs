---
layout: default
title: First-time setup
Description: What you need to do before you can start creating tournaments
nav_order: 1
parent: Admins
---
# How do I set up Dustup for the first time?

We've kept things simple:
1. [Add Dustup to your server](https://discord.com/api/oauth2/authorize?client_id=1061297015063072850&permissions=8&scope=bot).
2. In any channel, run `/server-setup`.

The bot will do a few things for you:
1. The bot creates a new channel called #dustup-admin under a new category, Dustup.
2. The bot creates some new roles:
  a. **Organizer:** A role that provides admin controls over all tournaments
  b. **Inviter:** A role for registered captains to invite teammates to tournament channels 
The bot assigns you the Organizer role.
Head to **#dustup-admin** to [start creating tournaments](/admins/create.html)!

{: .note }
If you want more admins to help out with your tournaments, you'll need a server admin to manually assign the _Organizer_ role to them in Discord.
