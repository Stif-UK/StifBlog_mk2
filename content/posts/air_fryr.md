---
title: "Air Fryr"
date: 2023-04-04T09:41:53+01:00
draft: false
socialshare: true
Categories: ['Development', 'Cooking', 'Air Fryr App']
Tags: ['App Development', 'Cooking', 'Tech', 'Release Notes']
featuredImage: "/img/2023-04/AirFryrHeader.png"
---

## Air Fryr - An Air Fryer Companion app
---
With energy bills going through the roof, the world seems to have gone air fryer mad over the last year or so.

I had an old one that was only ever used for making chips (aka _French fries_ for any readers on the other side of the Atlantic!), but I recently had a bunch of cashback pending from Quidco (if you're in the UK and don't already use Quidco you should [give them a look](https://www.quidco.com/raf/43546/)), so decided to treat myself to an absolute beast of an Air Fryer.

![Quidco Summary](/img/2023-04/QuidcoCashback.png)
<sub>I've been a Quidco member for over 10 years and averaged about £100 a year cashback, just doing normal shopping!</sub>

I'd been squirrelling away my cashback for a while and was thinking of treating myself to a new watch, or possibly a Switch OLED, but neither of those things were things that I really _needed_...and then the Ninja Foodi Air Fryers caught my eye...

Now I do like to cook for the family - pulling a meal together for everyone is a nice way to wind down at the end of a busy day, and being able to do this is one of my favourite things about working from home, however I do often find myself working fairly late, so being able to cook _quickly_ is a bonus for me.

With the crazy rise of air fryers over the last year or so though I also feel like I've been bombarded with information on them and was pleasantly surprised at just how _capable_ they are... I was mad only using the old one for the odd plate of chips, these things can cook _so much_ and do it well!

So I decided to take a chunk of my cashback out (boosted by 6% as I converted them to gift vouchers!) and treat myself and my family to a fancy all-singing, all-dancing Ninja AF451.

![Ninja Foodi Max AF451](/img/2023-04/AirFryer.jpg)
<sub>This bad boy is HUGE!</sub>

It's been a few weeks since it arrived now and I've been cooking with it _loads_ - I've cooked steak, whole chickens, sides of salmon, roast beef, chicken wings... my wife has used it almost daily to do 'boiled' eggs! It's so easy to use, so quick and so, so versatile!

But anyway... that's not really the purpose of this post is it!

Being the nerd that you know I am, I wanted to get the most out of it so decided to throw together a little app for myself!

### Enter Air Fryr

I had no idea what to call the app - I started off with the idea of _'Air Fryer Calculator'_, but as the app came together I realised that the calculator is really a _'nice to have'_ feature - the headline feature is probably actually the notebook.

So, rather jokingly, I did what loads of apps seem to have done and decided to just drop some vowels - well, if it's good enough for Flickr and Tumblr!

...and there we have it: **Air Fryr**

### What does it do?

In v1.0 Air Fryr has two main features:

#### The Calculator

Firstly, it offers a quick calculator function - air fryers are significantly faster than a standard oven, but can also cook the same dishes at lower temperatures. When I was researching what to buy I came across a simple algorithm for converting oven cooking times to air fryer ones - essentially, know 20C/35F off the temperature, and 20% off the time.

Something super easy to do in an app, and Flutter/Material Design makes this even easier with simple to use sliders (although maybe I'll write up a more tech focused note later as to why it's not really that easy when you start adding options like changing the units and making saved calculations editable!)

![The app calculator](/img/2023-04/Home-Light.png)

### The notebook

Secondly, the notebook... now I'm a bit of a pragmatist, and I know that an algorithm like the above is really just a _general rule_, it'll be right some of the time, but every oven and every air fryer is different (and let's not get started on individual tastes when it comes to food!), so I thought, _'why not allow calculations to be saved and edited later'_, hence _The Notebook_:

![The Notebook](/img/2023-04/AirFryerNotebook.jpg)

Now what's the point of a notebook if you can't keep notes in it, so as well as allowing you to save a title, the cooking temperature and time, you can also write detailed notes with each entry and categorise the note for future reference (at present the categories just show against the note with an icon, but in a future release I'll add in a category filter too!).

The notes are fully editable, so if you realise your dish needed more time, to be hotter or just that you want to make a note of what to try the next time you cook it, you can quickly and easily update the entry.

### Notebook Search

I know I mentioned two things, but since starting to write this post I got sidetracked and released an updated v1.1 of the app (I'm nice like that) which also includes a real-time search function, to quickly find things in an ever growing notebook

![Notebook Search](/img/2023-04/NotebookSearch.png)

...and that's a wrap! I had a lot of fun putting this together (you know how I _love_ building silly wee apps!) and have a few ideas to still add to it, so keep an eye out for a v1.2 before too long!

If you'd like to give Air Fryr a try you can find it [on the App Store](https://apps.apple.com/us/app/air-fryr/id6446950736) and [on Google Play](https://play.google.com/store/apps/details?id=com.stifdev.airfryr)
