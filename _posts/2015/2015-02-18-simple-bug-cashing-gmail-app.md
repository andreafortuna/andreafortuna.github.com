---
layout: post
title: "A very simple bug can crash the stock Email App on Android"
description: "Hector Marco discover a very simple bug can crash the stock Email App on Android"
category: Security
tags: 
- Android
- Google
- Vulnerability
---
{% include JB/setup %}

[Hector Marco](http://hmarco.org/) & [Ismael Ripoll](http://personales.upv.es/~iripoll/) have discovered a bug on android's stock Email App that can crash the client with a simple email message.

![Crash](http://hmarco.org/bugs/email_crash2.png)

<!-- more -->

The news is reported by [TheHackerNews](http://thehackernews.com/2015/02/stock-android-email-app.html), that writes:

>A Spain security researcher, Hector Marco, successfully exploited the vulnerability on his Samsung Galaxy S4 Mini running version 4.2.2.0200 of Stock Android Email App. He said the flaw appears to affect all older versions of Stock Android Email App, though devices running 4.2.2.0400 and newer versions are not affected.
According to the researcher, when the victim receives the malicious email and tries to view it, the email app crashes. Further attempts to open the email again triggers a crash in the application before the victim can do anything.

On [Marco's blog](http://hmarco.org/bugs/google_email_app_4.2.2_denial_of_service.html), there is a good explanation of the vulnerability:

>The bug appears because an incorrect handling of the Content-Disposition header. An incorrect Content-Disposition header causes the crash. The malformed header which produces the crash is:

```
Content-Disposition: ;
```

>According to RFC2183 the parameters are missing. The correct header shall look like:

```
Content-Disposition: attachment; filename=genome.jpeg;
```

and, about the exploit:

>To successfully exploit this vulnerability the attacker only needs to send an email to the victim with an empty Content-Disposition followed by a semicolon.

Marco also has writes a simple python script to send malicious emails: [crash_Android_Google_email_4.2.2.0200.py](http://hmarco.org/cyber-security/exploits/crash_Android_Google_email_4.2.2.0200.py)

![python script](http://oldsite.andreafortuna.org/images/androidemail.PNG)

