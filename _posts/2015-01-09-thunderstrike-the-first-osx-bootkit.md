---
layout: post
title: "Thunderstrike, the first OSX bootkit"
description: "Thunderstrike, infect OSX through thunderbolt"
category: Security
tags: 
- OSX
- Thunderstrike
---
{% include JB/setup %}

![Thunderstrike](https://farm9.static.flickr.com/8576/15519086824_abf2dc26bd.jpg)

**Trammel Hudson** gave a [talk](https://trmm.net/Thunderstrike_31c3#Summary) at the recent [31C3](http://events.ccc.de/congress/2014/wiki/Static:Main_Page) event in Hamburg, Germany, during which he described an attack called **Thunderstrike**, a *OSX bootkit* delivered either through direct access to the Apple hardware or via a thunderbolt-connected peripheral device.

<!-- more -->

The original Hudson's article is available at [this link](https://trmm.net/Thunderstrike_31c3), and a simple analysis is provided by [ThreatPost](http://threatpost.com/first-public-mac-os-x-firmware-bootkit-unleashed/110287):

>The end result is the installation of malicious firmware on an Apple machine that would survive reinstallation of OS X or replacement of the Solid State Drive (SSD). Thunderstrike is undetectable, Hudson said, and can be used for root access to an infected computer, putting all of its data and web traffic at risk for interception and monitoring.

and

>Hudson’s bootkit takes advantage of a vulnerability in how Apple computers deal with peripheral devices connected over Thunderbolt ports during a firmware update. In these cases, the flash is left unlocked, allowing an Option ROM, or peripheral firmware, to run during recovery mode boots. It then has to slip past Apple’s RSA signature check. Apple stores its public key in the boot ROM and signs firmware updates with its private key. The Option ROM over Thunderbolt circumvents this process and writes its own RSA key so that future updates can only be signed by the attacker’s key. The attack also disables the loading of further Option ROMs, closing that window of opportunity. A weaponized version of this attack would have free ring0 reign over the system.

![Thunderstrike details](https://farm8.static.flickr.com/7578/16141422325_56ea9c46f0.jpg)

How do we prevent Thunderstrike?
--
Hudson says:
>Apple has a partial fix that they have started shipping in the new Mac Mini's and iMac Retinas, and they plan to release it for older Macs soon as a firmware update. Their fix is to not load Option ROMs during firmware updates, which is effective against the current proof-of-concept.

but

>However... it is not a complete fix. Option ROMs are still loaded on normal boots, allowing snare's 2012 attack to continue working. Older Macs are subject to downgrade attacks by "updating" to a vulnerable firmware version.

Dark Jedi?
--
Thunderstrike could also eventually be done remotely using the **Dark Jedi attack**.

Dark Jedi attack is an exploit [presented at 31C3](http://events.ccc.de/congress/2014/Fahrplan/events/6129.html) by Corey Kallenberg and Rafal Wojtczuk. 
Their talk exposed vulnerabilities in UEFI that allows an attacker to re-flash firmware and run their own malicious firmware.

More informations on [Thunderstrike FAQ's page](https://trmm.net/Thunderstrike_FAQ) on [Hudson's website](https://trmm.net/).
