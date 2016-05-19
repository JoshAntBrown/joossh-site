---
layout: post
title:  "Experiences with Jekyll"
date:   2016-05-19 20:40:00 +0100
---

For a while I've been debating about adding a blog to my website, somewhere I can keep a log of my thoughts, ramblings and other content I create. Somewhere I can call my own. I spend a lot of my day building, creating and making web applications and for once I wanted something that just felt simpler. Away from Wordpress, away from Ghost, away from anything custom.

So I decided to give Jekyll a look, I've seen it mentioned briefly here and there across the Internet but never really given it much thought or attention until now. A few days ago I took a bit of a dive into Jekyll and have been playing with it in the free time I get converting some of the styling of my old site and bringing it into Jekyll.

## What is Jekyll?
Jekyll is a static site generator with a focus on blogging which you can find at [http://jekyllrb.com](http://jekyllrb.com). A static site generator typically takes some styles, some templates and some content and uses them to generate all the pages in your site. Every one of these posts are simply a markdown file that I write which then gets translated into the final static web page. It's a really smart way of building a website without having to rely on some database or complex server side logic which would ultimately slow your website down.

## Who is Jekyll for?
Jekyll isn't great for everyone. If you're not web savvy then it's probably not worth it too much, it does require some knowledge of the command line, html, and Markdown. Whilst there are themes you can download and then you just write files for posts it still requires you to understand Markdown and it's Front Matter configuration, a small piece of YAML that sits at the top of your markdown file to describe metadata about the post or page. But if you're a web designer or developer then it's a great tool to have in your arsenal.

Keep in mind though that Jekyll will generate static files which means you won't be able to include things like your own comments system. You can however use a third-party hosted solution such as [Disqus](https://disqus.com/) or [Facebook Comments](https://developers.facebook.com/docs/plugins/comments/).

## How to get started?
I'm not going to go into too many details on how to get started with Jekyll as their website does a pretty good job of that. You'll need to have installed Ruby (Mac's come with it installed from new) and then you can install it by running the following in your command line:

```
sudo gem install jekyll
jekyll new project-name
```

That will create a folder called project-name with a default Jekyll setup. Now you'll want to see what that website looks like so lets get Jekyll to build and serve the files.

```
cd project-name # Change into the project-name directory
jekyll serve
```

You should then be able to point your web browser to http://127.0.0.1:4000/ and see Jekyll's default template. The \_site folder is where your generated code goes so you shouldn't need to touch that ever. The rest of the files are your content, templates, styles and configuration. From there you can dive through the files and see what you can do, keep an eye on the console running the server and it'll build you're site as you change things so you can refresh and see your latest changes at any time.
