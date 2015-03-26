---
layout: post
title: "Facebook Fitness Report: a small update"
description: "Accessing opengraph fitness data through facebook API"
category: Programming
tags: 
- Running
- Facebook
- Opengraph
- Javascript
---
{% include JB/setup %}

A very small update of my 'runner-oriented' webapp [Facebook Fitness Report](http://fitnessreport.andreafortuna.org).

![screenshot](http://www.andreafortuna.org/images/fitnessReportScreenshot2.PNG)
<!-- more -->

With a [single line](http://git.andreafortuna.org/fitnessreport/src/c4c57afa559ca09680c8a93d82a5b360f5dc7c26/js/main.js?at=master#cl-112) of code i have resolved a bug that caused an incompatibility with Internet Explorer:

```
courseDate = courseDate.replace("+0000","");
```

(Internet Explorer have some problems parsing datetime from opengraph feed) 

I have introduced also a Facebook sharing button, that permits to share a simple report of the year's workouts.

![sharing tool](http://www.andreafortuna.org//images/FacebookSharing.PNG)


The updated [source code](http://git.andreafortuna.org/fitnessreport/src/) is available on my [GIT repository](http://git.andreafortuna.org/).
