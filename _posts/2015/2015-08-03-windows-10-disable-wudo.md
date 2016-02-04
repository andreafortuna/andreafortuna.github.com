---
layout: post
title: "Windows 10: how to disable Windows Update Delivery Optimization (WUDO)"
description: "Windows 10 introduced a new feature, called Windows Update Delivery Optimization (WUDO), initially designed to help users get faster software updates."
thumbnail: "http://www.andreafortuna.org/technology/images/WUDO_detail.png"
keywords: Windows 10, Issues, WUDO, peer-to-peer, Windows Update
category: Microsoft
tags: 
- Microsoft
- Windows 10
- WUDO

---
{% include JB/setup %}


*Windows 10* introduced a new feature, called *Windows Update Delivery Optimization* (WUDO), initially designed to help users get faster software updates.

![WUDO](/technology/images/WUDO_detail.png)
<!-- more -->

*Windows Update Delivery Optimization* works like a torrent node: your computer is used as part of a peer-to-peer network to deliver software updates faster to others.

Each computer distributes a part of the files across multiple systems and helps everyone to download updates more faster.

However, this *peer-to-peer* method uses your bandwidth, and the feature is enabled by default in Windows 10.

Here the steps to disable this feature:

1. Open *Settings* in the Start menu
2. Search for *Update & Security*
3. In the *Windows Update* section, open *Advanced Options*
4. In the *Choose How Updates are Installed* section, open *Choose how updates are delivered*
5. Now disable the toggle *Updated from More than One Place*

![WUDO](/technology/images/WUDO.png)

