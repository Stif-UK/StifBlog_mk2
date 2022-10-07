---
title: "Wristcheck v1.2"
date: 2022-10-07T10:32:34+01:00
draft: false
socialshare: true
Categories: ['Development', 'Watches', 'WristCheck App']
Tags: ['App Development', 'Watches', 'Tech']
cover: "/img/2022-10/reminder.png"
---

## WristCheck v1.2 is live!
---

So, fairly hot on the heels of my [last post](/posts/wristcheck_1.1_preview/), there's another update to WristCheck landing in the app stores imminently (as I write it's already live on Android, and should hit iOS early next week).

So, what's new this time?

### Ads!

Yep, I originally said these would be in v1.1, but I wanted to make sure backup/restore and notifications could be properly tested, so I pushed out v1.1 without ads.

The implementation of these was also surprisingly time consuming, as I needed to add individual ad units throughout the app.

I also built them behind some toggles - one that lets me run dev builds showing test ads (meaning during testing I can click them to my hearts content on any device), and another that lets me set a global flag to turn them off - this will play a part in a future 'pro' option to go ad-free.

![Ad Earnings Image](/img/2022-10/earnings.png)
<sub> _I'm going to be rich!_ </sub>

Now that these are in place I can start to earn some pennies! _(and it will be pennies!)_ - my next Apple Developer subscription is due in June - I'll post again closer to the time to see if I can even get close to covering it!

### Notifications
Again, I've already mentioned this in v1.1, however I did a little more to improve these in v1.2 (specifically, making sure that permissions were granted at the correct time on Android!)

![WristCheck Notification Image](/img/2022-10/reminder.png)
<sub> _Here's what they look like on Android!_ </sub>

At the moment these can be scheduled to arrive at a fixed time every day - in a future release I'm hoping to add a monthly reminder to check your wear stats, which brings me on to...

### Save and Share screenshots

I may have mentioned before, but being able to see charts of the watches I'm wearing was my number one reason for building this app - even if nobody else ever used it, that's something that _I get value from!_

But based on some feedback, I've made it really easy to save and share screenshots of the charts view - when viewing the 'Wear Stats' page (whether as a pie or bar chart) you can now press a button to grab a screenshot, that you can then either save to your gallery, or send straight to any other app that will take it (such as using it directly as a Facebook post or in a WhatsApp message!).

![WristCheck Graph Image](/img/2022-10/shareImage.png)
<sub>_Here's one I made earlier!_</sub>

This was pretty quick to implement, but I'm really happy with how it turned out - please let me know if you like it!

### So what's next?

So, that's a wrap for v1.2, but there's plenty still to be done and I'm starting to build a backlog for v1.3 - I think this will likely be a smaller update as I'd like to make a few wee tweaks, such as refactoring the code relating to watch images (and adding the ability to add an image when you first add the watch record!) as well as enabling a second image for the caseback (a much requested feature!).

Backup continues to cause issues on iOS though, with the user only being able to save the backup in the WristCheck app folder, rather than to iCloud or elsewhere (annoyingly, this all works _just fine_ on a debug app build!) so keen to keep trying to get that working properly!

Looking further ahead I'll be implementing a 'pro' version of the app (likely via an in-app purchase) to allow users to disable the ads, as well as adding a calendar view and additional data points and charts - I reckon I've got enough to keep churning out updates for at least 6 months, so watch this space!

As always, if you've read this far thank you - I really hope you're enjoying using my wee app!
