---
layout: post
title: "VMWare AirWatch MDM Agent on rooted Android Devices: how to force the enrollment"
thumbnail: "http://www.andreafortuna.org/technology/images/airwatch.png"
description: "A short and simple procedure to force the enrollment of rooted Android devices on AirWatch MDM."
keywords: Security, VMWare, AirWatch, Android, BOYD, Xposed, unWatch
category: Technology
tags: 
- Security
- VMWare
- AirWatch
- Android
- BOYD
- Xposed


---
{% include JB/setup %}

The *BOYD* (Bring your own device) policy starts being a very common practice in a lot of company.

![AirWatch Compromised](/technology/images/airwatch_c.png)

The ability to access corporate resources from their device makes it much easier to work in mobility, but it introduces a great number of security issues.

To overcome these problems companies can require, to employees who want to use their device, to install agents that allow company to control the security settings and necessarily take action if the devices are lost or stolen.

One of the most common agent for android devices is the [AirWatch MDM](http://www.air-watch.com/solutions/android/), by *VMware*:

>AirWatch provides enterprise mobility management for Android with a single console to manage devices, email, applications, content, browsing and more. AirWatch offers same-day support for Android releases to enable our customers to take advantage of the latest technology and advancements. The AirWatch platform has best-in-class architecture that is highly scalable, secure and flexible to meet your global enterprise mobility initiatives.

<hr/>

A complete and integrated solution!
--

However, enrollment is usually blocked if the device  has root permissions enabled.

Understandable limitation, in the case of a normal user: the root permissions enabled introduces less control by the agent and the possibility of more security issues.

*Nevertheless, not always root permissions imply security problems*: 

**often the same vendors release devices on which can enable root without 'esoteric' procedures, and very often are essential for developers and skilled users.**

<hr/>

How to force enrollment?
--

Fortunately there is a simple and quick way to force the enrollment of the device with root permissions.

*Xposed framework* is required (I have already spoken about in [this post](http://www.andreafortuna.org/technology/2015/11/10/root-and-installing-xposed-on-vodafone-smart-prime-6/)): just install *[unWatch](http://forum.xda-developers.com/xposed/modules/app-unwatch-root-support-airwatch-t3183082){:target="_blank"}*, a great module developed by [digitalhigh](http://forum.xda-developers.com/member.php?u=3400685){:target="_blank"}, a member of the [XDA forum](http://forum.xda-developers.com/){:target="_blank"}.

![unWatch](/technology/images/unWatch.png)

Activate the module from *Xposed Installer*, restart the device and...enroll!

![AirWatch Ok](/technology/images/airwatch.png)