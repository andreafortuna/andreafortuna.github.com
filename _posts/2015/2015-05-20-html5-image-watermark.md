---
layout: post
title: "Apply a text watermark on images with HTML5 Canvas"
description: "A simple code snippet to watermarking images with HTML5 Canvas, and a complete browser tool"
category: Programming
tags: 
- Tips
- Programming
- HTML5
- Canvas
- javascript
- watermark

---
{% include JB/setup %}
Using the CANVAS object introduced by HTML5 we can do several operations  on images. Today we see how to apply a text watermark.

![jswatermark](http://oldsite.andreafortuna.org/images/jswatermark.PNG)
<!-- more -->

I have [already covered (in italian)](http://oldsite.andreafortuna.org/2013/05/24/html5-utilizzare-loggetto-canvas-per/) the topic in the past, but I explained how to apply a watermark using a logo in PNG. 
Now let's see how to apply a text watermark.

The extended project can be seen on [http://jswatermark.andreafortuna.org](http://jswatermark.andreafortuna.org): it's a  client-side tool for scaling images and applying watermark.

It's started as a custom application dedicated to the volunteers of the photographic section of the "[International Journalism Festival](http://www.festivaldelgiornalismo.com/) 2015" in Perugia  and then I decided to make it available to the public.

The 'heart' of the tool is collected  in the following snippet, in which the image is reduced to a maximum size of 800x600 pixels, and is applied a translucent watermark text in the lower right of the picture:

<script src="https://gist.github.com/andreafortuna/3747ecef491d6eb344a1.js"></script>

The full source code is available on my git repository on bitbucket: [https://bitbucket.org/andreafortuna/watermarktool/](https://bitbucket.org/andreafortuna/watermarktool/src).

