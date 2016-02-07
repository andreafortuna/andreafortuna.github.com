---
layout: post
title: "Testing the performance of a new system before website's migration"
description: "a very simple trick to testing the performance of a new system before the website's migration"
category: Programming
tags: 
- Tips
- Programming
- Webdesign
- iframe
- javascript

---
{% include JB/setup %}
Situation: the new server for the site is ready. How can I be sure the sizing is being made correctly and the machine is able to improve the performance of the previous server?

![Site Speed](http://1.bp.blogspot.com/-7teIbvGZnlo/VK9viPRDQtI/AAAAAAAAASA/z5ZuhyMv8Fo/s1600/loading.png)
<!-- more -->

With a simple (and stupid) trick!

Add a hidden iframe to the live site that makes the same request to your development system. (ex: *www.site.com/some/url/123* -> *dev.site.com/some/url/123/*). 

Place the code in a common section, that is repeated in all site pages (es. footer).

You can use a simple javascript code, like this snippet:

<script src="https://gist.github.com/andreafortuna/d5eedbcc2fbc05c7e3dd.js"></script>

