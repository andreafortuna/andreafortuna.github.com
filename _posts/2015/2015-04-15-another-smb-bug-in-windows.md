---
layout: post
title: "'Redirect to SMB': an old Windows bug that back in the spotlight"
description: "A very old Windows bug back in the spotlight"
category: Security
tags: 
- Security
- Windows
- Microsoft
- Cylance

---
{% include JB/setup %}
[Cylance](http://cylance.com/) has discovered a 'new' vulnerability in Windows, a weakness that was never patched by Microsoft.


![Cylance1](http://cdn2.hubspot.net/hubfs/270968/SPEAR_blogs/RedirectToSMB/RedirectToSMB-Diagram-1.png?t=1429022094769)
<!-- more -->

The bug, called "Redirect to SMB," is a variant of a vulnerability found in Windows by  Aaron Spangler  18 years ago: this cause the exposition of  a user's Windows username and password.

From [Cylance website](http://blog.cylance.com/redirect-to-smb):

>*Redirect to SMB* is a way for attackers to steal valuable user credentials by hijacking communications with legitimate web servers via man-in-the-middle attacks, then sending them to malicious SMB (server message block) servers that force them to spit out the victim’s username, domain and hashed password.

and about the *original vulnerability*:

>The Redirect to SMB attack builds on a vulnerability discovered in 1997 by Aaron Spangler, who found that supplying URLs beginning with the word “file” (such as file://1.1.1.1/) to Internet Explorer  would cause the operating system to attempt to authenticate with a SMB server at the IP address 1.1.1.1. 

Affected applications?
---

In his [white paper](http://cta-redirect.hubspot.com/cta/redirect/270968/ffdef579-934a-4f0f-9ed0-f9e528449d84), Cylance says that are 31 applications vulnerable to this flaw:

*Widely Used Applications:*

- Adobe Reader
- Apple QuickTime
- Apple Software Update (which handles the updating for iTunes)

*Microsoft Applications:*

- Internet Explorer
- Windows Media Player
- Excel 2010, and even in Microsoft Baseline Security Analyzer

*Antivirus:*

- Symantec’s Norton Security Scan
- VG Free
- BitDefender Free
- Comodo Antivirus

*Security Tools:*

- .NET Reflector
- Maltego CE

*Team Tools:*

- Box Sync
- TeamViewer

*Developer Tools:* 

- Github for Windows
- PyCharm
- IntelliJ IDEA
- PHP Storm
- JDK 8u31’s installer


<iframe width="560" height="315" src="https://www.youtube.com/embed/QNE6T91XZfk" frameborder="0" allowfullscreen></iframe>


How do you protect yourself?
---
- Block outbound traffic from TCP 139 and TCP 445. 
- Apply applicable and up-to-date software patches from vendors.
- Use strong passwords so that it requires a larger time for brute forcing of any hashing algorithms.