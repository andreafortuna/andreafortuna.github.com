---
layout: post
title: "Windows 10: uninstall all modern apps with a single Powershell command"
description: "I have already explained how to uninstall a Metro/Modern app using Powershell on Windows 8, but some readers ask me how to 'clean' the new Windows 10 from all pre-installed Apps."
thumbnail: "http://www.andreafortuna.org/technology/images/ModernApps.PNG"
keywords: Windows 10, modern, apps, powershell, tips
category: Microsoft
tags: 
- Microsoft
- Windows 10
- Powershell

---
{% include JB/setup %}
I have [already explained](http://www.andreafortuna.org/windows/2014/11/17/windows-8-1-uninstall-metro-apps-with-powershell/) how to uninstall a Metro/Modern app using Powershell on Windows 8, but some readers ask me how to 'clean' the new Windows 10 from all pre-installed Apps.

![Apps](/technology/images/ModernApps.PNG)
<!-- more -->


The solution is simple and fast:

1. Press the "Win" key on the keyboard and type "Powershell"
2. When it comes up in the search results, right click on it and choose "Run as administrator".
![](/technology/images/powershell.png)
3. Type the following commands in the Powershell window:
*Get-AppXProvisionedPackage -online | Remove-AppxProvisionedPackage -online* (to remove all Modern apps for new users)
and
*Get-AppXPackage | Remove-AppxPackage* (to remove apps from current user account)

Some apps cannot be uninstalled: Store, Edge, Windows Feedback, Settings,Contact Support, Cortana, Photos.

That's all!