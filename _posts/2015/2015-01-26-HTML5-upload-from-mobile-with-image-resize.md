---
layout: post
title: "HTML5: resize a photo before upload"
description: "Simple tutorial: resize a photo before upload"
category: Programming
tags: 
- HTML5
- PHP
- Javascript
---
{% include JB/setup %}
Today, the same colleague of [previous post](http://www.andreafortuna.org/programming/2015/01/21/HTML5-upload-from-mobile/), tell me: 

>"Your script works great, but if i take a very big image, the upload with 3G data network is sooooo slow! It's possible to resize the image BEFORE the upload?"

Yes, it's possible!

![HTML5](http://www.andreafortuna.org/images/resize.jpg)

<!-- more -->
Using the [File API](https://developer.mozilla.org/en-US/docs/Using_files_from_web_applications), and processing the images with the [canvas element](https://developer.mozilla.org/en-US/docs/Web/API/Canvas_API/Tutorial/Using_images), we can resize the image before upload it.

Here a small snippet:

<script src="https://gist.github.com/andreafortuna/fa4ab910e72bc6e3882a.js"></script>

In this example, the size of image is forced to 400x300 pixels.

It's required also a simple change on **savetofile.php**:

<script src="https://gist.github.com/andreafortuna/b5da306503fa3cbcfa0f.js"></script>


In this version of the script, the image is posted to the form as base64 array, and needs to be decoded when it arrives on server.

The [updated source](https://bitbucket.org/andreafortuna/html5-mobile-upload/src) is available on my [GIT repository](https://bitbucket.org/andreafortuna/).

