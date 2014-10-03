---
layout: post
title: "Protesters in Hong Kong are spied through a trojan installed on their iPhone?"
description: ""
category: Security
tags: 
- iPhone
- Hong Kong
- Trojan
---
{% include JB/setup %}
In [this article](http://www.nytimes.com/2014/10/02/business/protesters-are-targets-of-scrutiny-through-their-phones.html) on [The New York Times](http://www.nytimes.com), *Paul Mozur*  explains that the Chinese government would be using a trojan installed on the phones of protesters to monitor their movements and communications.

![Xsser mRAT](https://c2.staticflickr.com/4/3929/15385808216_23b85def3f_z.jpg)

<!-- more -->
The trojan could be **Xsser mRAT**, [discovered](https://www.lacoon.com/lacoon-discovers-xsser-mrat-first-advanced-ios-trojan/) few days ago from [Lacoon Mobile Security](https://www.lacoon.com):

>The Xsser mRAT specifically targets iOS devices, and is related to Android spyware already distributed broadly in Hong Kong.

The infection is spread by using a link sent through a WhatsApp message, that invites to download an app to help coordinate Occupy Central protests in Hong Kong. 

>In its investigation of that spyware, Lacoon uncovered the Xsser mRAT hosted on the same Command and Control (CnC) domain with the project being named Xsser. Though called Xsser, this is not related to an XSS attack.

The text in the anonymous message is this:

>“Check out this Android app designed by Code4HK for the coordination of OCCUPY CENTRAL!”

[Code4HK](http://www.code4.hk/) is a community of programmers who have been working to support the democracy movement: it has nothing to do with the application, according to Lacoon.

Lacoon has released a lot of informations about infection methods:

>The iOS device needs to be jailbroken in order to be infected. Then with Cydia installed, the repository would be need to be added and then the package could be installed. All that’s known is that both the iOS and Android attacks share a CnC server.

>The package itself is a debian .deb package. The package installs an iOS ‘launchd’ service to make sure the app starts after booting and in addition starts it up immediately.

More information in the [original post](https://www.lacoon.com/lacoon-discovers-xsser-mrat-first-advanced-ios-trojan/).