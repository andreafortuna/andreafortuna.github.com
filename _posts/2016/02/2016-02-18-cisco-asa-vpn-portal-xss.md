---
layout: post
title: "Cisco ASA VPN Portal Cross Site Scripting, 0Day"
thumbnail: "http://oldsite.andreafortuna.org/technology/images/CiscoASA.jpg"
description: "After the vulnerability in the fragmentation of the IKE payload, a new zero-day afflicts the Cisco ASA VPN Portal."
keywords: Security, Threat, Cisco, 0Day, XSS, Cross Site Scripting
category: Security
tags: 
- Security
- Threats
- Vulnerability
- 0Day
- Cisco
- XSS


---
{% include JB/setup %}

Recently there is no peace for the *Cisco ASA Appliance*.

After the vulnerability in the [fragmentation of the IKE payload](https://tools.cisco.com/security/center/content/CiscoSecurityAdvisory/cisco-sa-20160210-asa-ike), a new zero-day afflicts the *Cisco ASA VPN Portal* through *XSS* attack.

![CiscoASAVpnPortal](/technology/images/CiscoASA.jpg)

From the [advisory](https://packetstormsecurity.com/files/135813/ciscoasavpnportal-xss.txt) posted by *Juan Sacco* on [PacketStorm](https://packetstormsecurity.com/):

> Cisco ASA VPN is prone to a XSS on the password recovery page.

> This vulnerability can be used by an attacker to capture other user's credentials.

> The password recovery form fails to filter properly the hidden inputs fields.

Here a simple *Proof-Of-Concept* to check the vulnerability:

<script src="https://gist.github.com/andreafortuna/f2f79ab8def1f0e37ae6.js"></script>


