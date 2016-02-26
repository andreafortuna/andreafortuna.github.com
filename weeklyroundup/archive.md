---
layout: page
title: My Weekly Roundup
description: "My weekly report of best news on the net about technology, programming, security, wellness, music, movies and geekness"
thumbnail: "http://www.andreafortuna.org/weeklyroundup/images/roundup.png"
keywords: technology, security, programming, music, movie, geekness, ukulele, guitar
tagline: WeeklyRoundup
---

![My Ukulele](/ukulele/images/ukulele2.jpg)

<p style="text-align: right;float:right;margin-top:10px;margin-left:20px;"><a href="/ukulele/rss.xml"><i class="fa fa-rss fa-4x" >&nbsp;</i></a></p>
<div class="blog-index">

{% for post in site.categories['WeeklyRoundup'] }
        {% assign content = post.content %}
        {% include post_detail.html %}
{% endfor %}

</div>


