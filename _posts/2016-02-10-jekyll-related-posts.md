---
layout: post
title: "Jekyll: a custom 'related posts' script"
description: "I do not like the system of related articles native of Jekyll, so for my site so I created a short script to filter posts similar based on shared tags."
thumbnail: "http://www.andreafortuna.org/technology/images/jekyll.png"
keywords: Jekyll,Programming, Ruby, Theming, Liquid
category: Programming
tags: 
- Jekyll
- HTML5
- Blogging

---
{% include JB/setup %}
I do not like the system of related articles native of Jekyll, so for my site so I created a short script to filter posts similar based on shared tags.

![Jekyll](/technology/images/jekyll.png)

The snippet is very simple, it can be placed in post.html of the theme:

<script src="https://gist.github.com/andreafortuna/31152c34cf6077d3699f.js"></script>

