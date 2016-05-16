---
layout: post
title: "Wordpress tips: bulk update of permalinks and image paths"
thumbnail: "http://oldsite.andreafortuna.org/technology/images/wpsql.png"
description: "When you change domain for an existing wordpress blog, it may be difficult to upgrade permalinks and posts meta."
keywords: Wordpress, Tips, SQL, Programming
category: Programming
tags: 
- Wordpress
- Tips
- SQL


---
{% include JB/setup %}

When you change domain for an existing wordpress blog, it may be difficult to upgrade permalinks and posts meta.

![Wordpress](/technology/images/wpsql.png)
<!-- more -->

In [this post](http://kevindees.cc/2011/08/updating-wordpress-permalinks-and-image-paths/){:target="_blank"} Kevin Dees presents a quick and easy solution, with 3 SQL commands:

<script src="https://gist.github.com/andreafortuna/874618774e729dbb9635.js"></script>

Warning: read the notes in the post before launching random SQL commands:

1. Backup the DB first.
2. Second, you will need to change the domain placeholders in this code to your own before it will work it’s magic.
3. If you have any plugins installed this code may change the domins for them too. This is not guaranteed so you will need to check the DB first.
4. If a plugin has added its own tables and you need to change the links it stores, you will need to run the replace on those cells as well.
5. This is the most important! Be sure to change the table prefix. If you don’t this will not work when it has been modified.