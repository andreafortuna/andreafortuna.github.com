---
layout: post
title: "Import a Windows physical machine into a VirtualBox virtual machine "
description: "It had to help a user in the migration from an old laptop (with serious motherboard issues) to a new laptop. "
thumbnail: "http://www.andreafortuna.org/technology/images/virtualWinXP.png"
keywords: Windows, VirtualBox, Tips, Disk2VHD
category: Technology
tags: 
- Windows
- VirtualBox
- Tips
- Disk2VHD

---
{% include JB/setup %}
*English version of an [old Italian post (2013/07/29)](/2013/07/29/importare-una-macchine-fisica-in-una/) that has received many visits.*
Maybe it can be useful!

<hr/>

It had to help a user in the migration from an old laptop (with serious motherboard issues) to a new laptop. 

![VirtualBOX](/technology/images/virtualWinXP.png)
<!-- more -->

The old PC was equipped with *Windows XP*, it contained at least 6 years of data stratified and some old copies of licensed software (with an old version of Lotus Notes) of which had been lost licenses and install media. 

Data and software migration seemed so complicated: the old laptop go to freeze when the CPU temperature exceeded 20 degrees. 

So i played the card of virtualization: I open the laptop, i pull out the hard drive and i mount it in a *SATA-USB* box . 

The goal: create an image of the physical disk to use in a virtual machine to run from [VirtualBox](http://www.virtualbox.org/){:target="_blank"} in the new computer. 

With only a Windows PC , without downloading a live distro of Linux I decided to use an official Microsoft tool. 

The tool is [Disk2vhd](http://technet.microsoft.com/en-us/sysinternals/ee656415.aspx){:target="_blank"} , and allows you to create a disk image from a physical disk: the image format is *VHD* (Virtual Hard Disk - Microsoft's Virtual Machine disk format), which fortunately is fully supported by *VirtualBox* . 

![Disk2vhd](http://i.technet.microsoft.com/ee656415.Disk2vhd163r(en-us,MSDN.10).jpg)

The use is very simple: just start the utility, select the disk you want to import and choose the directory in which to save the image. 
The procedure is also quite fast: a *60GB* disk was imported in less than 15 minutes. 

Once the image is created, I created a new virtual machine and, when choosing whether to create a new disk or use an existing one, I chose the second option and specify the path of the file just created. 

To avoid boot errors caused by the change of hardware, I made a few small changes to the configuration: in the *System* section I modified the chipset tp **ICH9** and enabled **IO PIC**. 

![Settings](http://1.bp.blogspot.com/-D1UknDXYkjs/UfYo-ibWHmI/AAAAAAAAFaE/yEgvBzGCC10/s640/vbox.png)

After starting the virtual machine, I installed the [VirtualBox Guest Additions](http://www.virtualbox.org/manual/ch04.html){:target="_blank"} and created a shortcut on the desktop to start the emulated machine. 
