---
layout: post
title: "Recovering from a 'rm -rf /'?"
thumbnail: "http://www.andreafortuna.org/technology/images/sudo-rm-rf/sudo-rm-rf-cover.jpg"
description: ""
keywords: Technology, Humor, CentOS, Linux, Safe-rm, Serverfault
category: Technology
tags: 
- Technology
- Humor

---

UPDATE
--
It was a hoax: [That man who ‘deleted his entire company’ with a line of code? It was a hoax](http://www.pcworld.com/article/3057235/data-center-cloud/that-man-who-deleted-his-entire-company-with-a-line-of-code-it-was-a-hoax.html){:target="_blank"}

![hoax](http://core0.staticworld.net/images/article/2016/04/troll-100656387-medium.jpg)


<hr/>

Recently i read this ask on [Serverfault](http://serverfault.com/q/769357){:target="_blank"}:

>I run a small hosting provider with more or less **1535** customers and I use Ansible to automate some operations to be run on all servers. Last night I accidentally ran, on all servers, a Bash script with a ```rm -rf {foo}/{bar}``` with those variables undefined due to a bug in the code above this line.

>All servers got deleted and the offsite backups too because the remote storage was mounted just before by the same script (that is a backup maintenance script).

>How I can recover from a ```rm -rf /``` now in a timely manner?

<hr/>

![rm -rf](https://framasphere.org/camo/f75bfb974b0e9b8e15ddd3dc03b2493acc8336fb/68747470733a2f2f6c68332e676f6f676c6575736572636f6e74656e742e636f6d2f2d6c5865395678564d446d6b2f56745747393969357342492f41414141414141416169552f776f62426e52664171686f2f773334362d683139352f7375646f726d2e676966)

<hr/>

A few hours after the publication, ServerFault blocked the topic for this reason: 

> This post has been locked due to the high amount of off-topic comments generated.

A good lesson for all.

The solution?
--
![safe-rm](http://www.andreafortuna.org/technology/images/sudo-rm-rf/safe-rm.png)

Keep backups (really) offsite, and use **[Safe-rm](https://launchpad.net/safe-rm){:target="_blank"}**:

> Safe-rm is a safety tool intended to prevent the accidental deletion of important files by replacing /bin/rm with a wrapper, which checks the given arguments against a configurable blacklist of files and directories that should never be removed.

