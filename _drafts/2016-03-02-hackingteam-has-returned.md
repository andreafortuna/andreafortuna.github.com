---
layout: post
title: "Undetected Mac malware sighted online: HackingTeam has returned?"
thumbnail: "http://www.andreafortuna.org/security/images/HackingTeam.png"
description: "Researchers have uncovered a malicious tool that appears to be a newly developed Mac malware from HackingTeam, the first since the hack of last July that leaked gigabytes of the group's private e-mail and source code."
keywords: Security, Threat, Mac, Apple, HackingTeam, 2ee9e9d9a0cd3cee6519e7b950821d5c90af03da665879615e52fd093dd8e947
category: Security
tags: 
- Security
- Threats
- Vulnerability
- HackingTeam
- Apple

---

Researchers have uncovered a malicious tool that appears to be a newly developed Mac malware from *HackingTeam*, the first since the hack of last July that leaked gigabytes of the group's private e-mail and source code.

The sample was uploaded on *February 4* to the [Google-owned VirusTotal scanning service](https://www.virustotal.com/it/file/2ee9e9d9a0cd3cee6519e7b950821d5c90af03da665879615e52fd093dd8e947/analysis/){:target="_blank"}, which at the time showed it wasn't detected by any of the major antivirus programs. 

![VirusTotal](https://reverse.put.as/wp-content/uploads/2016/02/zip_vt_submission.png)

Some technical information
--

![reverse](https://reverse.put.as/wp-content/uploads/2016/02/keypress_packer.png)

A [technical analysis](https://reverse.put.as/2016/02/29/the-italian-morons-are-back-what-are-they-up-to-this-time/){:target="_blank"} published Monday morning by *SentinelOne* showed that the installer was last updated in October or November, and an embedded encryption key is dated October 16, three months after the HackingTeam compromise:

>Last Friday a new OS X RCS sample was sent to me (big thanks to @claud_xiao from Palo Alto Networks for the original discovery, and as usual to @noarfromspace for forwarding it to me). My expectations weren’t big since all the public samples were rather old and know we had their source code so if it were an old sample it was totally uninteresting to analyse. But contrary to my expectations there are some interesting details on this sample. So let’s start once more our reverse engineering journey…

<hr/>

How i check if my computer has been infected?
--

![check](https://objective-see.com/images/blog/blog_0x0D/knockknock.png)

Another very good technical analysis was published by [Patrick Wardle](https://objective-see.com/blog/blog_0x0D.html){:target="_blank"}, that has examined the malware and says that it appears to install a new version of the old Hacking Team implant and it uses several advanced tricks to evade detection and analysis.

*Wardle* suggest also a fast method to check if your system has been infected:

To *check if you are infected*, simply look for the following directory: ```~/Library/Preferences/8pHbqThW/``` containing ```_9g4cBUb.psr``` and/or ```Bs-V7qIU.cYL```. 

To *disinfect yourself*, delete that entire directory, and remove the ```~/Library/LaunchAgents/com.apple.FinderExtAvt.plist``` file. 
Of course if you really are infected - throw out your computer and get a new one! 




