---
layout: page
title: Technology articles
description: "My articles about technology, programming, hacking, security and geekness"
thumbnail: "http://www.andreafortuna.org/technology/images/technology_cover.jpg"
keywords: technology, hacking, programming, security, geekness, privacy
tagline: Technology
---
{% include JB/setup %}

![Tech Cat](/technology/images/technology_cover.jpg)

«We are stuck with technology when what we really want is just stuff that works.»
--
<p style="text-align: right;font-style: italic;"><strong>Douglas Adams</strong></p>

<hr/>

[![Security](/security/images/security_cover.jpg)](/security/)

[![Programming](/programming/images/programming-cover.jpg)](/programming/)

<hr/>

Latest posts
--

<p style="text-align: right;float:right;margin-top:10px;margin-left:20px;"><a href="rss.xml"><i class="fa fa-rss fa-4x" >&nbsp;</i></a></p>
<div class="blog-index">
{% for post in site.posts %}
    {% unless post.categories contains 'Ukulele' or post.categories contains 'Running' or post.categories contains 'WeeklyRoundup' or post.categories contains 'Wellness' or  post.categories == empty %}
     
        {% assign content = post.content %}
        {% include post_detail.html %}
       
    {% endunless  %}
{% endfor %}
</div>



