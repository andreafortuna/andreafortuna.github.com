---
layout: page
title: My Weekly Roundup
description: "My weekly report of best news on the net about technology, programming, security, running, music, ukulele, movies and geekness"
thumbnail: "http://www.andreafortuna.org/weeklyroundup/images/roundup.png"
keywords: technology, security, programming, music, movie, geekness, ukulele
tagline: WeeklyRoundup
---
{% include JB/setup %}
«That's the press, baby. The press! And there's nothing you can do about it. Nothing!»
--
<p style="text-align: right;font-style: italic;"><strong>Ed Hutcheson</strong></p>

![Roundup](/weeklyroundup/images/roundup.png)

<hr/>
<p style="text-align: right;float:right;margin-top:10px;margin-left:20px;"><a href="rss.xml"><i class="fa fa-rss fa-4x" >&nbsp;</i></a></p>
<div class="blog-index">

{% for post in site.posts %}
    {% if post.categories contains 'weeklyroundup' %}
        {% assign content = post.content %}
        {% include post_detail.html %}
    {% endif %}
{% endfor %}

</div>


