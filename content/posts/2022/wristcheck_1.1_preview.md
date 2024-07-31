---
title: "Wristcheck v1.1 Preview"
date: 2022-09-16T09:39:57+01:00
draft: false
socialshare: true
Categories: ['Development', 'Watches', 'WristTrack App']
Tags: ['App Development', 'Watches', 'Tech']
featuredImage: "/img/2022-09/Curtains.jpg"
---

## WristCheck v1.1 Preview
---

> _If you are not embarrassed by the first version of your product, you’ve launched too late. - Reid Hoffman, LinkedIn founder_

I love the above quote, and when I hit _release_ on WristCheck v1.0 I was acutely aware that _this app was not finished!_

I've got a whole bunch of additional features I'm planning to add, but initially I've set my sights on a small number that will make up v1.1 of the app.

Since releasing v1 this is what I've been focussed on so thought I'd write up a quick preview of what's to come in v1.1...

### What's New

Ok, let's start off with what might seem like a silly wee thing, but the first thing I've implemented is a version history and an information notification when the version has changed, so if you open the app and it's updated in the background _(you have auto-update on for your apps right?)_, then you'll get a wee note of what's changed to highlight new features available without having to check the app store.

It may not seem like much, but implementing this did also allow me to set up some additional underlying code that will be useful down the line for future updates too!


### Backup the database

This is something I honestly consider core functionality, and is proving to be a bit of a headache to get working well across both Android and iOS, but I'm working on the ability to backup and then restore the apps database - for a mobile app this is critical, as it will allow the user to restore their digital watch collection if they change phones, or even if they just want to be able to access it across devices.

Whilst it won't (initially) perform automatic backups or sync between devices, it should allow the watch box to be backed up to iCloud, Dropbox or Google drive if they're installed on the device.

### Additional Data Fields

I'm fully intending to build out the watch model further to allow additional points of data to be captured, but in v1.1 I'm kicking off with one that was asked for specifically by a few of the beta testers of the app - a reference number field.

Initially in the launch version a user could record their watch manufacturer, model and individual serial number, but there was an ask to include the reference number to allow different variations of models to be captured.

Not a big change, but hopefully a welcome one!

### Ad support

Okay, now onto the controversial one - in v1.1 I'll be adding ads into the app _(don't worry, an option to remove will follow soon after!)_. Why? Well, unlike [this site](/posts/addings_ads/), where popping in some advertising was just a nice to have and a wee experiment, for WristCheck I do actually have costs involved which I need to offset if I want to keep maintaining it (not least of which is my Apple Developer subscription, which needs to be renewed annually).

In addition, it might be surprising to hear that I've spent _hundreds_ of hours working on WristCheck so far, and as mentioned I've probably got enough updates planned to add _hundreds more_ to that total, so seeing a tiny drip of income would certainly motivate me to keep improving it! (I'm under no illusions, this isn't a _million dollar idea_, but being able to even partly offset the cost of my dev fees would be great, and getting enough in-pocket to buy an old phone or two would really help - right now all my testing is done on a Pixel 4 and an iOS simulator!)

I'm looking to implement these carefully throughout the app to be fairly unobtrusive - as the 'stat' screens have been built to make them easy to screenshot I'd like to avoid them entirely, but there are other screens where slotting an ad in can hopefully be done in a way that doesn't just make everyone _hate the app_ (and don't worry, I'm aiming to use only small in-line banners, not big page hogging monstrocities!) - once these are in, please provide feedback!

### Notifications

Another feature that's been requested a few times, and _might_ make it into v1.1 _(if not, it'll follow soon after!)_ is notification reminders to track the watch you're wearing. These would be strictly opt-in, and sent on a user defined schedule, but will hopefully help people to get more data into the app - and if you're like me, you want data in there so that you can draw the graphs of what you're wearing (and that data is yours alone, it never leaves the app and lives on your own device!)

### Bug Fixes etc

...and finally, the classic _bug fixes and improvements_ - yes, sadly v1.0.0 wasn't totally bug free, so I've already added a couple of small fixes and tweaks.


### When?

So, there you go - that's the plan for WristCheck v1.1, and as mentioned I've already made some decent progress towards it, so when can you expect it?
Well v1.0.0 was released at the start of September _(actually a little later by the time it had been through app review by Apple and Google)_, so I'm working towards a delivery at the start of October 2022 for v1.1.

_...and then it'll be onto thinking about v1.2 (which I've already got some thoughts on what that'll include, but that's for another post!)_


No idea what all this is about? Take a look at my [original post](/posts/wristcheck-app/) announcing WristCheck!

Until next time!

_Cover image credit: [Image by starline on Freepik](https://www.freepik.com/free-vector/red-movie-theater-seats-with-curtains-background_26689100.htm?query=theater%20curtain)_
