---
title: "Addings Ads"
date: 2022-09-14T11:06:50+01:00
draft: false
socialshare: true
Categories: ["Blog"]
Tags: ["Blog", "Ads"]
featuredImage: "/img/2022-09/DigitalScreens_TimesSquareSpectacular.jpeg"
---

## Adding Ads... and stuff...
---


Yep, I've done it...sorry.

I've gone ahead and added some hideous advertising all across the site...but _why?_

Good question, and I'm not sure I have a good answer... It's not really to _make money_, as the volume of readers of this site are _tiny_. It's a site I've built far more for myself than for anyone else, but hey, if you've found you're way here thanks for visiting (and if you've enjoyed your time here, even better!)

The site does _cost me money_ though. Not a lot, as I host it for free via [github pages](pages.github.com), but that lovely vanity domain up in the address bar does cost a bit (and I've been paying for it for a decade...), so maybe I can offset a little of that cost. Hell, to be honest, covering that whole cost for a year would be _more success than I've ever dreamed of_ for the site!

Anyway, maybe the more interesting question is... _how have I done it?_

### Implementing Ads

In all honesty, implementing ads on the site turned out to be significantly easier than I'd expected.

I've mentioned in previous posts that I've put this site together using [Hugo](www.gohugo.io) a static site generator - at a basic level all that means is that I can create quite posts written in [Markdown](https://www.markdownguide.org/basic-syntax/), write a wee command in Terminal, and then have a website generated that I can quickly post (and by linking it up with github pages, all I need to do is commit any changes to my remote code repository and it automagically publishes...it really is nice!)

It's hopefully clear then that the benefits of a static site generator are the simplicity of getting new posts published, and unlike a system like WordPress the sites are usually super fast because all the processing happens when you compile the site - after that, it's all just flat pages.

The _downside_ to this though, is that it can be more awkward to do make changes to a site, such as implementing change that requires additional lines of code added within the pages etc.

### Google Analytics

One of the benefits of Hugo is it's integration of Google Analytics - thanks to this integration, adding analytics support to the site was as simple as updating a configuration file with an analytics ID - I did this about 3 years ago when I remade the site, and have been surprised that there have literally been _tens of people_ reading my nonsense!

### Cookie Banner

I then realised that if I wanted to implement ads, I'd need to ensure I had a cookie pop-up (necessary since I'm in the EU, although I'm in the _this is a terrible solution_ camp when it comes to cookie pop-ups!).
Now, on reflection it turns out this might have been _wasted effort_ (see the section on Adsense for more!)

To do this, I followed [this guide](https://dev.to/basman/add-a-cookie-warning-notice-to-a-hugo-powered-site-4d34)

You'll see that this required me to add lines of code into the header and footer code of the site, i.e. pop some code inside the html <head> section, and just before the end of the </body> section. The guide doesn't mention how the author specifically did this, but thankfully a bit of digging around the documentation for the [hello friend theme](https://github.com/panr/hugo-theme-hello-friend) that I use for the site, highlighted that the creator had already thought about this and included specific files that would be pulled into these locations.

Specifically a _'prepended_head.html'_ file and an _'extended_footer.html'_ file - so all I needed to do to add code in these places was to create these files within my _/layouts/partials/_ folder... and just like magic when I recompiled the site, they just worked!

The pop-up as created creates links to a [privacy policy](/privacy/website_privacy_policy/) and [cookie policy](/privacy/website-cookie-policy/)...so I then had to create these too!

Rather nicely, when I thought about this I realised that I could easily create a /privacy/ sub-folder to the site, that still generated all sub-pages as expected, but didn't show them in the main blog view (like anything in my /posts/ folder would) - this let me also 'hide' my other privacy policies for the apps I've built. I'd still like to keep these published and accessible, but it means they don't take up space in the wider blog view.

### Adsense

Lastly, I had to implement the ads themselves. To do this, I enrolled for [Google's Adsense](www.google.com/adsense) and... hell, that's actually pretty much it!

Google have an option to let them place ads for you, so initially I've just said _"here's my website, place ads on it"_, and toggled a couple of settings (for example I've turned off things like full page ads between page loads...because that sounds _awful_, as well as turning off persistant bottom of page ads).
So adding ads across the whole site was as simple as adding another couple of lines of code in the page header (which will then populate to every page on the site).

As part of this they can also auto-generate a GDPR compliant banner for the site (so as above, I could have saved myself all the effort of generating my own pop-up banner!)

I'll be keeping a wee eye on things to see how these look going forward - there is an option to turn this off and manually implement ad units on the pages myself, if it all looks too messy I'll take a look at that.

Anyway, what do you think? Does implementing ads make the whole site suddenly _awful_. Is it acceptable as a necessary evil to help me keep this site going (and hell, if they actually start making double digit $$$'s then maybe I'll actually be motivated to write more...sorry...)


_Cover image credit timessquarenyc.org_
