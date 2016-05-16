---
layout: post
title: "Ransomware written in PHP attacks blogs and CMS?"
thumbnail: "http://oldsite.andreafortuna.org/security/images/aids-ransomware.png"
description: "Interesting article that i read on Naked Security Blog by Sophos, about a specific type of ransomware written in PHP attacking blogs and CMS"
keywords: Security, Threat, ransomware, PHP, AIDS Information Trojan, Windows
category: Security
tags: 
- Security
- Threats
- Vulnerability
- Ransomware
- PHP

---

The very first ransomware, more than *25 years ago*, was the [AIDS Information Trojan](https://en.wikipedia.org/wiki/AIDS_(Trojan_horse)){:target="_blank"}, that ran on old *MS-DOS*: a trojan horse that replaces the *AUTOEXEC.BAT* file which would be used to count the number of times the computer has booted. 

![AIDS ransomware](http://oldsite.andreafortuna.org/security/images/aids-ransomware.png)

Once this boot count reaches 90, *AIDS* hides directories and encrypts the names of all files on drive *C:* and asks the user to **renew the license** and contact *PC Cyborg Corporation* for payment (which would involve sending *189 US$* to a post office box in *Panama*).

Today, most *file-scrambling* ransomware is written for *Windows computers*, although it can encrypt files anywhere they have write access, including file servers and cloud storage sites.

There are also a few attempts at both *Android* and *Linux* ransomware.

Recently, a new generation on ransomware was discovered.

<hr/>

A ransomware written in PHP
--

From [Naked Security](https://nakedsecurity.sophos.com/2016/03/02/php-ransomware-attacks-blogs-websites-content-managers-and-more/){:target="_blank"}:

>...if a crook has your blog password and can upload files to your server, or if you have an unpatched server plugin that allows him to modify files that are supposed to be write-protected, and he can alter one or more of your PHP files…
…then he can install a payload on your website that will trigger whenever anyone happens to visit the booby-trapped page.

The malware, known as *Troj/PHPRansm-B*, infects your server with a *index.php* file that contains:

- File encrypting and decrypting code using *PHP*.
- Style-sheet information using *CSS*, plus inline images.
- A *pay page* using **HTML** and **JavaScript**.

Once the encryption process is completed, anyone visiting the page will see a warning page like this:

![PHP Ransomware](https://sophosnews.files.wordpress.com/2016/03/paypage-640.png)

<hr/>

How can I prevent it?
--

[Naked Security](https://nakedsecurity.sophos.com/2016/03/02/php-ransomware-attacks-blogs-websites-content-managers-and-more/){:target="_blank"} suggests:

- Pick a *proper password* for your web server, content management system or blog. 
- Consider using *two-factor* authentication. 
- Review all your server access permissions. 
- Make sure your server is patched against security holes. 
- Run a *real-time anti-virus* on your server. 