---
layout: post
title: "Skype: the eight-characters of death!"
description: "This eight-character message causes Skype to endlessly crash"
category: Security
tags: 
- Security
- Skype
- Crash

---
{% include JB/setup %}
Not only [iOS is affected by annoying bugs](http://oldsite.andreafortuna.org/security/2015/05/29/ios-imessage-crash/) (and stupid) that cause crashes and reboots with the simple insertion of a sequence of characters.

![SkypeCrash](http://venturebeat.com/wp-content/uploads/2015/06/skype_bug_autocrash.png)
<!-- more -->

Today is the turn of Skype: users have discovered that sending the characters "http://:" (without the quotes) crashes Skype (also receiving a message with those characters), and makes it crash any time you try to sign in again.

The bug works on *Windows*, *Android*, and *iOS*. 
It seem to have no effect on Skype for Mac and Skype for modern Windows.

[Venturebeat.com](http://venturebeat.com/2015/06/02/these-8-characters-crash-skype-and-once-theyre-in-your-chat-history-the-app-cant-start/) asked to Skype a confirm:

>**Update**: Skype has confirmed the bug. "We are aware of the problem and are working to provide an resolution" a Skype spokesperson told VentureBeat.

<hr/>

<a name="update">**UPDATE**</a>

Reddit user [yorkshireale](http://www.reddit.com/user/yorkshireale) tells me:

>This has already been fixed with the latest update to Skype.