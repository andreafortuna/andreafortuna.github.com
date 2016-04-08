---
layout: post
title: "Two new threats for mobile users"
thumbnail: "http://www.andreafortuna.org/security/images/android-and-ios.jpg"
description: "In the last two days, two new threats for mobile users are discovered by researchers."
keywords: Security, Threat, IOS, Android, Qualcomm, Snapdragon, Apple, FairPlay, CVE-2016-0819,CVE-2016-0805, PaloAltoNetworks, TrendMicro
category: Security
tags: 
- Security
- Threats
- IOS
- Android
- CVE-2016-0819
- CVE-2016-0805

---
In the last two days, two new threats for mobile users are discovered by researchers.

<hr/>

A  bug on Qualcomm's Snapdragon code, at kernel-level
--

![Snapdragon](https://4.bp.blogspot.com/-yGivCivoXGE/Vul1_9MvkzI/AAAAAAAAnOA/IXEajWpKh9kxwEeCJqJzvb0z_o2T4DU2g/s1600/root-android-exploit.png)

The first, related to android ecosystem but focused on a particular *CPU technology (Qualcomm Snapdragon)* was discovered by [Trend Micro](https://blog.trendmicro.com/trendlabs-security-intelligence/android-vulnerabilities-allow-easy-root-access/){:target="_blank"}:

>We recently found vulnerabilities affecting Snapdragon-powered Android devices, which could be exploited by an attacker in order to gain root access on the target device simply by running a malicious app.

<hr/>

Two exploits, one result
--

More from [Trend Micro](https://blog.trendmicro.com/trendlabs-security-intelligence/android-vulnerabilities-allow-easy-root-access/){:target="_blank"}:

*CVE-2016-0819*

We discovered this particular vulnerability, which is described as a logic bug when an object within the kernel is freed. 

A node is deleted twice before it is freed. 

This causes an information leakage and a *Use After Free* issue in Android. 


*CVE-2016-0805*

This particular vulnerability lies in the function *get_krait_evtinfo*. 

The function returns an index for an array; however, the validation of the inputs of this function are not sufficient. 

As a result, when the array *krait_functions* is accessed by the functions *krait_clearpmu* and *krait_evt_setup*, an out-of-bounds access results. 

This can be useful as part of a multiple exploit attack.


*Using these two exploits, one can gain root access on a Snapdragon-powered Android device*. 

This can be done via a malicious app on the device.

Any *Snapdragon-powered Android* device with a *3.10-version kernel* is potentially at *risk of this attack*.

<hr/>

Now it's up to IOS
--

![Fairplay](http://researchcenter.paloaltonetworks.com/wp-content/uploads/2016/03/AceDeceiver-1-1-500x244.png)

[Paloalto Networks](http://researchcenter.paloaltonetworks.com/){:target="_blank"}  has discovered a new *iOS* malware threat named ["AceDeceiver"](http://researchcenter.paloaltonetworks.com/2016/03/acedeceiver-first-ios-trojan-exploiting-apple-drm-design-flaws-to-infect-any-ios-device/){:target="_blank"}  that afflicts *non-jailbroken iDevices* via a flaw in *Apple's DRM* mechanism:

>What makes AceDeceiver different from previous iOS malware is that instead of abusing enterprise certificates as some iOS malware has over the past two years, AceDeceiver manages to install itself without any enterprise certificate at all. 

>AceDeceiver is the first iOS malware we’ve seen that abuses certain design flaws in Apple’s DRM protection mechanism — namely FairPlay — to install malicious apps on iOS devices regardless of whether they are jailbroken. This technique is called “FairPlay Man-In-The-Middle (MITM)” and has been used since 2013 to spread pirated iOS apps, but this is the first time we’ve seen it used to spread malware.

For more technical info, refer to ["Paloalto Research Blog"](http://researchcenter.paloaltonetworks.com/2016/03/acedeceiver-first-ios-trojan-exploiting-apple-drm-design-flaws-to-infect-any-ios-device/){:target="_blank"}