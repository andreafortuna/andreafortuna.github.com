---
layout: page
title: "My music: research, experiments, opinions and compositions"
description: "My music: research, experiments, opinions and compositions"
thumbnail: "http://www.andreafortuna.org/music/images/cover.jpg"
keywords: Music, tabs, transcriptions, arrangements
tagline: Music
---
{% include JB/setup %}

![Music](/music/images/music_cover.jpg)

<p style="text-align: right;float:right;margin-top:10px;margin-left:20px;"><a href="/ukulele/rss.xml"><i class="fa fa-rss fa-4x" >&nbsp;</i></a></p>
<div class="blog-index">

{% for post in site.posts %}
     {% if post.categories contains 'Guitar' or post.categories contains 'Music' or post.categories contains 'Ukulele' %}
    
        {% assign content = post.content %}
        {% include post_detail.html %}
       
    {% endif %}
{% endfor %}


</div>


