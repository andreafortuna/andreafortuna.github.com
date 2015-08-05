---
layout: post
title: "Windows 10: enable right click with two fingers tap on Synaptics touchpad"
description: "After upgrading to Windows 10, the touchpad of my Lenovo 50-45 has lost a feature in my opinion very useful: the right click with the two-fingers tap."
thumbnail: "http://www.andreafortuna.org/technology/images/lenovo-g50-45.png"
keywords: Windows 10, Issues, Synaptics, Touchpad, Two Fingers, Right Click
category: Microsoft
tags: 
- Microsoft
- Windows 10
- Synaptics

---
{% include JB/setup %}


After upgrading to *Windows 10*, the touchpad of my *Lenovo 50-45* has lost a feature in my opinion very useful: the right click with the two-fingers tap.

![WUDO](/technology/images/lenovo-g50-45.png)
<!-- more -->

In the new settings interface of the Synaptics driver, there is no option to enable this feature.
However, is still possible enable this from the system registry:

1. Open *Registry Editor* (Windows + R, type *regedit* and hit *Enter*)
2. Navigate to *HKEY_CURRENT_USER\SOFTWARE\Synaptics\SynTP\TouchPadPS2TM28xx*
3. Change the value of *2FingerTapAction* to *2*

![regedit](/technology/images/Synaptics2fingertap.PNG)

4. Logoff or Restart

That's all!