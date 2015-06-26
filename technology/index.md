---
layout: page
title: Technology articles
tagline: Technology
---
{% include JB/setup %}

«We are stuck with technology when what we really want is just stuff that works.»
--
<p style="text-align: right;font-style: italic;"><strong>Douglas Adams</strong></p>

![Tech Cat](/technology/images/technology.png)

<hr/>
<p style="text-align: right;float:right;margin-top:60px;margin-left:20px;"><a href="rss.xml"><i class="fa fa-rss fa-4x" >&nbsp;</i></a></p>
<div class="blog-index">
{% for post in site.posts limit:50 %}
    {% unless post.categories contains 'ukulele' or post.categories contains 'running' or post.categories contains 'weeklyroundup' %}
        {% assign content = post.content %}
        {% include post_detail.html %}
    {% endunless  %}
{% endfor %}
</div>
<br>
<a href="archive.html" style="float:right;">All posts...</a>
<br>


