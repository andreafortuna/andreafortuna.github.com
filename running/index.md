---
layout: page
title: My Running Chronicles
tagline: Running
---
{% include JB/setup %}

«Pain is inevitable. Suffering is optional.»
--
<p style="text-align: right;font-style: italic;"><strong>Haruki Murakami</strong></p>

![Homer on the couch](/images/homer.png)

<hr/>

In June 2012, my life changed: after 34 years spent on the couch, I decided to start doing something for my body and start doing exercise.

I wore the first pair of sneakers that I found in the house, I went out to run and since that day I have not stopped more!
 
<hr/>
<p style="text-align: right;float:right;margin-top:10px;margin-left:20px;"><a href="rss.xml"><i class="fa fa-rss fa-4x" >&nbsp;</i></a></p>
<div class="blog-index">

{% for post in site.posts %}
    {% if post.categories contains 'running' %}
        {% assign content = post.content %}
        {% include post_detail.html %}
    {% endif %}
{% endfor %}

</div>


