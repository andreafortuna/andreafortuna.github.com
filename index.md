---
layout: page
title: 
tagline: Code monkey by day, code ninja by night...
---
{% include JB/setup %}

 
<div class="blog-index">
{% for post in site.posts limit:5 %}
{% assign content = post.content %}
{% include post_detail.html %}
{% endfor %}
</div>
<hr>
<a href="archive.html">All posts...</a>



