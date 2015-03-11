---
layout: post
title: "Reconnect, a Facebook hacking tool"
description: "Hacking Facebook Account with 'Reconnect' Tool"
category: Security
tags: 
- Facebook
- Security
- Reconnect
- Hacking
- Sakurity
- Egor Homakov
- CSRF

---
{% include JB/setup %}

Egor Homakov, a security researcher of penetration testing company "[Sakurity](http://sakurity.com/)", has discovered a vulnerability that allows malicious hackers take over Facebook accounts on websites that use the 'Login with Facebook' feature.

![ReConnect](http://sakurity.com/img/reconnect.png)
<!-- more -->

The flaw doesn't allow hackers access to the Facebook's password, but it does allow them to access your accounts using a Facebook application developed by third-party websites.

Homakov has published a [blog post](http://sakurity.com/blog/2015/03/05/RECONNECT.html) with more information about the CSRF (Cross-Site Request Forgery) vulnerability and a simple tool, called ["Reconnect"](http://sakurity.com/reconnect) to exploit the flaw:

>RECONNECT is a ready to use tool to hijack accounts on websites with Facebook Login, for example Booking.com, Bit.ly, About.me, Stumbleupon, Angel.co, Mashable.com, Vimeo and many others. Feel free to copy and modify its source code. Facebook refused to fix this issue one year ago, unfortunately it’s time to take it to the next level and give blackhats this simple tool. 

What is Cross-Site Request Forgery (CSRF)?
---
Can help us [RedTeam Security Consulting](http://www.redteamsecure.com/labs/post/66/Demystifying-Cross-Site-Request-Forgery):

>A cross-site request forgery attack is a type of malicious attack that forces an end-user to execute an unwanted action, without his/her knowledge on behalf of the attacker, within a web application in which the end-user is currently authenticated.
In essence, the end-user (victim) is often tricked into clicking on a link, perhaps inside an email sent from the attacker posing as another party, that will perform a function within the website where the end-user is already authenticated. CSRF attacks generally target functions within websites that are considered “high value,” such as areas of websites that allow users to change passwords, transfer money, change an email address or purchase something.

![Cross-Site Request Forgery](http://www.redteamsecure.com/images/labs/csrf.png)

How to protect yourself?
---
Quoting an article by [TheHackersNews.com](http://thehackernews.com/2015/03/facebook-hacking-tool.html):

> One could realize the dangerous consequences of RECONNECT Facebook hacking tool by calculating how many number of websites over Internet use that blue color ' f ' button of Facebook login. And once a hacker makes a way to get into you account, they could access your private information and use them to hack into your other online accounts.
So, in order to prevent your accounts from malicious hackers, Do Not click on any suspicious URLs provided to you via online messages, emails or social media accounts. And always be careful while surfing over the Internet.
