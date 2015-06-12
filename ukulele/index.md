---
layout: page
title: Ukulele transcriptions, tutorials, videos
description: "Ukulele transcriptions, tutorials, videos"
thumbnail: "http://www.andreafortuna.org/ukulele/images/ukulele2.jpg"
tagline: Ukulele
---
{% include JB/setup %}

«If everyone played the ukulele, the world would be a better place.»
--
<p style="text-align: right;font-style: italic;"><strong>Jake Shimabukuro</strong></p>

![My Ukulele](/ukulele/images/ukulele2.jpg)

<hr/>

As a child I started studying music and classical guitar, then i dedicated myself also to other musical genres.

Recently, I had a "love at first sight" for the ukulele: a musical instrument that many call a "little guitar", but with a soul and a technique radically different from his cousin with 6 strings.

In this section I am going to publish my thoughts, my exercises and my transcriptions.
<hr/>
<p style="text-align: right;float:right;margin-top:60px;margin-left:20px;"><a href="rss.xml"><i class="fa fa-rss fa-4x" >&nbsp;</i></a></p>
<div class="blog-index">

{% for post in site.posts %}
    {% if post.categories contains 'ukulele' %}
        {% assign content = post.content %}
        {% include post_detail.html %}
    {% endif %}
{% endfor %}

</div>


