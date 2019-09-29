---
title: "Blog Workflow"
date: 2019-09-24T16:31:56+01:00
draft: true
Categories: ["Development"]
Tags: ["Blog"]
---

## My blog workflow
---
So, I'm writing this post as much for my own benefit as anyone else's. The last time I tried to build a blog I left it alone for a while and when I came back to it I'd forgotten the steps to build it... If this is of benefit to anyone else though, great!

___

I've put this blog together using [Hugo](https://gohugo.io "gohugo.io"), a static site generator. What does that mean? Simply, I can write pages in simple markdown, then run Hugo and it takes all the pages and assets and outputs a fully formed website which can then be uploaded to the web.

I then use git to version control it and push changes to a remote [github](https://github.com "github.com") repository ([like this](https://help.github.com/en/articles/adding-an-existing-project-to-github-using-the-command-line)), and make use of [_github pages_](https://pages.github.com/ "github pages") to host the site (with my domain pointed to github per [these instructions](https://help.github.com/en/articles/using-a-custom-domain-with-github-pages "Using a custom domain with github pages") ).

___

So, that's the background, but how do I go about generating and uploading a post.
Well, I do 90% of that via Terminal _because it's cool_.

<sub>_I assume this would be virtually identical on a Windows machine via Command Prompt, I'll give it a go at some point._ </sub>

___

* Open Terminal

* Create a new post  
`Hugo new posts/post_name.md`

* Open the generated file in Atom (the program I use to write and edit markdown, amongst other things)  
`open -a "Atom" stifblog_mk2/content/posts/post_name.md`  

  <sub> _Note: The "a "Atom"" part of this is only required as my Macbook seems determined to only let me edit markdown posts in Xcode, despite Atom being set as the default..._ </sub>

* Edit the front matter of the post to add any categories or tags that I want to associate with the post (_I often actually do this last_).

* Write the post (_the hardest part for someone as un-creative as me!_)
