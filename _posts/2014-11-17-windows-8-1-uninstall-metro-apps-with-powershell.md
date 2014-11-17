---
layout: post
title: "Windows Tips: Completely Uninstall Metro Apps From Windows 8/8.1/10 with PowerShell"
description: "Windows Tips: Completely Uninstall Metro Apps From Windows 8/8.1/10 with PowerShell"
category: Windows
tags: 
- Windows
- Tips
---
{% include JB/setup %}
When you uninstall a **Windows Store App** from usual options, the app is removed temporarily and goes to a "staged condition":  the app still lies in Windows and is prepared to get automatic installation when a new user account is created.

![App Uninstall](http://images.gizmag.com/inline/annoyingmetro81-4.png)

<!-- more -->

To completely remove the app, you must be signed in as Administrator of you Windows Account – and you need to remove it in two places:

1. Remove the provisioned package
2. Remove the "installed" package from the administrator account.

How?
---
1. Open a PowerShell session with administrator privileges
2. In the PowerShell you can get a list of installed apps with this command:
```
Get-AppxPackage -AllUsers
```
3. With the correct name of the app package (**PackageFullName**), you can uninstall the provisioned package with this command:
```
Remove-AppxProvisionedPackage -package PACKAGENAME
```
4. ...and the installed package with
```
Remove-AppxPackage PACKAGENAME
```
