---
layout: post
title: "Crashing an iPhone with a simple message?"
description: " A iOS bug  allows anyone to reboot an iPhone by simply sending it a certain string of characters in a message"
category: Security
tags: 
- Security
- iOS
- Apple
- iMessage
- Unicode

---
{% include JB/setup %}
Seriously? An iOS bug  allows anyone to reboot an iPhone by simply sending it a certain string of characters in a message?

![Humor](http://i.imgur.com/RyjawQd.jpg)
<!-- more -->

The flaw was [reported](http://www.reddit.com/r/iphone/comments/37eaxs/um_can_someone_explain_this_phenomenon/) by a Reddit user who received this message 

![Evil string](https://regmedia.co.uk/2015/05/27/dodgy_unicode.png) 

which has crashed his smartphone and rebooted it in recovery mode. 
The attack has  been replicated on other iOS devices such as Apple Watch.

TheRegister published an in-depth [article](http://www.theregister.co.uk/2015/05/27/text_message_unicode_ios_osx_vulnerability/):

>Cads and/or bounders can crash and reboot iPhones from afar by sending them specially crafted texts, thanks to a new vulnerability in iOS.
A 75-byte sequence of unicode characters triggers the glitch, and can be smuggled into text messages, causing Things to crash if they appear in the victim's notification screen. 

>The string-of-death crashes applications that use Apple CoreText library. OS X is vulnerable, too, so sticking the killer sequence in your server's /etc/motd file will crash Terminal when a Mac user logs in, for example.

<iframe width="640" height="360" src="https://www.youtube.com/embed/PnoDw2jsvnc" frameborder="0" allowfullscreen></iframe>


The crash happens at the instruction at 0x0af42d in CoreText:

![Unicode bug](https://regmedia.co.uk/2015/05/27/unicode_crash.png)

>At 0x0af428, CoreText checks whether or not the value in the CPU register rax is zero: if it is, it skips the next part. If not, at 0x0af42d it tries to read a 32-bit value from memory using rax as the memory address.

>In other words, it tries using rax as a pointer after checking it is not NULL – this is all well and good, and supposed to trap this sort of crash, except rax ends up with the value 0x04 so the NULL check is useless in this case.

After receiving the message, you can no longer use iMessage.

MacRumors however suggests [some workarounds](http://www.macrumors.com/2015/05/26/ios-bug-crashing-iphones-with-text-message/) waiting for a [patch by Apple](http://www.engadget.com/2015/05/27/apple-fixing-ios-text-crash-bug/):

>If the Messages app was opened to the conversation with the person who sent the offending message, the Messages app can be reopened to this conversation. Sending a reply message fixes the problem.

>If Messages was opened to the conversation list view, the app will crash when you attempt to open it. You can fix this by having someone send you a message or by sending a message to yourself. There are several options for sending a message to yourself, including sending yourself a message via Siri or through the Share sheet in any app.

>To send yourself a message in Siri, tell Siri to "Send a message to myself." Siri will open up a dialogue where you can give her a quick message like "Fix" that'll be sent to your iPhone to clear away the malicious message.

>Alternatively, you can open an app like Notes, craft a quick note, and use the Share option (the little document with an arrow) to message it to yourself. Sending yourself something though the share sheet of an app opens a new messages window where you can enter your own contact information. 

<iframe width="640" height="360" src="https://www.youtube.com/embed/x9Rq6qPaKRY" frameborder="0" allowfullscreen></iframe>