---
layout: post
title: "Three new Android vulnerabilities, one remote"
description: "Three new Android vulnerabilities, one remote"
category: Security
tags: 
- Android
---
{% include JB/setup %}

Yesterday on [PacketStorm](http://packetstormsecurity.com/) were published advisories for three newly discovered vulnerabilities on Android, in versions prior to Lollipop (5.0): one of these allows  to be exploited by remote.

![Android Exploits](http://www.maximumpc.com/files/android_sick_3.jpg)

<!-- more -->

* [Android Settings Pendingintent Leak](http://packetstormsecurity.com/files/129281/android-appleak.txt)

>In Android <5.0 (and maybe >= 4.0), Settings application leaks Pendingintent with a blank base intent (neither the component nor the action is explicitly set) to third party application, bad app can use this to broadcast intent with the same permissions and identity of the Settings application, which runs as SYSTEM uid.

* [Android WAPPushManager SQL Injection](http://packetstormsecurity.com/files/129283/androidwappushmanager-sql.txt)

>In Android <5.0, a SQL injection vulnerability exists in the opt module WAPPushManager, attacker can remotely send malformed WAPPush message to launch any activity or service in the victim's phone

* [Android SMS Resend](http://packetstormsecurity.com/files/129282/android-smsresend.txt)

>In Android <5.0, an unprivileged app can resend all the SMS stored in the user's phone to their corresponding recipients or senders (without user interaction).
