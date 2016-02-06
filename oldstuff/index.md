---
layout: page
title: Old stuff
description: "Old stuff and articles from previous versions of this blog"
thumbnail: "http://www.andreafortuna.org/technology/images/technology.png"
keywords: technology, hacking, programming, security, geekness, privacy, oldstuff, andreafortuna.wordpress.com,andreafortuna.org
tagline: Old Stuff
---
{% include JB/setup %}

![OldStuff](/images/oldstuff.jpg)



Old stuff and articles from previous versions of this blog

<hr/>
<div class="blog-index">
{% assign posts_collate = site.posts | where: "category", "" %}
{% include JB/posts_collate %}
</div>
<br>

