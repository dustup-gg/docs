---
layout: default
title: How do I create a tournament?
nav_order: 2
parent: Admins
---

{: .note }
You'll need to [complete initial setup](https://help.dustup.gg/en/articles/8565503-how-do-i-set-up-dustup-for-the-first-time) in your server before following the steps below.

If you'd like to use only the scoring automation feature of Dustup, follow the steps for results-only instead.

1.  In the **#dustup-admin** channel, hit the **Create tournament** button.

2.  Enter a tournaments name and submit. This will:

    -   Create a new category for the tournament that contains all the channels you need: **#admin**, **#tournament-info**, **#lobby**, and **#chat**. [Read more about tournament channels](https://help.dustup.gg/en/articles/8565796-what-channels-does-dustup-create-and-what-are-they-for).

    -   Create a new role for the tournament (for registered players).

    -   Message you in the new **#admin** channel with a tournament info embed (this will be blank).

3.  Go to the tournament's **#admin** channel. Below the tournament embed, click **Input details**. This will open the tournament settings in your default browser. If this is the first time you've used the dashboard, you'll also be asked to authenticate through Discord.

4.  Enter your tournament details.

5.  Click **Save**.

6.  Go back to the tournament's **#admin** channel in Discord. You'll see that the details in the tournament embed have now been updated.

7.  Make sure the details are accurate, then click **Publish**. This will:

    -   Create a **#register** channel (visible to everyone on your server).

    -   Publish basic tournament details to **#register** with a registration button.

    -   Publish full tournament details to **#tournament-info** (only visible to registered players).

{: .note }
If you've disabled registrations, you'll need to manually assign the tournament role to all registered players before they can see the competition details in **#tournament-info**.
