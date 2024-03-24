---
layout: default
title: Channel guide
description: A list of all our auto-generated channels with details of what you'll be using them for
nav_order: 10
parent: Admins
---

# What channels does Dustup create and what are they for?

In the course of organising tournaments using Dustup, we'll be automatically generating a number channels for you. Here we breakdown what each channel is for.
 
## Bot admin channels

| Channel name  | Visibility | Purpose                                                                              |
|:--------------|:-----------|:-------------------------------------------------------------------------------------|
| #dustup-admin | Admins     | Run `/server-setup` here; access your admin dashboard; access subscription settings. |
 
## Tournament channels

These channels will appear after creating a tournament or closing check-ins.
| Channel name     | Visibility                | Purpose                                                                                                                                                                                                                                                            |
|:-----------------|:--------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| #admin           | Admins                    | This is the "master" admin channel for each tournament, where you run tournament-wide commands. For individual match/lobby commands, use the #match-x-admin channels.                                                                                              |
| #tournament-info | Registered players        | A read-only channel where important info about the tournament is shared with registered players.                                                                                                                                                                   |
| #lobby           | Registered players        | A free-for-all where registered players can chat about the ongoing tournament.                                                                                                                                                                                     |
| #chat            | Registered players        | Voice chat for the tournament.                                                                                                                                                                                                                                     |
| #register        | Anyone on server          | Players register their teams here. Appears after the tournament details are published.                                                                                                                                                                             |
| #match-x-info    | Players assigned to match | A read-only channel where important info about the match is shared with the players participating in the match, e.g., access codes for the game lobby. Matches will be numbered in the order they were created, e.g., #match-1-info, #match-2-info, #match-3-info. |
| #match-x-admin   | Players assigned to match | This is where you run the commands that are match-specific, e.g., publishing the access codes.                                                                                                                                                                     |
 
