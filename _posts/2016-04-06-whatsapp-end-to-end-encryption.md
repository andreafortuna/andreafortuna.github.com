---
layout: post
title: "WhatsApp (finally!) enables End-To-End encryption by default"
thumbnail: "http://www.andreafortuna.org/security/images/e2ee.jpg"
description: "WhatsApp has enabled end-to-end encryption across all versions of its app, according to the announcement on the company's blog."
keywords: Security, Whatsapp, E2E Encryption
category: Security
tags: 
- Security
- Cryptography

---

WhatsApp has enabled *end-to-end encryption* across all versions of its app, according to the [announcement](https://blog.whatsapp.com/10000618/end-to-end-encryption) on the [company's blog](https://blog.whatsapp.com/):

>The idea is simple: when you send a message, the only person who can read it is the person or group chat that you send that message to. No one can see inside that message. Not cybercriminals. Not hackers. Not oppressive regimes. Not even us. End-to-end encryption helps make communication via WhatsApp private – sort of like a face-to-face conversation.

WhatsApp has also published a technical paper that can be downloaded at [this link](https://www.whatsapp.com/security/WhatsApp-Security-Whitepaper.pdf):

<div class="video-container">
<embed src="http://www.andreafortuna.org/security/files/WhatsApp-Security-Whitepaper.pdf" pluginspage="http://www.adobe.com/products/acrobat/readstep2.html">
</div>

Given that **WhatsApp** is already in use by over 1 billion people worldwide, as users upgrade to the latest version, it will become the **most widely used end-to-end crypto tool**.


<div class="video-container">
<iframe src="https://www.youtube.com/embed/K3nT_fXzvpQ" frameborder="0" allowfullscreen></iframe>
</div>

What is End-To-End Encryption?
--
In **End-To-End Encryption**, the data is encrypted on the sender's device and only the recipient device is able to decrypt it. 

*Nobody in between (Internet service provider or hacker) can read it.*

![e2ee](https://vpncritic.com/wp-content/uploads/2014/07/end-to-end-encryption.jpg)

The **cryptographic keys** used to encrypt and decrypt the messages are stored exclusively on the endpoints, and the key exchange in this scenario is considered unbreakable using known algorithms and currently obtainable computing power, there are at least two potential weaknesses that exist outside of the mathematics. 

Each endpoint must obtain the public key of the other endpoint, but a would-be attacker who could provide one or both endpoints with the attacker's public key could execute a man-in-the-middle attack. 

The generally employed method for ensuring that a public key is in fact the legitimate key created by the intended recipient is to embed the public key in a certificate that has been digitally signed by a well-recognized certificate authority (CA).


Some reactions from most important sites
--

From [Hacker News - WhatsApp's Signal Protocol integration is now complete](https://news.ycombinator.com/item?id=11431108):

> This is really excellent. A few thoughts:

> 1) They seem to have replaced TLS/SSL between client and server with "Noise Pipes". Based on a couple of minutes Googling this seems to be a brand new one-man protocol from Trevor Perrin (the same guy who did Axoltl on which Signal is based). At least, I'd never heard of it. I wonder if this is the first inkling of a post-TLS future? (http://noiseprotocol.org/noise.html)

> 2) It's a shame to see key words be killed off by internationalisation concerns. 12 words seems so much more friendly, at least to English speakers, than a 50 digit number. In practice I doubt any non-trivial numbers of people will ever compare codes by reading out such a number. I hope further research here can develop better replacements for encoding short binary strings in i18n friendly ways (perhaps with icons instead of specific words? if you don't speak a common language with your chat partner then the app is useless anyway).

> 3) What's the next step? My feeling is that the next step is securing the build and distribution pipeline. WhatsApp could partner with security firms around the world, like Kaspersky Lab in Moscow, perhaps one in Germany and another in Iran, to make it harder for the software to be forcibly backdoored by a single decision of a single government representative. This would require splitting the RSA signing keys used by the app stores. I have some code in my inbox that claims it can do this (it's written by some academics and I obtained it after a bit of a runaround) but I never found the time to play with it.

<hr/>

From [Arstechnica](http://arstechnica.com/tech-policy/2016/04/whatsapp-is-now-most-widely-used-end-to-end-crypto-tool-on-the-planet/):

> The implementation of this crypto protocol is largely thanks to American tax dollars: since 2013, Open Whisper Systems has received a total of $2.25 million from the Open Technology Fund, an umbrella group whose primary funder is the United States government, through agencies such as the Broadcasting Board of Governors and the Department of State.

>The WhatsApp paper also points out that the encryption protocol uses perfect forward secrecy, so that **"even if encryption keys from a user’s device are ever physically compromised, they cannot be used to go back in time to decrypt previously transmitted messages."**

Specifically, WhatsApp uses **[Curve25519](https://en.wikipedia.org/wiki/Curve25519)**, and the app now allows users to verify fingerprints for a given chat session, presumably over a secondary communications channel.

<hr/>

From [The Guardian](https://www.theguardian.com/technology/2016/apr/05/whatsapp-rolls-out-full-encryption-to-a-billion-messenger-users):

> WhatsApp appears to be betting that three years after **[Edward Snowden’s revelations](http://www.theguardian.com/us-news/the-nsa-files)** rekindled a global debate over digital surveillance, consumers do care about data security as a deciding issue in which apps they will use.

> **Telegram**, a Berlin-based messaging service that has grown dramatically since 2013, has made similar bets as it offers privacy features. Meantime, Google and Snapchat both are exploring their own encrypted messaging services.

<hr/>

From [Slashdot](https://it.slashdot.org/story/16/04/05/1713244/whatsapp-enables-end-to-end-encryption-for-all-forms-of-communications-by-default):

> Once a client recognizes a contact as being fully e2e capable, it will not permit transmitting plaintext to that contact, even if that contact were to downgrade to a version of the software that is not fully e2e capable. This prevents the server or a network attacker from being able to perform a downgrade attack.

> While WhatsApp is among the few communication platforms to build full end-to-end encryption that is on by default for everything you do, we expect that it will ultimately represent the future of personal communication.

<hr/>

From [Wired](http://www.wired.com/2016/04/forget-apple-vs-fbi-whatsapp-just-switched-encryption-billion-people/):

> The company employs only about **50 engineers**. And it took a team of **only 15 of them** to bring encryption to the company’s one billion users—a tiny, technologically empowered group of individuals engaging in a new form of asymmetrical resistance to authority, standing up not only to the US government, but all governments.

<hr/>

From [SecurityWeek](http://www.securityweek.com/whatsapp-toughens-encryption-after-apple-fbi-row):

> US Congress is expected to consider legislation which would require technology firms to retain "keys" that could retrieve data in a criminal investigation, with a court order. Similar measures are under consideration in Britain and France.

> A broad coalition of technology companies and activists have argued against any encryption rules that would allow "special access" for law enforcement, claiming these would be vulnerabilities that could be exploited by hackers or repressive governments, and threaten security of banking, electronic commerce, trade secrets and more.

<hr/>

From [The Hacker News](http://thehackernews.com/2016/04/whatsapp-end-to-end-encryption.html):

>**Important Note —** However, there is one point to be noted that if several users are sending texts in a group chat and one of the users is running an older version of WhatsApp that doesn’t support encrypted messages, all the conversation going through that group chat will remain unencrypted.