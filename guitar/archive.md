---
layout: page
title: Guitar arrangements, tips and exercises
description: "Guitar arrangements, tips and exercises"
thumbnail: "http://www.andreafortuna.org/guitar/images/guitar.jpg"
keywords: guitar, tabs, transcriptions, arrangements, music
tagline: Guitar
---
{% include JB/setup %}

![Guitar](/music/images/guitar_cover.jpg)

<p style="text-align: right;float:right;margin-top:10px;margin-left:20px;"><a href="/guitar/rss.xml"><i class="fa fa-rss fa-4x" >&nbsp;</i></a></p>
<div class="blog-index">

{% for post in site.categories['Guitar'] }
        {% assign content = post.content %}
        {% include post_detail.html %}
{% endfor %}

</div>


