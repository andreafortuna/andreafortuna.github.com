---
layout: post
title: "Rooting and installing Xposed Framework on Vodafone Smart Prime 6 (VF-895N)"
thumbnail: "http://www.andreafortuna.org/technology/images/smartprime6.jpg"
description: "Rooting and installing Xposed Framework on Vodafone Smart Prime 6 (VF-895N): a simple tutorial!"
keywords: Android, Vodafone, Smart Prime 6, VF-895N, Rooting, KingRoot, SuperSU, Xposed Frameword, FireFlash, Greenify
category: Technology
tags: 
- Tips
- Android
- Xposed
- Greenify
- Hacking
- VF-895N
- Vodafone

---
{% include JB/setup %}

I am a hacker in the original sense of the term, I like taking things apart, modify them and (when I can) improve them.

So, whenever I find myself in your hands a new smartphone (especially *Android*) i feel like a child in which was given a new toy :-)

![SMartPrime6](/technology/images/smartprime6.jpg)

<!-- more -->

Recently, my company has equipped me with a shiny new *Vodafone Smart Prime 6* (VF-895N), a smartphone reasonably fast with support for 4G networks.

I immediately started to study it and I decided to go with my usual settings:

- Gaining root permissions
- Remove the *bloatware* and the pre-installed applications that i do not use
- Install the *Xposed framework*
- Install and configure [Greenify](https://play.google.com/store/apps/details?id=com.oasisfeng.greenify){:target="_blank"} and the respective Xposed module 

Let's see in detail the required steps

<hr/>

Gaining the root permissions with *KingRoot*
--

![KingRoot](https://lh3.googleusercontent.com/proxy/vS4OG5w0qyID4ww6Xpd1SIAJOqmdTDOcE2lXbpHYhQC30m1AFvxbPLLpQPNyXT7JFZCssRyPAVMXTjrSHQuB0g=w426-h240-n)

Get root permissions is quite simple: just install the well known *KingRoot*.

Version 4.5.2 works very well with the latest firmware update (Android 5.0.2 - 120FDN1): can be downloaded from the [official thread on XDA](http://forum.xda-developers.com/android/apps-games/one-click-root-tool-android-2-x-5-0-t3107461){:target="_blank"}.

Download the app, install it, start it and follow on screen instructions :-)

<hr/>

Replace *KingRoot* with *SuperSU*
--

![SuperSU](http://cdn.droidviews.com/wp-content/uploads/2014/11/SuperSU.jpg)

For *FlashFire* compatibility (and privacy!) reasons, before proceeding with the other steps we have to replace KingRoot with [SuperSU](https://play.google.com/store/apps/details?id=eu.chainfire.supersu&hl=it){:target="_blank"}.

The procedure is always on XDA, at [http://forum.xda-developers.com/android/general/guide-to-replace-kinguser-supersu-t3185998](http://forum.xda-developers.com/android/general/guide-to-replace-kinguser-supersu-t3185998){:target="_blank"}:

- Install [*SuperSu* from *GooglePlay*](https://play.google.com/store/apps/details?id=eu.chainfire.supersu&hl=it){:target="_blank"}
- Send the extracted folder "mrw" to the internal storage of your device and make sure that this folder contains 4 files
- Open Terminal emulator and type : *su*
- Allow root permission
- Type : *sh /sdcard/mrw/root.sh*
- It might display some error ignore these errors, at the end it will launch supersu or open supersu manually.
- Update *SU* binary from *SuperSU app*, then reboot.

<hr/>

Installing FlashFire
--

![FlashFire](http://droidgeeks.org/wp-content/uploads/2015/04/FlashFire-DG-1024x576.jpg)

The beta version of *Xposed* for *Android Lollipop* needs to be installed through a package that must be flashed with a *custom recovery*.

However, currently there is no custom recovery for the *Vodafone Smart Prime 6* (it's a young and not very common device).

To install *Xposed*, we should then use a tool alternative to custom recovery: *FlashFire*.

Currently in beta stage, *FlashFire* can be downloaded joining the [developers community on Google plus](https://plus.google.com/communities/116661625291346007584){:target="_blank"}.

After that, sign up on *Google play* with the same *G+* account and open [this link](https://play.google.com/apps/testing/eu.chainfire.flash){:target="_blank"}.

Once registered, the beta link on *Google Play* will be provided, now you should able to download the FlashFire tool.

<hr/>

Installing *Xposed Framework*
--

![Xposed](http://img.tuttoandroid.net/wp-content/uploads/2015/01/xposed.png)

Finally, we start to install the *Xposed framework*.

First, go to the [Official XDA Thread](http://forum.xda-developers.com/showthread.php?t=3034811){:target="_blank"}, download the *XposedInstaller_3.0_alpha4.apk* and the *xposed-v75-sdk21-arm.zip*, and copy them in phone storage.

From phone, open any file manager app, head over to the folder where you have saved the *Xposed installer*, and select it to confirm  installation.

Open *FlashFire app* and provide it root access. 

Now use the *Flash Zip* option (from 'Plus' button on bottom right) to install the *Xposed framework* that you downloaded in the above step.

The procedure can take several minutes, do not worry if the screen remains blank for a long time.

After the restart, open *Xposed Installer App* and verify the correct installation of the framework:

![xposed](/technology/images/xposedlollipop.png).

Now, you can install a full feature [Greenify](https://play.google.com/store/apps/details?id=com.oasisfeng.greenify){:target="_blank"} with xposed module!

