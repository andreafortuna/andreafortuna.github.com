---
layout: post
title: "Windows 10: generate a battery report"
description: "When Windows 10 is running on a tablet or a laptop, one of the aspects to be checked periodically is the battery life."
thumbnail: "http://oldsite.andreafortuna.org/technology/images/battery.png"
keywords: Windows 10, battery, report, tablet, laptop, UAC
category: Microsoft
tags: 
- Microsoft
- Windows 10
- Battery

---
{% include JB/setup %}


When *Windows 10* is running on a tablet or a laptop, one of the aspects to be checked periodically is the battery life.

![Battery Report](/technology/images/battery.png)
<!-- more -->

Check the estimated battery life is very simple: just click the icon in the taskbar.
However, the value indicates an estimate and not the actual life of the battery. 

Let's see how to generate a report of the actual battery life in Windows 10:

1. Type in the search box "cmd", click with the right mouse button and select "Run as administrator"
2. Click Yes to the *UAC* prompt
3. Paste in the the command prompt window  the following string: *powercfg /batteryreport /output C:\battery_report.html*
4. Go to C:\ and open the *battery_report.html* file.

That's all! 