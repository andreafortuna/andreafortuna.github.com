---
layout: post
title: "Lubuntu 16 freeze after suspend? Upgrade the kernel!"
thumbnail: "http://www.andreafortuna.org/technology/images/lubuntu-16-freeze-on-suspend/lubuntu.png"
description: "After upgrade to Lubuntu 16, your laptop not responding when suspended? It can be solved with a simple kernel upgrade."
keywords: Technology, Linux, Lubuntu, Kernel 4.4.8, canonical, Lenovo G50-45
category: Technology
tags: 
- Technology
- Linux
- Lubuntu

---

After upgrade to **Lubuntu 16**, your laptop (in my case, a **Lenovo G50-45**) not responding when suspended? It can be solved upgrading the kernel to **4.4.8**.

![lubuntu](http://www.andreafortuna.org/technology/images/lubuntu-16-freeze-on-suspend/lubuntu.png)

**Canonical** has packed all the kernel releases as deb packages and made them available for Ubuntu-based systems, via its **kernel.ubuntu.com** repository.

Simply follow this steps, from [http://linuxdaddy.com/](http://linuxdaddy.com/blog/install-kernel-4-4-on-ubuntu/){:target="_blank"}:


```$ cd /tmp```
```$ wget kernel.ubuntu.com/~kernel-ppa/mainline/v4.4.8-wily/linux-headers-4.4.8-040408_4.4.8-040408.201604200335_all.deb``` 
```$ wget kernel.ubuntu.com/~kernel-ppa/mainline/v4.4.8-wily/linux-headers-4.4.8-040408-generic_4.4.8-040408.201604200335_amd64.deb```
```$ wget kernel.ubuntu.com/~kernel-ppa/mainline/v4.4.8-wily/linux-image-4.4.8-040408-generic_4.4.8-040408.201604200335_amd64.deb```
```$ sudo dpkg -i linux-headers-4.4*.deb linux-image-4.4*.deb```

That's it! :-)





