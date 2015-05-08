---
layout: page
title: Ukulele stuff
tagline: Ukulele
---
{% include JB/setup %}

![My Ukulele](/images/ukulele.jpg)

Coming soon!
---
 
<div class="blog-index">

{% for post in site.posts %}
    {% if post.categories contains 'ukulele' %}
        {% assign content = post.content %}
        {% include post_detail.html %}
    {% endif %}
{% endfor %}

</div>


