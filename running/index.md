---
layout: page
title: My Running Chronicles
tagline: Running
---
{% include JB/setup %}

![Homer on the couch](/images/homer.png)

«Pain is inevitable. Suffering is optional.»
--
<p style="text-align: right;font-style: italic;"><strong>Haruki Murakami</strong></p>

<hr/>

In June 2012, my life changed: after 34 years spent on the couch, I decided to start doing something for my body and start doing exercise.

I wore the first pair of sneakers that I found in the house, I went out to run and since that day I have not stopped more!
 
<hr/>

<div class="blog-index">

{% for post in site.posts %}
    {% if post.categories contains 'running' %}
        {% assign content = post.content %}
        {% include post_detail.html %}
    {% endif %}
{% endfor %}

</div>


