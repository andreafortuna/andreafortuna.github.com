---
layout: post
title: "OneClick PayPal Hacking?"
description: "Hacking PayPal Accounts with one click"
category: Security
tags:
- Paypal
- Exploits
---
{% include JB/setup %}

[Yasser H. Ali](http://yasserali.com/), an Egyptian security researcher, has discovered three critical vulnerabilities in PayPal website which could be used to take control of customer accounts.

![PayPalHacking](http://yasserali.com/wp-content/uploads/2014/10/Screen-Shot-2014-08-13-at-12.20.52-AM.png)
<!-- more -->
Yasser explain in [this post](http://yasserali.com/hacking-paypal-accounts-with-one-click/) the three vulnerabilities used to breach into accounts:

1. Reusable CSRF Token

>The CSRF token “that authenticate every single request made by the user” which can be also found in the request body of every request with the parameter name “Auth” get changed with every request made by user for security measures, but after a deep investigation I found out that the CSRF Auth is Reusable for that specific user email address or username, this means If an attacker found any of these CSRF Tokens, He can then make actions in the behave of any logged in user.

2. Bypassing the CSRF Auth System

>The CSRF Auth verifies every single request of that user, So what If an attacker "not logged in" tries to make a "send money" request then PayPal will ask the attacker to provide his email and password, The attacker will provide the “Victim Email” and ANY password, Then he will capture the request, The request will contain a Valid CSRF Auth token Which is Reusable and Can authorise this specific user requests. 

3. Bypassing the Security Questions Change

>[...] the request of setting up the security questions “which is initiated by the user while signing up” is not password-protected, and it can be reused to reset the security questions up without providing the password, hence, Armed with the CSRF Auth, an attacker can CSRF this process too and change the victim’s Security questions.

Here is the Proof Of Concept video:

<iframe width="420" height="315" src="//www.youtube.com/embed/KoFFayw58ZQ" frameborder="0" allowfullscreen></iframe>
