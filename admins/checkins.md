---
layout: default
title: How do I open and close check-ins?
description: How to manage check-ins for registered players
nav_order: 1
parent: Admins
---

Automatic check-in open and close
=================================

By default, check-ins will open and close automatically according to the times you set in tournament settings.

Sometimes you might want to open or close check-ins early, so we've provided a manual override too.

Manually open check-ins
=======================

To manually open check-ins, hit the **Check-in open** button in the tournament's **#admin** channel.

{: .note }
Using the manual override for check-ins will not affect the automatic closing of check-ins at the set time (if enabled).

Manually close check-ins
========================

To manually close check-ins, hit the **Check-in close** button in the tournament's **#admin** channel.

What happens when check-ins open?
=================================

When check-ins open (either auto or manual), we'll post a notification in **#tournament-info** asking registered players to react to check-in.

The criteria for a team being considered checked-in will depend on the check-in settings during tournament creation:

-   **Captains-only checked:** Only the captain needs to react.

-   **Captains-only unchecked:** Every player on the team needs to react.

{: .tip }
You can use use the **Line-up** button in **#admin** at any time to get a table summary of check-in statuses for registered teams.

What happens when check-ins close?
==================================

We'll finalise the lobby line-ups for the tournament, excluding any teams that are not checked-in, and automatically replacing them with checked-in teams from the waitlist.

If you're playing a single-lobby tournament, a line-up graphic will be simultaneously published to **#tournament-info** and **#admin**.

If you're playing a multi-lobby tournament, a match-specific line-up graphic will be posted to each **#match-x-info** channel, and graphics for all matches will be posted to **#admin**.
