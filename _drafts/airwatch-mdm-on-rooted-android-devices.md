---
layout: post
title: "Using VMWare AirWatch MDM Agent on rooted Android Devices"
thumbnail: ""
description: ""
keywords: Security, VMWare, AirWatch, Android, BOYD
category: Security
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

![XXX](/xxx)

The ability to access corporate resources from their device makes it much easier to work in mobility, but it introduces a great number of security issues.

To overcome these problems companies can require, to employees who want to use their device, to install agents that allow company to control the security settings and necessarily take action if the devices are lost or stolen.To

One of the most common agent for android devices is the [AirWatch MDM](http://www.air-watch.com/solutions/android/), by VMware:

>AirWatch provides enterprise mobility management for Android with a single console to manage devices, email, applications, content, browsing and more. AirWatch offers same-day support for Android releases to enable our customers to take advantage of the latest technology and advancements. The AirWatch platform has best-in-class architecture that is highly scalable, secure and flexible to meet your global enterprise mobility initiatives.

A complete, integrated solution! 

However, enrollment is usually blocked if the device  has root permissions enabled.

Understandable limitation, in the case of a normal user: the root permissions enabled introduces less control by the agent and the possibility of more security issues.

