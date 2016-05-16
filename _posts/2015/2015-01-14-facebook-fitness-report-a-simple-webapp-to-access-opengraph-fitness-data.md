---
layout: post
title: "Facebook Fitness Report: a simple webapp to access opengraph fitness data"
description: "Accessing opengraph fitness data through facebook API"
category: Programming
tags: 
- Running
- Facebook
- Opengraph
- Javascript
---
{% include JB/setup %}

In my [previous post](http://oldsite.andreafortuna.org/running/2015/01/12/running-chronicles-2014-report/), I have published a simple report of my running activities in 2014.
All data used for the report are extracted from my facebook datafeed, using the [OpenGraph API](https://developers.facebook.com/docs/opengraph?locale=it_IT).

![caledos](/images/caledosRunner.PNG)
<!-- more -->

Some of my twitter followers asked me if I have used a custom script to make the report: yes, initially I have realized a simple jquery page, that i have converted in a webapp with small changes. May be useful for other runners!

The app is realized in HTML5 (using a usefull [responsive boilerplate](http://www.initializr.com/)), with some facilities offered by *JQuery* and *JQueryUI*.

After the facebook login process, needed to obtain an access token, the access to facebook data feed is made with a simple **$.getJSON** call, with a simple trick: by default, the result is paginated but with an optional querystring parameter (**limit=100000**)

```
$.getJSON("https://graph.facebook.com/v2.2/me/fitness.runs?limit=100000&access_token=" + fbToken
```

i have forced the API to return all datafeed.

![screenshot](/images/FacebookFitnessReport.PNG)

All processed data are stored locally in the browser using the **localStorage** capability, for a fast further access.

The application is available from [http://fitnessreport.andreafortuna.org](http://fitnessreport.andreafortuna.org) (actually works only with **Firefox** and **Chrome**): is made with a responsive layout, so can be visualized on mobile and desktop.

Obviously all [source code](http://git.andreafortuna.org/fitnessreport/src/) is available on my [GIT repository](http://git.andreafortuna.org/): suggestions and bug reports are welcome!
