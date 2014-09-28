---
layout: page
title: 
tagline: Code monkey by day, code ninja by night...
---
{% include JB/setup %}

 
<div class="blog-index">
{% assign post = site.posts.first %}
{% assign content = post.content %}
{% include post_detail.html %}
</div>

<hr>

<ul class="posts">
  {% for post in site.posts limit:5 %}
    <li><span>{{ post.date | date_to_string }}</span> &raquo; <a href="{{ BASE_PATH }}{{ post.url }}">{{ post.title }}</a></li>
  {% endfor %}
</ul>



