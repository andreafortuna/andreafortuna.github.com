---
layout: page
title: My Weekly Roundup
description: "My weekly report of best news on the net about technology, programming, security, wellness, music, movies and geekness"
thumbnail: "http://www.andreafortuna.org/weeklyroundup/images/roundup.png"
keywords: technology, security, programming, music, movie, geekness, ukulele, guitar
tagline: WeeklyRoundup
---

![Roundup](/weeklyroundup/images/roundup.png)

«That's the press, baby. The press! And there's nothing you can do about it. Nothing!»
--
<p style="text-align: right;font-style: italic;"><strong>Ed Hutcheson</strong></p>

<hr/>

Every week i publish a list of links to resources and articles I read and found interesting.

<form  action="https://feedburner.google.com/fb/a/mailverify" method="post" target="popupwindow" onsubmit="window.open('https://feedburner.google.com/fb/a/mailverify?uri=andreafortuna/newsletter', 'popupwindow', 'scrollbars=yes,width=550,height=520');return true"><p>You may receive this report in your mailbox entering your email address:</p><p><input type="text" style="width:140px" name="email"/></p><input type="hidden" value="andreafortuna/newsletter" name="uri"/><input type="hidden" name="loc" value="en_US"/><input type="submit" value="Subscribe" /></form>
<hr/>
	
Latest posts
--

<p style="text-align: right;float:right;margin-top:10px;margin-left:20px;"><a href="rss.xml"><i class="fa fa-rss fa-4x" >&nbsp;</i></a></p>
<div class="blog-index">

{% for post in site.categories['WeeklyRoundup'] limit:4%}
        {% assign content = post.content %}
        {% include post_detail.html %}
{% endfor %}

<p style="text-align: right;font-size:1.5em;"> <a href="./archive/">Go to Archive</a> </p>

</div>

