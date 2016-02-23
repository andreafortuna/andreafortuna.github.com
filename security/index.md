---
layout: page
title: IT Security Articles
description: "My articles about security and privacy"
thumbnail: "http://www.andreafortuna.org/security/images/security_cover.jpg"
keywords: technology, hacking, security, privacy
tagline: Security
---
{% include JB/setup %}

![Security](/security/images/security_cover.jpg)

«Being able to break security doesn’t make you a hacker anymore than being able to hotwire cars makes you an automotive engineer.»
--
<p style="text-align: right;font-style: italic;"><strong>Eric Raymond</strong></p>


<hr/>

Latest posts
--

<p style="text-align: right;float:right;margin-top:10px;margin-left:20px;"><a href="rss.xml"><i class="fa fa-rss fa-4x" >&nbsp;</i></a></p>
<div class="blog-index">
{% for post in site.posts %}
    {% if post.categories contains 'Security' %}
        {% assign content = post.content %}
        {% include post_detail.html %}
    {% endif %}
{% endfor %}
</div>



