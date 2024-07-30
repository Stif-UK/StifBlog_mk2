---
title: "Blog Workflow"
date: 2019-09-24T16:31:56+01:00
draft: false
Categories: ["Development"]
Tags: ["Blog"]
featuredImage: "/img/2019-11/blogging.jpg"
---

## My blog workflow
---
So, I'm writing this post as much for my own benefit as anyone else's. The last time I tried to build a blog I left it alone for a while and when I came back to it I'd forgotten the steps to build it... If this is of benefit to anyone else though, great!


I've put this blog together using [Hugo](https://gohugo.io "gohugo.io"), a static site generator. What does that mean? Simply, I can write pages in simple markdown, then run Hugo and it takes all the pages and assets and outputs a fully formed website which can then be uploaded to the web.

I then use git to version control it and push changes to a remote [github](https://github.com "github.com") repository ([like this](https://help.github.com/en/articles/adding-an-existing-project-to-github-using-the-command-line)), and make use of [_github pages_](https://pages.github.com/ "github pages") to host the site (with my domain pointed to github per [these instructions](https://help.github.com/en/articles/using-a-custom-domain-with-github-pages "Using a custom domain with github pages") ).


So, that's the background, but how do I go about generating and uploading a post.
Well, I do 90% of that via Terminal _because it's cool_.

<sub>_I assume this would be virtually identical on a Windows machine via Command Prompt, I'll give it a go at some point._ </sub>

___

#### Creating the post

* Open Terminal

* Create a new post  
`Hugo new posts/post_name.md`

* Open the generated file in Atom (the program I use to write and edit markdown, amongst other things)  
`open -a "Atom" stifblog_mk2/content/posts/post_name.md`  

  <sub> _Note: The "a "Atom"" part of this is only required as my Macbook seems determined to only let me edit markdown posts in Xcode, despite Atom being set as the default..._ </sub>

* Edit the front matter of the post to add any categories or tags that I want to associate with the post (_I often actually do this last_).

* Write the post (_the hardest part for someone as un-creative as me!_)

* Preview the post by running a local server  
`Hugo server -D`

This command runs a local server that hosts the site at _localhost:1313_  
The _'-D'_ suffix tells Hugo that I want to see posts that are still marked as drafts (until the draft flag is set to false Hugo won't include them in the site build).

* Finally, once the post is ready (_and saved! CMD + S_ ), set the draft flag to false and generate the _'Prod ready'_ site  
`Hugo`

#### Getting it live

The last thing to do is to create a git commit and then push the changes to the remote repository, from there github works it's magic.

* First, I like to check that the only deviations from what's on github are those I just made  
`git status`  
<sub>_I do this at the start if I am, or have been,  working on a different machine._ </sub>

* Stage **all** of the changed files  
`git add .`  

* Now turn the staged changes into a _commit (including a suitable message)_  
`git commit -m"Description of the change"`

* Finally, push the changes to the remote master branch  
`git push`

Since writing a post is simple text (and the odd image), rather than any structure or code changes, I'm comfortable commiting straight to the _master_ branch - if I was making any code changes (which I might try to do later...) then I'd create a develop or specific feature branch to do this on first.

So there we go - how long will it be before I need to pull this post up to remind me how it all works?
