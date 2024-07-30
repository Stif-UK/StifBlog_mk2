---
title: "New App: MP Checklist"
date: 2023-02-27T13:48:44Z
draft: false
socialshare: true
Categories: ['Development', 'Video Games', 'MP Checklist App']
Tags: ['App Development', 'Video Games', 'Tech', 'Release Notes']
featuredImage: "/img/2023-02/MPchecklist_header.png"
---

## A helper app for Metroid Prime...
---
Ok, so I realise this post quickly became an essay - if you want to read some background please read on, but if you just want to know about the app, please feel free to [skip to the end.]()

### Returning to Tallon VI

From 2002 until early 2017 if anyone asked me what my favourite game of all time was (and I know that's a school playground question...) without hesitation I'd have answered _Metroid Prime_.


<sub>(If you're wondering, past 2017 a certain elfish gent waking up from a 100 year slumber gave this a nudge into second place...)</sub>

Back in the early 2000's I was in my early 20s and going through a bit of a _gaming phase_, and owned all of that current generation of consoles and handhelds, as well as a rather fine retro collection, but of them all my absolute favourite was my GameCube because it was just full of _Nintendo Magic!_

When Metroid Prime came out I was incredibly disappointed when it was announced that the UK (and other PAL regions) would have to wait at least six months to get our hands on it - _this was long before the days of simultaneous global releases_ - so I did what any self respecting Games Nerd did back in those days...

I bought an import US GameCube and ordered myself an NTSC copy of the game (and from that moment on 90% of my Nintendo games made their way to me early, usually from Canada...)

Prime was a revelation, taking the 2D games _explore-'em-up_ backtracking adventure style and making it 3D, the game was full of little touches that really made you feel like you _were_ Samus Aran, from the effects of rain on her visor to the wonderful reflection of her eyes when you set of an explosion too close.
To me though, what really elevated it to another level was the passive way the story was told, everything you learn about what's going on in the world is through scanning the environment and reading the associated log book entries - to me this was just wonderful and whilst arguably Metroid Prime 2 improves on the gameplay aspects I have to say it took a step backwards for me in this regard (but I really should try to replay that soon too...).

Anyway, with the _(sooooo long awaited)_ release of **Metroid Prime: Remastered** I was desperate to make my way back to Tallon VI and not only replay the game, but do what every Metroid Nerd wants to do and gain a 100% completion of it!

### Hold on lad's, I've got an idea...

Now what I really didn't want to do was to follow a guide - why ruin my trip to this wonderful, immersive world by jumping back and forth through a list of where to go next... no, what I wanted was just a simple checklist of all of the items available to collect, so that I could tick them off as I went...

A quick google turned up [this excellent post](https://www.reddit.com/r/Metroid/comments/59uafk/couldnt_find_anything_like_it_so_i_made_my_own/) on the r/Metroid subReddit by _u/PityUpvote_ where they mention a printable list to tick off as you go.... fantastic, this is _exactly what I want!_


Except... I don't have a printer! Now, here's where we head into 'solution looking for a problem' territory, but if you've read anything else on this site you'll know I like to mess around with code, and this seemed like a fun wee problem to solve...

### A little weekend hackathon

So, I set myself a wee challenge - could I throw together an app to encapsulate this checklist in a weekend?

As such, like [WristCheck](/posts/wristcheck-app/) before it, MP Checklist is built using Flutter and uses a fast end efficient Hive database to store data and state.

Every item in the game is tracked as an Object in the database, which then makes it nice and easy to manipulate them in different ways, as well as track different statuses (e.g. collected / not collected).

I was able to throw the app together over two days, and then spent probably twice as long doing a few tweaks to add some QoL features (that became apparent when I started to use it) as well as wrestling to get it onto the app stores (Google weren't keen on the Trademarked name 'Metroid' being anywhere...so the app description doesn't really tell you what the app is for, and on iOS I faced some hurdles getting the privacy declaration and app permissions setup correctly - useful experience for next time though!)

### What is MP Checklist and what does it do

If you've skipped all of the above (and who can blame you) here's a wee idea of what MP Checklist actually is.

In essence it's a big list of all of the items that can be collected within the game Metroid Prime, which can be ticked off as you go. You can see a summary of either the completion per game region, or by item type.

![MP Checklist home screen image](/img/2023-02/MPChecklist_homescreens.png)
<sub>_Also, light or dark theme!_</sub>

Clicking on either an item type or region then gives you a list of associated items, which can either be ticket off straight from the list...

![Item List](/img/2023-02/item_list.png)
<sub>_Here's a regional view!_</sub>

or you can click in to add notes against the item, perhaps with information of how you _think_ it might be unlocked for collection.

![Item Notes](/img/2023-02/item_notes.png)
<sub>_Here's one I made earlier!_</sub>

Every item contains both the _Region_ it is found in (the five distinct areas of the game) and also the _Room_ - if you pause Metroid Prime you'll see each 'room' on the map has a title.
In v1.2 of the app (the current version in the stores) I also implemented a search feature where you can search by room name, so if playing the game when you find an item you can quickly pull up the map in game, search in the app for the items associated with that room, and then either mark as collected, or make notes quickly.

In later Metroid games (such as the Excellent _Metroid Dread_ and _Metroid Prime 3: Corruption_) the developers implemented great features such as map indicators where you had seen, but not yet collected, an item, which really improves the 100% item chase experience, but that's definitely a gap I found going back to the original _Prime_ that hopefully this app fills.

This app might be a solution looking for a problem, but I've enjoyed using it during my playthrough of the Remaster so far, and hopeful it'll help me hit that magical _100% items completion!_


### Where can I find this wonderful app?

The Android app is currently approved and available on [Google Play](https://play.google.com/store/apps/details?id=com.stifdev.mpchecklist) just now.

A build has been submitted to Apple and is currently working it's way through the review process - I'll update this post with a link once that's complete.

Got any comments or feedback? I still can't figure out why comments on the blog died, so please feel free to either leave an app review or drop a note via the developer contact options on the stores!
