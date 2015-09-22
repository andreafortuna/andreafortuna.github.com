---
layout: post
title: "Geolocating with a single javascript line"
thumbnail: "http://www.andreafortuna.org/technology/images/geocaching.jpg"
description: "Geolocating in HTML5 with a single line of code? 'It Could Work!'"
keywords: HTML5, JAVASCRIPT, Geolocation, Programming
category: Programming
tags: 
- Tips
- Programming
- Javascript

---
{% include JB/setup %}

Geolocating in HTML5 with a single line of code? "It Could Work!"

![Geolocation](/technology/images/geocaching.jpg)

<!-- more -->

Some infos about geolocation API from [http://dev.w3.org/](http://dev.w3.org/geo/api/spec-source.html){:target="_blank"}:

>The Geolocation API defines a high-level interface to location information associated only with the device hosting the implementation, such as latitude and longitude. The API itself is agnostic of the underlying location information sources. Common sources of location information include Global Positioning System (GPS) and location inferred from network signals such as IP address, RFID, WiFi and Bluetooth MAC addresses, and GSM/CDMA cell IDs, as well as user input. No guarantee is given that the API returns the device's actual location.

>The API is designed to enable both "one-shot" position requests and repeated position updates, as well as the ability to explicitly query the cached positions. Location information is represented by latitude and longitude coordinates.

And here the code:

<iframe width="100%" height="100" src="//jsfiddle.net/4t5tb489/embedded/" allowfullscreen="allowfullscreen" frameborder="0"></iframe>

Obviously, the functions for *error* and *success* events could  be externally declared for better readability.
