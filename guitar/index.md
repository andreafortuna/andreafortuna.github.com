---
layout: page
title: My2c about the guitar
description: "Guitar arrangements, tips and exercises"
thumbnail: "http://www.andreafortuna.org/guitar/images/guitar.jpg"
keywords: guitar, tabs, transcriptions, arrangements, fingerstyle, music
tagline: Guitar
---
{% include JB/setup %}

![Guitar](/music/images/guitar_cover.jpg)

«I had only one teacher, myself, and only one student, myself.»
--
<p style="text-align: right;font-style: italic;"><strong>Andrés Segovia</strong></p>



<hr/>

Latest posts
--

<p style="text-align: right;float:right;margin-top:10px;margin-left:20px;"><a href="/guitar/rss.xml"><i class="fa fa-rss fa-4x" >&nbsp;</i></a></p>
<div class="blog-index">

{% for post in site.categories['Guitar'] limit:10 }
        {% assign content = post.content %}
        {% include post_detail.html %}
{% endfor %}

</div>

<p style="text-align: right;font-size:1.5em;"> <a href="./archive/">All posts...</a> </p>

