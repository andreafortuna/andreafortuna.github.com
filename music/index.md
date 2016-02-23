---
layout: page
title: "My music: research, experiments, opinions and compositions" 
description: "My music: research, experiments, opinions and compositions"
thumbnail: "http://www.andreafortuna.org/music/images/cover.jpg"
keywords: Music, tabs, transcriptions, arrangements
tagline: Music
---
{% include JB/setup %}

![Music](/music/images/cover.jpg)


«Lesser artists borrow, great artists steal.»  
--
<p style="text-align: right;font-style: italic;"><strong>Igor Stravinsky</strong></p>



<hr/>


[![Guitar](/music/images/guitar_cover.jpg)](/guitar/)

[![Ukulele](/music/images/ukulele_cover.jpg)](/ukulele/)

<hr/>


Latest posts
--

<p style="text-align: right;float:right;margin-top:10px;margin-left:20px;"><a href="/music/rss.xml"><i class="fa fa-rss fa-4x" >&nbsp;</i></a></p>
<div class="blog-index">

{% for post in site.posts limit:30 %}
     {% if post.categories contains 'Guitar' or post.categories contains 'Music' or post.categories contains 'Ukulele' %}
    
        {% assign content = post.content %}
        {% include post_detail.html %}
       
    {% endif %}
{% endfor %}

</div>

<p style="text-align: right;font-size:1.5em;"> <a href="./archive/">All posts...</a> </p>


