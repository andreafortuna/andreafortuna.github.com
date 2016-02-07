---
layout: post
title: "Wordpress tips: courtesy page for anonymous users without plugins"
description: "Create on wordpress a courtesy page for anonymous users without plugins"
category: Programming
tags: 
- Wordpress
- PHP
- Tips


---
{% include JB/setup %}
It may happen that you have need to make a wordpress site accessible only to registered users or administrators (for example, during an update). 

Let's see how to make a courtesy page for anonymous users without using any plugins.

![Wordpress](http://www.andreafortuna.org/images/wordpress2.jpg)
<!-- more -->

It is enough to add on top of the file ***header.php*** of the active theme the following code snippet:


<script src="https://gist.github.com/andreafortuna/c731ae213c04b068d81b.js"></script>

In this way the anonymous users will see only a courtesy message, while the logged users will display all pages of the site.
