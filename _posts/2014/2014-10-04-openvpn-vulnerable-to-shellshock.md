---
layout: post
title: "OpenVPN Vulnerable to Shellshock"
description: ""
category: Security
tags: 
- ShellShock
- OpenVPN
---
{% include JB/setup %}
Fredrick Stromberg reported on [HackerNews](https://news.ycombinator.com/item?id=8385332) that [OpenVPN](https://openvpn.net/) is vulnerable to [Shellshock](http://oldsite.andreafortuna.org/tags.html#Shellshock-ref) , the vulnerability in Bash present in most UNIX based systems.

![OpenVPN Logo](http://oi61.tinypic.com/2n697uu.jpg)

<!-- more -->
The attack vector in *OpenVPN* is particularly dangerous because it’s pre-authenticated, putting all communication through a supposedly secure tunnel at risk:

>OpenVPN servers are vulnerable to Shellshock under certain configurations.

>OpenVPN has a number of configuration options that can call custom commands during different stages of the tunnel session. Many of these commands are called with environmental variables set, some of which can be controlled by the client. One option used for username+password authentication is "auth-user-pass-verify". If the called script uses a vulnerable shell, the client simply delivers the exploit and payload by setting the username. This attack vector is pre-auth.

>When we discovered this last week we contacted security@openvpn.net as well as many of our colleagues. Given how many users could potentially be affected we reasoned that maximum utility would be achieved by giving VPN providers a heads up before warning everyone. If you were affected but not informed I apologize.

*Fredrick Stromberg* is cofounder of [Mullvad](https://mullvad.net/en/), a Swedish **VPN** company.
