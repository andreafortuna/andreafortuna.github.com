---
layout: post
title: "Mazar BOT spoofing campaign in Denmark and Italy"
thumbnail: "http://www.andreafortuna.org/technology/images/MazarBOT.png"
description: "A new Mazar BOT campaign is currently targeting Android users in Denmark and Italy. Attackers are spoofing trustworthy organizations to infected Android smartphones."
keywords: Security, Threat, Android, MazarBOT, PEBKAC, TOR, SMS, Heimdal Security, Italy, Denmark
category: Security
tags: 
- Security
- Threats
- Vulnerability
- Android
- MazarBOT
- Tor
- Malware
- SMS

---

The announcement was given by [Heimdal Security on his blog](https://heimdalsecurity.com/blog/security-alert-new-android-malware-post-denmark/):

> This new campaign aims to spread the Mazar BOT malware that sprawled across Europe and beyond earlier this year, in February 2016. The change is that, this time, the code is obfuscated and it’s a lot more difficult to analyze. The cyber criminals who created Mazar BOT must have learnt from previous campaigns and wanted to make it even more challenging for law enforcement and cyber security specialists to dissect the malicious code.

> So far, this new Mazar BOT campaign has infected almost 400 Android devices in **Denmark** and 1500 in **Italy**.

![MazarBOT](http://www.andreafortuna.org/technology/images/MazarBOT.png)

<hr/>

I already wrote a [post dedicated to Mazar BOT](http://www.andreafortuna.org/security/2016/02/16/mazar-bot-root-and-erase-android-devices/), I recommend you give it a look:

> Once installed, the malware retrieves,unpacks and runs the TOR application, which will then be used to connect to a .onion server in the darkweb (http://pc35hiptpcwqezgs.Onion) and after sends an automated SMS to the number 9876543210 (+98 is the country code for Iran) with the text message: “Thank you”.

> The catch is that this SMS also includes the device’s location data.

> Mazar BOT would seem to be the first Android malware with the ability to remain covert by using TOR to hide its communication.

<hr>

In **Denmark**, potential victims are receiving the **SMS** below:

![SMS](https://heimdalsecurity.com/blog/wp-content/uploads/new-android-malware-post-denmark-1.png)

(*Your package is available for pick up. Follow link to see all the information on your package:*)

Once clicked, the shortened link leads to **www.fhsinsaat.com/apk/post.apk**, which downloads an Android app installation file onto the victim’s smartphone.

<hr>

How to protect yourself?
--

The advices are the same as [my previous post](http://www.andreafortuna.org/security/2016/02/16/mazar-bot-root-and-erase-android-devices/):

1. NEVER click on links in SMS or MMS messages on your phone: Android phones are notoriously vulnerable and current security product dedicated to this OS are not nearly as effective as they are on computers.
2. Go to **Settings > Security** and make sure this option is turned *OFF*: "Unknown Sources – Allow installation of apps from sources other than the playstore."
3. Install a top antivirus for Android. It may not be enough to protect your phone, but it’s certainly good to have.
4. Do not connect to unknown and unsecured *Wi-Fi hotspots*. There are plenty of dangers lurking out there, and following some common-sense steps to keep yourself safe from them is the best thing to do. Also, keep your *Wi-Fi* turned *OFF* when you don’t use it.
5. Install a *VPN* on your smartphone and use constantly. It’s good for both your privacy and your security.
6. Maintain a cautious attitude at all times. Android security has not kept up with the high adoption rate of smartphones running the OS, and users may have to wait a long time until better security solutions appear. Until then, a careful evaluation of what happens on your phone is a very good safeguard.

