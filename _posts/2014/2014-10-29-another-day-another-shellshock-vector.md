---
layout: post
title: "Another day, another ShellShock vector: today is the turn of the SMTP"
description: "Another ShellShock attack vector: SMTP!"
category: Security
tags: 
- ShellShock
- SMTP
---
{% include JB/setup %}
[SANS Internet Storm Center](https://isc.sans.edu/diary/Shellshock+via+SMTP/18879) announced that some web hosting providers reports a strange activity  that appears to be a [*shellshock*](http://oldsite.andreafortuna.org/tags.html#ShellShock-ref) exploit attempt via SMTP.

![Remote code execution](http://cdn.zdnet.be/thumb/600-600/i/2014/44/shutterstock_222964006.jpg)

<!-- more -->

[*The Register*](http://www.theregister.co.uk/2014/10/28/shellshocked_via_email_smtp_attacks_on_the_rise/) jokes about this news:

>**Shellshock over SMTP attacks mean you can now ignore your email**

>*'But boss, the Internet Storm Centre says it's dangerous for me to reply to you'*

Attackers are using Shellshock exploits in order to drop a perl script onto compromised computers. 

The script adds the hacked servers to a botnet that receives its commands over IRC, said [Binary Defense Systems](https://www.binarydefense.com/bds/active-shellshock-smtp-botnet-campaign/): 

>We recently became aware of a SMTP botnet campaign occurring for a number of large-scale customers targeting SMTP gateways with Shellshock based attacks. 

>The attack leverages **Shellshock** as a main attack vector through the subject, body, to, from fields (targets every main header field in order to download the perl botnet script).

The payload is an IRC perl bot with simple DDoS commands and the ability to fetch and execute further code.

Watch out and...**update your bash**!
