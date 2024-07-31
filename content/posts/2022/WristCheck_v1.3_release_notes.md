---
title: "WristCheck v1.3 Release Notes"
date: 2022-10-25T15:44:33+01:00
draft: false
socialshare: true
Categories: ['Development', 'Watches', 'WristTrack App']
Tags: ['App Development', 'Watches', 'Tech', 'Release Notes']
featuredImage: "/img/2022-10/WristCheck_PickImg_code.png"
---

## WristCheck v1.3 Release Notes
---
Version 1.3 of WristCheck is now available to the app beta testers, so will be released over the next couple of days (as I write this I've already got confirmation that Apple have approved it, so it's just a case of hitting the button!) As [before](/posts/wristcheck_v1.2/) I thought I'd share a post with a bit more information on what's changed, expanding a bit on the bullet points you'll see in the app or on the store listings.

### Updates to Image Handling

This is probably the biggest change in v1.3 and perhaps worth discussing a bit here. Firstly, to summarise how the app handles images, when a user wants to add a watch image to a watch record, they click a wee 'add image' button, which pulls up a _bottom sheet_ allowing them to select whether to select the image from their gallery, or to take a new one with their camera - this is achieved using the Flutter _image_picker_ library.

Once selected or taken, the image file is then passed to a second library, _image_cropper_ to, you guessed it, crop it - by doing this I can control the aspect ratio of the final image, which allows me to better manage the page layout.

Finally, the image is saved - there are two parts to this. First, the image file is saved locally on the phone and secondly the _path_ to this image file is saved as a parameter of the watch record in the database (I purposely keep the images and watch records separate - a small database means a faster, more responsive app even for large collections, thus the images themselves are _not_ in the database).

As you can imaging, to achieve all of the above I've got a series of methods written, including _pickImage()_, _saveImage()_, _imageSourcePopUp()_ etc.

Initially some of these were methods within the class for the page, and others were in my _WatchMethods()_ class, but given these all relate to the same purpose - managing images - I began v1.3 by refactoring all image related code out into its own _ImageUtil()_ utility class.

This keeps everything together in its own wee corner of the app, simplifying code maintenance and supporting reusability.

As part of this refactor I also fixed some hidden issues with the earlier versions of the app.
Firstly, the app now creates an _/img/_ subdirectory in the apps storage - on Android you'll never see this as app data is hidden and encrypted, but on iOS you can use _Files_ to navigate the app directory and see the structure. Therefore from v1.3 all images will live in this sub-folder (which will make building a backup solution for images in future easier too!)

I also updating the way images are named - previousy the image_cropper plugin threw out a random name, which is fine if you never see the file, but will be rubbish if you export them to use later - so now the images get a more human readable name!

Secondly, in the early versions of the app images would be saved along with their paths (as above)...but they were never deleted! _(oops!)_
Therefore if you deleted a watch or changed it's picture, the old one was still sitting there taking up space on your phone...
Clearly, that is _Not Very Good!_

Thus in v1.3 I've fixed this! Now whenever a new image is saved, the old one is deleted (if it exists), as well as images being deleted when a watch is deleted, or if the 'delete collection' button is triggered, they're all deleted (I doubt anyone will use that 'delete all' function, but it was useful for testing so I kept it in...)

But I didn't just do this refactoring to fix _glaring issues_, it was also done to support two new features...

### Add watch images when adding a new watch

I was asked more than once why, when adding a new watch record, the user had to add the watch and then go in and edit it to add an image to it. Partly this was down to how I'd implemented the code to save the image. Partly it was down to needing a watch record to exist, before it could save the image path to it (see my note above about keeping the images out of the database).

But following this refactoring, I've now made it easy for me to manage this - the UI isn't fantastic to be honest _(is any of my UI?)_ but it works, and users can now add watch pictures at the same time as they record their new watch in the app!

### Add caseback images!

One of the most requested additions to the app was the ability to add a second image for each watch, to show the caseback - and with the above work complete, this became a nice easy task! Now you can save both a main image and a second one (and hey, nobody is forcing you to take a picture of the caseback, you can use it for the bracelet clasp or whatever you want!)

![WristCheck CaseBack Image](/img/2022-10/CaseBackImg.png)
<sub>_Some casebacks are worth sharing!_</sub>

### _"Minor Improvements"_

Every app release always includes a few _little things_ that don't make the headlines, but again it's good to give an idea of what's going on!

Firstly, another change that's come from user feedback, is that watch names now auto-capitalise the first letter of each word - a small change, but one that was asked for a few times!

_(as an aside, comments on this blog seem to have broken...sure that's my fault... you can provide feedback via the app stores themselves as a user review, or via email - again on the store listings - or finally there's a thread on the [Christopher Ward Forum](https://www.christopherwardforum.com/offtopic/wristcheck-stif-s-mobile-watchbox-app-project-almost-at-beta-t59567.html) )_

Another change that falls under the 'minor improvements' category is updating the help text relating to the watch calendar view - if you click to see the dates you've worn a watch when no dates are tracked the on screen text was misleading, and there was no additional guidance on this page - which is rubbish since this is where you can add to or amend the watches history! (I think I'll also write a [guide](/categories/wristcheck-guides-faqs/) about this at some point too...)


### App Review Prompt

Lastly, to round out these release notes the last change was to implement a review prompt in the app. Both Android and iOS provide libraries to do this, which are now also both encapsulated in a Flutter library, so the core implementation is pretty straightforward.

Both app stores also ensure that this isn't abused, and thus any request to show a prompt is first checked with the underlying platform before it's shown (thus nobody should ever get one at _every login_)

I laid some groundwork for this in an earlier release _(v1.1 I think)_ by recording in the background how many times the app was opened and how many times watches had been marked as worn. These stats live locally on the device and weren't used, but it's allowed me to write some logic to make sure the prompt is triggered only after a user has had a chance to make some use of the app.
If dismissed it will then potentially re-prompt after around 100 days - a good space to hopefully help gather further feedback as I continue to improve the app.

I _haven't_ hidden this prompt behind a _'do you like this app'_ question first (lots of apps do this, to make sure that only users who are going to rate an app highly get the actual prompt)... partly this is through laziness, it would be more work to do, but at this point I'm not desperate for everyone to rate WristCheck 4 or 5 stars (although it would be nice!), but rather I want to get as much feedback as possible to help me continue to make the app better!

Anyway, that's it for v1.3... v1.4 will be along soon enough in another 3-4 weeks!
