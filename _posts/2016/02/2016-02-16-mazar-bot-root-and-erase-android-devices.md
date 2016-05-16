---
layout: post
title: "Mazar BOT: new Android malware that can root and erase your device"
thumbnail: "http://oldsite.andreafortuna.org/technology/images/MazarBOT.png"
description: "Researchers of Heimdal Security, analyzing an SMS message sent to random mobile numbers and locations, have discovered a new Android Malware, Mazar BOT."
keywords: Security, Threat, Android, MazarBOT, PEBKAC, TOR, SMS, Heimdal Security
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
{% include JB/setup %}

Researchers of [Heimdal Security](https://heimdalsecurity.com/){:target="_blank"}, analyzing an *SMS* message sent to random mobile numbers and locations, have discovered a new Android Malware, **Mazar BOT**.

![MazarBOT](/technology/images/MazarBOT.png)


The SMS / MMS in question arrives with the following contents:

>You have received a multimedia message from +[country code] [sender number] Follow the link http: //www.mmsforyou [.] Net / mms.apk to view the message.

The Malware
--

If the *APK* runs on an Android device, then it will ask administrator rights on the victim’s device. 

This will allow the attackers to:

- Gain boot persistence to help survive device restarts
- Send and Read your SMS messages
- Make Calls to your contacts
- Read the phone's state
- Plague phone's control keys
- Infect your Chrome browser
- Change phone settings
- Force the phone into sleep mode
- Query the network status
- Access the Internet
- Wipe your device's storage (the most critical capabilities of all)

Once installed, the malware retrieves,unpacks and runs the *TOR* application, which will then be used to connect to a .onion server in the darkweb (http://pc35hiptpcwqezgs.Onion) and after sends an automated SMS to the number 9876543210 (+98 is the country code for Iran) with the text message: "Thank you". 

The catch is that this *SMS* also includes the device’s location data.

*Mazar BOT* would seem to be the first *Android malware*  with the ability to remain covert by using *TOR* to hide its communication.

How to protect yourself?
--

[Heimdal Security](https://heimdalsecurity.com/blog/security-alert-mazar-bot-active-attacks-android-malware/){:target="_blank"} suggests:

1. NEVER click on links in SMS or MMS messages on your phone: Android phones are notoriously vulnerable and current security product dedicated to this OS are not nearly as effective as they are on computers.
2. Go to **Settings > Security** and make sure this option is turned *OFF*: "Unknown Sources – Allow installation of apps from sources other than the playstore."
3. Install a top antivirus for Android. It may not be enough to protect your phone, but it’s certainly good to have.
4. Do not connect to unknown and unsecured *Wi-Fi hotspots*. There are plenty of dangers lurking out there, and following some common-sense steps to keep yourself safe from them is the best thing to do. Also, keep your *Wi-Fi* turned *OFF* when you don’t use it.
5. Install a *VPN* on your smartphone and use constantly. It’s good for both your privacy and your security.
6. Maintain a cautious attitude at all times. Android security has not kept up with the high adoption rate of smartphones running the OS, and users may have to wait a long time until better security solutions appear. Until then, a careful evaluation of what happens on your phone is a very good safeguard.

Personally, I think the *last point* is really important: as in most cases, without user intervention, the malware can not infect the terminal. 

It therefore constitutes a perfect [PEBKAC](https://en.wikipedia.org/wiki/User_error#PEBKAC){:target="_blank"}.

![PEBKAC](http://www.userfriendly.org/cartoons/archives/98may/uf980506.gif)