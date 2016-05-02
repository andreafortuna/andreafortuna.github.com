---
layout: post
title: "Tor in a company network: how to detect and block it?"
thumbnail: "http://www.andreafortuna.org/security/images/TOR/tor_cover.png"
description: "TOR is an important tool. It has its benefits and it could be the perfect way for end users to cover their tracks, but the use of this tool in a corporate network can open up organizations to some risks."
keywords: Security, Threat
category: Security
tags: 
- Security
- Privacy
- Tor

---

**TOR** is an important tool. 

It has its benefits and it could be the perfect way for end users to cover their tracks, but the use of this tool in a corporate network can open up organizations to some risks.

<hr/>

What is TOR?
--

![What is TOR](http://www.makeuseof.com/wp-content/uploads/2015/06/Wat_is_Tor_The_onion_routing--640x312.png)

Tor is a software that allows users to browse the Web anonymously. 

Tor stands for "The Onion Router" and it is called so because it uses the "Onion routing protocol" to hide information about user activity, location and usage from anyone that conducts network surveillance or traffic analysis. 

It’s often used by journalists, political dissidents and criminals to keep their communications private.

The development of the "onion routing protocol" was sponsored by the **U.S. Naval Research Laboratory** in the 1990s, and Tor was developed by the Navy and independent researchers in 2002. 

Currently the protocol is still being worked on and supported under the **[Tor Project](https://www.torproject.org)**, a nonprofit organization.

<div class="video-container">
<iframe src="https://www.youtube.com/embed/JWII85UlzKw" frameborder="0" allowfullscreen></iframe>
</div>


<hr>


How it works?
--

![TOR Explain](http://www.andreafortuna.org/security/images/TOR/tor_explain.png)

When you connect to Tor, your computer becomes a node and can be used by any other Tor users to relay their traffic. 

The Tor network hides your identity by moving your (encrypted) traffic across different computers (nodes) located all across the world. 

Instead of taking a direct route from source to destination, the data packet sent on the Tor network takes a random pathway through several servers: no one will ever know the complete path that a data packet has taken (in effect no one at any single node can tell where the data originally came from and where is the final destination).



<hr/>

It can be a risk?
--

<div class="video-container">
<iframe src="https://www.youtube.com/embed/HjejYd_9Oik" frameborder="0" allowfullscreen></iframe>
</div>


While it is true that Tor can be used with the legitimate goal of anonymity on the internet, it can represent a gigantic problem for a company, for example:

- **Bypass security controls**: Tor encrypts all the traffic over the network and makes the monitoring of the activities very hard. Employees can bypass the security policies and controls of the organization very easily.

- **Information theft**: Exit nodes can monitor the traffic transiting through his device and capture any non-encrypted information such as login/password.

- **Impacts on the organization’s reputation and Blacklisting**: people managing the “exit nodes” can use the node to add malware, and any user downloading through Tor exposes the organization network to malware infection.

- **Malware and botnet attacks**: people operating one of the "exit nodes" can use the device to add malware, and any user downloading through Tor exposes the organization network to malware infection.

- **DDoS attacks**: Tor network traffic can cause high use of the corporate network bandwidth which makes the organization permanently exposed to a DDoS attack.


<hr/>

How to block Tor inside a company network?
--

The censors governments have developed various methods to block Tor traffic.

<div class="video-container">
<iframe src="https://www.youtube.com/embed/GwMr8Xl7JMQ" frameborder="0" allowfullscreen></iframe>
</div>

>**Iran** blocked Tor handshakes using Deep Packet Inspection (DPI) in January 2011 and September 2011. Bluecoat tested out a Tor handshake filter in **Syria** in June 2011. **China** has been harvesting and blocking IP addresses for both public Tor relays and private Tor bridges for years.

<div class="video-container">
<embed src="http://www.andreafortuna.org/security/files/TOR/slides-28c3.pdf" pluginspage="http://www.adobe.com/products/acrobat/readstep2.html">
</div>


Detecting and blocking **Tor** in a corporate network is not an easy thing. 

Sysadmins should consider the deployment of more than one solution to enhance the chance of preventing the use of **Tor** in their network.

Tor doesn't just provide encryption, it is also designed to look like normal **HTTPS** traffic, which makes Tor communication difficult to identify.

So, block the use of TOR in a corporate network in my view it's not possible, but it can be applied some mitigation actions that can bring us closer to the goal:


- **Stop users from installing Tor**: Implementing security controls that limit user access rights to a computer will contribute to prevent the installation of unauthorized software or device.

- **Develop a blacklist of Tor nodes**: Stopping all the outbound traffic related to Tor at the border firewalls level by creating an explicit outbound deny rule based on the blacklisted IPs. 
 This solution makes also possible to build a log of all hosts attempting to connect with the Tor nodes. 
 The blacklist can be build using online resources, like [https://www.dan.me.uk/tornodes](https://www.dan.me.uk/tornodes).

- **Block all traffic using self-signed digital certificates**: Tor uses self-generated SSL certificates to encrypt traffic between nodes and servers. Blocking all the outbound SSL traffic that uses self signed SSL certificates across your network (using Proxy services and Web Application Firewall) can contribute to prevent the use of Tor.
