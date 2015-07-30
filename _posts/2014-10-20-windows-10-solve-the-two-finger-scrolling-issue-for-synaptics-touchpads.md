---
layout: post
title: "Windows 10: fix 'two-finger scrolling' issue for Synaptics touchpads"
description: "Windows 10: fix 'two-finger scrolling' issue for Synaptics touchpads"
category: Microsoft
keywords: Windows 10, Microsoft, Synaptics, Lenovo
tags: 
- Windows 10
- Touchpad
- Synaptics
---
{% include JB/setup %}

*UPDATE: With the latest builds of Windows 10 you can install the updated Synaptics drivers  through Windows Update , which no longer requires this procedure.* 

<hr/>

I'm testing the **Windows 10** *Technical preview*: i find some problems, but the new microsoft's OS is light and stable.

However, on my *Lenovo* notebook with *Synaptics* touchpad the "two-finger scroll" (osx-like, very useful) seems not work.

![](http://www.lenovo.com/images/gallery/main/lenovo-laptop-ideapad-z500-touch-closeup-touchpad-4.jpg)

<!-- more -->

After a quick search on support forums, i have found a very simple solution:

1. Open Registry Editor (Windows + R, type *regedit* and hit *Enter*)
2. Navigate to HKEY_LOCAL_MACHINE\SOFTWARE\Synaptics\SynTPEnh
3. Create a new **DWORD** called **UseScrollCursor** with a value of **0**.
4. Logoff or Restart

That's all!

<hr/>
*Other posts about Windows 10 issues:*

- [Windows 10: missing MIDI wavetable?](/microsoft/2015/07/30/windows-10-missing-midi-wavetable/)
<hr/>