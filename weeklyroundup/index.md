---
layout: page
title: My Weekly Roundup
description: "Ukulele transcriptions, tutorials, videos"
thumbnail: "http://www.andreafortuna.org/ukulele/images/ukulele2.jpg"
tagline: Ukulele
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


