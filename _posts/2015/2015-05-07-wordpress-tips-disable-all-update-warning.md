---
layout: post
title: "Wordpress tips: disable all update notifications without plugins"
description: "Disable Update Notifications and Maintenance Nags in WordPress"
category: Programming
tags: 
- Wordpress
- PHP
- Tips


---
{% include JB/setup %}
In some configurations with special customizations, updating wordpress cannot/must be made.

How to disable the update messages without using a [special plug-in](https://wordpress.org/plugins/disable-wordpress-updates/)?

![Wordpress](http://oldsite.andreafortuna.org/images/wordpress.jpg)
<!-- more -->

With a simple snippet! Paste this code in ***function.php*** of the active theme:

<script src="https://gist.github.com/andreafortuna/4f370a94c20861947c24.js"></script>
