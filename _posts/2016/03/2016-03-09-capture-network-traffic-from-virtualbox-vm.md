---
layout: post
title: "Capture network traffic on a VirtualBox VM"
thumbnail: "http://www.andreafortuna.org/technology/images/VirtualBox.png"
description: "Simple tip to dump all network traffic of a VirtualBox VM without using other tools."
keywords: Technology, Security, VirtualBox, WireShark, pcap, traffic dump
category: Technology
tags: 
- Technology
- Tips
- VirtualBox

---

Simple tip to dump all network traffic of a *VirtualBox VM* without using other tools (like *WireShark*), using the built-in capability of *VirtualBox* to create *pcap* files.

![Virtualbox](http://www.andreafortuna.org/technology/images/VirtualBox.png)

To enable network tracing do the following:

```# VBoxManage modifyvm [your-vm] --nictrace[adapter-number] on --nictracefile[adapter-number] file.pcap```

and start the *VM*.

For example:

```# VBoxManage modifyvm "ubuntu" --nictrace1 on --nictracefile1 capture.pcap```

All network traffic of *VM* will be dumped into *capture.pcap*.

*Warning*: in case of intensive network traffic, the pcap file will grow a lot, so when the debugging session is closed, remember to disable the tracing:

```# VBoxManage modifyvm "ubuntu" --nictrace1 off```
