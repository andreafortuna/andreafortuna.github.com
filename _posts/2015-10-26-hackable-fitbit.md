---
layout: post
title: "Fitbit Activity tracker bluetooth vulnerability?"
thumbnail: "http://www.andreafortuna.org/technology/images/fitbit.jpg"
keywords: Security, FitBit, tracker, malware, bluetooth
description: "A vulnerability in FitBit fitness trackers first reported to the vendor in March could still be exploited by an attacker that sits near you."
category: Security
tags: 
- Security
- Malware
- Fitbit
- Bluetooth

---
{% include JB/setup %}

A vulnerability in FitBit fitness trackers first reported to the vendor in March could still be exploited by an attacker that sits near you.

![FitBit](/technology/images/fitbit.jpg)
<!-- more -->

The activity trackers wearables are wide open on their Bluetooth ports, according to research by Fortinet. 

The attack is quick, and *can spread to other computers that connect to an infected FitBit*.


Attack is made over Bluetooth and the attacker must be near the target device. 
The malware can be delivered in 10 seconds once devices connect, making even fleeting proximity a problem.

Fortinet researcher *Axelle Apvrille* ([@cryptax](https://twitter.com/cryptax)) says:

>An attacker sends an infected packet to a fitness tracker nearby at bluetooth distance then the rest of the attack occurs by itself, without any special need for the attacker being near,

>[...] when the victim wishes to synchronise his or her fitness data with FitBit servers to update their profile … the fitness tracker responds to the query, but in addition to the standard message, the response is tainted with the infected code.

>From there, it can deliver a specific malicious payload on the laptop, that is, start a backdoor, or have the machine crash [and] can propagate the infection to other trackers (Fitbits).

>It is the first time malware has been viably delivered to fitness trackers.

<hr/>

Here a video of the Proof-Of-Concept:

<iframe width="640" height="480" src="https://www.youtube.com/embed/qa8qVAPPlTE" frameborder="0" allowfullscreen></iframe>