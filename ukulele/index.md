---
layout: page
title: Ukulele tabs and arrangements
description: "Ukulele tabs and arrangements, tutorials, videos"
thumbnail: "http://www.andreafortuna.org/ukulele/images/ukulele2.jpg"
keywords: ukulele, tabs, transcriptions, arrangements, fingerstyle, music, tabs
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

<a href="/ukulele/tabs.html">Tabs and arrangements archive</a>
--

- [Classical pieces](/ukulele/tabs.html#classicalpieces)
- [Traditionals](/ukulele/tabs.html#traditionals)
- [TV, Movies and Videogames Themes](/ukulele/tabs.html#soundtracks)
- [Pop songs and riffs](/ukulele/tabs.html#pop)
- [Tips and Exercises](/ukulele/tabs.html#tips)
<hr>

Latest posts
--

<p style="text-align: right;float:right;margin-top:10px;margin-left:20px;"><a href="rss.xml"><i class="fa fa-rss fa-2x" >&nbsp;</i></a></p>
  
{% for post in site.posts limit:10 %}
    {% if post.categories contains 'ukulele' %}
 
 <li><span>{{ post.date | date: "%B %e, %Y" }}</span> &raquo; <a href="{{ BASE_PATH }}{{ post.url }}">{{ post.title }}</a></li>
 
    {% endif %}
{% endfor %}

<p style="text-align: right;font-size:1.5em;"> <a href="./archive.html">All posts...</a> </p>


Latest videos
--

<div class="video-container">
<iframe src="https://www.youtube.com/embed/?listType=user_uploads&list=andreafortuna" frameborder="0" allowfullscreen></iframe>
</div>



