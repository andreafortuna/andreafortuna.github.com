---
layout: post
title: "How to schedule a post in Jekyll?"
description: ""
category: Programming
tags: 
- Blogging
- Jekyll
- GitHub
---
{% include JB/setup %}
Since i started blogging with jekyll i felt the lack of the ability to schedule posts, ignoring the fact that - with a small change to ``_config.yml`` - i can plan my posts even on blogs hosted by **GitHub**.

![Jekyll](http://girliemac.com/assets/images/articles/2013/12/jekyll.png)

<!-- more -->
The solution I found in a post written by [Mirosław Pragłowski](http://praglowski.com/2013/03/14/scheduling-a-future-posts-in-jekyll/):

>The solution is very simple…
>    
>…and already build in Jekyll. Just add a line: ``future: false`` in your ``_config.yml`` and then add a post with: ``rake post title="Some future post" date="2013-06-07"`` commit, push and that’s all - the post will be visible on a given date.
… almost :(
    
>You need to made *GitHub Pages* to rebuild your blog - by pushing something to repository or in other way - need to find some cron task to do it for me.

