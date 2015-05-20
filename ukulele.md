---
layout: page
title: Ukulele stuff
tagline: Ukulele
---
{% include JB/setup %}

![My Ukulele](/images/ukulele.jpg)

As a child I started studying music and classical guitar, then i dedicated myself also to other musical genres.

Recently, I had a "love at first sight" for the ukulele: a musical instrument that many call a "little guitar", but with a soul and a technique radically different from his cousin with 6 strings.

In this section I am going to publish my thoughts, my exercises and my transcriptions.

<hr/>
 
<div class="blog-index">

{% for post in site.posts %}
    {% if post.categories contains 'ukulele' %}
        {% assign content = post.content %}
        {% include post_detail.html %}
    {% endif %}
{% endfor %}

</div>


