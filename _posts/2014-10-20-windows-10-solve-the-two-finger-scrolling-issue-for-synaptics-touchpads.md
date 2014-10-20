---
layout: post
title: "Windows 10: fix 'two-finger scrolling' issue for Synaptics touchpads"
description: ""
category: Microsoft
tags: 
- Windows 10
- Touchpad
- Synaptics
---
{% include JB/setup %}
I'm testing the **Windows 10** *Technical preview*: i find some problems, but the new microsoft's OS is light and stable.

However, on my *Lenovo* notebook with *Synaptics* touchpad the "two-finger scroll" (osx-like, very useful) seems not work.

![](http://www.lenovo.com/images/gallery/main/lenovo-laptop-ideapad-z500-touch-closeup-touchpad-4.jpg)

<!-- more -->

After a quick search on support forums, i have found a very simple solution:

*  Open Registry Editor (Windows + R, type *regedit* and hit *Enter*)
*  Navigate to HKEY_LOCAL_MACHINE\SOFTWARE\Synaptics\SynTPEnh
*  Create a new **DWORD** called **UseScrollCursor** with a value of **0**.
*  Logoff or Restart

That's all!