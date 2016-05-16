---
layout: post
title: "KeRanger, the first OSX ransomware comes bundled into Transmission installer"
thumbnail: "http://oldsite.andreafortuna.org/security/images/transmission.png"
description: "Security researchers from Palo Alto Networks claims to have discovered the first OSX Ransomware, called 'KeRanger'."
keywords: Security, Threat, OSX, Apple, Palo Alto Networks, KeRanger, Transmission, ransomware, malware
category: Security
tags: 
- Security
- Threats
- Ransomware
- Apple

---

Security researchers from *Palo Alto Networks* claims to [have discovered](http://researchcenter.paloaltonetworks.com/2016/03/new-os-x-ransomware-keranger-infected-transmission-bittorrent-client-installer/) the first *OSX Ransomware*, called *KeRanger*.

The *ransomware* comes bundled into the popular Mac app [Transmission](), a BitTorrent client with a lot of users.

![transmission](http://oldsite.andreafortuna.org/security/images/transmission.png)

Technical analisys
--

From [Palo Alto Networks](http://researchcenter.paloaltonetworks.com/2016/03/new-os-x-ransomware-keranger-infected-transmission-bittorrent-client-installer/):

>The two KeRanger infected Transmission installers were signed with a legitimate certificate issued by Apple.

>The KeRanger infected Transmission installers include an extra file named General.rtf in the Transmission.app/Contents/Resources directory. It uses an icon that looks like a normal RTF file but is actually a Mach-O format executable file packed with UPX 3.91. When users click these infected apps, their bundle executable Transmission.app/Content/MacOS/Transmission will copy this General.rtf file to ~/Library/kernel_service and execute this “kernel_service” before any user interface appearing.

>After unpacking the General.rtf with UPX, we determined that its main behavior is to encrypt the user’s files and hold them for ransom.

How protect?
--
*Apple* has since revoked the abused certificate, and *Gatekeeper* will now block the malicious installers. 

*Apple* has also updated *XProtect* signatures to cover the family, and the signature has been automatically updated to all *Mac* now. 

As of *March 5*, [Transmission Project](https://www.transmissionbt.com/) has removed the malicious installers from its website.
