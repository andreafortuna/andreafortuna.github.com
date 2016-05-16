---
layout: post
title: "HTML5: take a photo and upload it from mobile phone browser"
description: "Simple tutorial: take a photo and upload it from mobile phone browser"
category: Programming
tags: 
- HTML5
- PHP
- Javascript
---
{% include JB/setup %}

**UPDATED on 2015-01-26 with [Image Resize](/programming/2015/01/26/HTML5-upload-from-mobile-with-image-resize/)**

***

Yesterday, a colleague asked me: 

>"Andy, I need to make a simple mobile application that takes a picture and sends it to my webserver. It's too difficult?"

Obviously no, with a little bit of HTML5. ;-)

![HTML5](http://oldsite.andreafortuna.org/images/HTML5Common.png)

<!-- more -->
Let's start making an HTML page with a simple form that permits the user to select or take a photo using the phone camera:

<script src="https://gist.github.com/andreafortuna/a83737513a1f9a5529ce.js"></script>

We use the attribute 

> "accept="image/*" 

to say to mobile browser to set the INPUT tag to accept images from camera roll or camera app, and some javascript to display a simple upload progress.

Server side, the PHP script is dramatically simple:

<script src="https://gist.github.com/andreafortuna/8f7927e2787064b8bb59.js"></script>

That's all!

The [complete source](http://git.andreafortuna.org/html5-mobile-upload/src) is available on my [GIT repository](http://git.andreafortuna.org/).

