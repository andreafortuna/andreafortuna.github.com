---
layout: page
title: Technology articles
tagline: Technology
---
{% include JB/setup %}

«We are stuck with technology when what we really want is just stuff that works.»
--
<p style="text-align: right;font-style: italic;"><strong>Douglas Adams</strong></p>

<hr/>

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


