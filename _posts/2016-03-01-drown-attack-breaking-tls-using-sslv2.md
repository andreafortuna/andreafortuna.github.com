---
layout: post
title: "DROWN attack breaking TLS using SSLv2: more than 13 million sites at risk"
thumbnail: "http://www.andreafortuna.org/security/images/DROWNAttack.PNG"
description: "A new attack allows an attacker to decrypt an intercepted TLS-protected communications that rely on the RSA cryptosystem when the key is exposed even indirectly through SSLv2, a TLS precursor that was retired almost two decades ago for structural weaknesses. "
keywords: Security, Threat, DROWN, SSLv2, TLS, RSA
category: Security
tags: 
- Security
- Threats
- Vulnerability
- DROWN
- RSA
- SSLv2
- TLS

---
A new attack allows an attacker to decrypt an intercepted *TLS-protected* communications that rely on the *RSA* cryptosystem when the key is exposed even indirectly through *SSLv2*, a TLS precursor that was retired almost two decades ago for structural weaknesses. 

<hr/>

How it works?
---

![DROWN](http://cdn.arstechnica.net/wp-content/uploads/2016/03/drown-explainer-640x438.jpg)

The vulnerability allows an attacker to decrypt an intercepted TLS connection by repeatedly using SSLv2 to make connections to a server.

While many security experts suggest the removal of *SSLv2* support from browser and e-mail clients prevented abuse of the legacy protocol, some misconfigured *TLS* implementations still tacitly support the legacy protocol when an end-user computer specifically requests its use.

<hr/>

From [ArsTechnica](http://arstechnica.com/security/2016/03/more-than-13-million-https-websites-imperiled-by-new-decryption-attack/){:target="_blank"}:

>Recent scans of the Internet at large show that more than 5.9 million Web servers, comprising 17 percent of all HTTPS-protected machines, directly support SSLv2. 

>The same scans reveal that at least 936,000 TLS-protected e-mail servers also support the insecure protocol. That's a troubling finding, given widely repeated advice that SSLv2—short for secure sockets layer version 2—be disabled. More troubling still, even when a server doesn't allow SSLv2 connections, it may still be susceptible to attack if the underlying RSA key pair is reused on a separate server that does support the old protocol. 

>A website, for instance, that forbids SSLv2 may still be vulnerable if its key is used on an e-mail server that allows SSLv2. By the researchers' estimate, that leaves 11.5 million HTTPS-protected websites and a significant number of TLS-protected e-mail servers open to attack.

![TLS](http://cdn.arstechnica.net/wp-content/uploads/2016/02/drown-attack-640x507.png)

More technical informations can be read on [this paper](https://www.drownattack.com/drown-attack-paper.pdf){:target="_blank"}:

<div class="video-container">
<embed src="https://www.drownattack.com/drown-attack-paper.pdf" pluginspage="http://www.adobe.com/products/acrobat/readstep2.html">
</div>

<hr/>

How i fix the problem on my server?
--

First, you can check the correct configuration of your server using this online tool: [https://www.drownattack.com/#check](https://www.drownattack.com/#check){:target="_blank"}.

After, follow the instruction on [drownattack.com](https://www.drownattack.com/):

Disabling *SSLv2* can be complicated and depends on the specific server software. We provide instructions here for several common products:

*OpenSSL*: OpenSSL is a cryptographic library used in many server products. For users of OpenSSL, the easiest and recommended solution is to upgrade to a recent OpenSSL version. OpenSSL 1.0.2 users should upgrade to 1.0.2g. OpenSSL 1.0.1 users should upgrade to 1.0.1s. Users of older OpenSSL versions should upgrade to either one of these versions.

*Microsoft IIS (Windows Server)*: IIS versions 7.0 and above should have SSLv2 disabled by default. (A small number of users may have enabled SSLv2 manually and will need to take steps to disable it.) We still recommend checking whether your private key is exposed elsewhere, using the form above. IIS versions below 7.0 are no longer supported by Microsoft and should be upgraded to supported versions.

*Network Security Services (NSS)*: NSS is a common cryptographic library built into many server products. NSS versions 3.13 (released back in 2012) and above should have SSLv2 disabled by default. (A small number of users may have enabled SSLv2 manually and will need to take steps to disable it.) Users of older versions should upgrade to a more recent version. We still recommend checking whether your private key is exposed elsewhere, using the form above.

*Other affected software and operating systems:* Instructions for: [Apache](https://www.drownattack.com/apache), [Postfix](https://www.drownattack.com/postfix), [Nginx](https://www.drownattack.com/nginx)

*Browsers and other clients:* There is nothing practical that web browsers or other client software can do to prevent *DROWN*. Only server operators are able to take action to protect against the attack.