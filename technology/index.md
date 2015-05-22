---
layout: page
title: Technology articles
tagline: Technology
---
{% include JB/setup %}

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


