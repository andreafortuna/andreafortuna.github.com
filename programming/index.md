---
layout: page
title: Programming articles
description: "My articles about programming and hacking"
thumbnail: "http://www.andreafortuna.org/programming/images/programming-cover.jpg"
keywords: technology, hacking, programming
tagline: Programming
---
{% include JB/setup %}

![Programming](/programming/images/programming-cover.jpg)

«Most good programmers do programming not because they expect to get paid or get adulation by the public, but because it is fun to program.»
--
<p style="text-align: right;font-style: italic;"><strong>Linus Torvalds</strong></p>



<hr/>

Latest posts
--

<p style="text-align: right;float:right;margin-top:10px;margin-left:20px;"><a href="rss.xml"><i class="fa fa-rss fa-4x" >&nbsp;</i></a></p>
<div class="blog-index">
{% for post in site.posts %}
    {% if post.categories contains 'Programming' %}
        {% assign content = post.content %}
        {% include post_detail.html %}
    {% endif %}
{% endfor %}
</div>



