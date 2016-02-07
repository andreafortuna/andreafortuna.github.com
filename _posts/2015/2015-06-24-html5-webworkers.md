---
layout: post
title: "HTML5: Using WebWorkers"
description: "WebWorkers was created to allow execution of javaScript code asynchronously: can be compared to a thread that the webpage can launch and with which it can communicate through specific methods."
thumbnail: "http://www.andreafortuna.org/technology/images/webworkers.png"
category: Programming
tags: 
- Programming
- HTML5
- WebWorkers
- javascript

---
{% include JB/setup %}
WebWorkers was created to allow execution of javaScript code asynchronously: can be compared to a thread that the webpage can launch and with which it can communicate through specific methods.

![webworkers](http://www.andreafortuna.org/technology/images/webworkers.png)
<!-- more -->

A small disadvantage ... the WebWorkers not have access to the DOM: it must be seen as stand-alone applications, useful to perform challenging tasks without interrupt the current application.

A simple WebWorker
--

Let's see how to start a simple thread:

<script src="https://gist.github.com/andreafortuna/c11f197cb2f1e357ee87.js"></script>

Nothing complicated: the code in the file stepsToBeMade.js are executed and the return data are written in a log.
The data are sent back to the parent process (stepsToBeMade.js) by using the *postMessage* function:



<script src="https://gist.github.com/andreafortuna/77c7a429117ed756156e.js"></script>


All on one page?
--

We can choose not to use an external file to define the code of our webworker, packing up everything on a single page using a [Blob](https://developer.mozilla.org/en-US/docs/Web/API/Blob).

Then we declare a *script* element containing the code to be executed (a simple counter):


<script src="https://gist.github.com/andreafortuna/9b0a88dd65eca9156ee9.js"></script> 


and then we create and start the WebWorker from a blob filled with the contents of the *script* tag:

<script src="https://gist.github.com/andreafortuna/7fd6733382114d523339.js"></script> 

Putting it all together
--

Let's see the complete example:

<iframe width="100%" height="300" src="//jsfiddle.net/AndyFor/VdEzw/3/embedded/" allowfullscreen="allowfullscreen" frameborder="0"></iframe>

<p style="font-size:0.6em;float:right;">Italian version <a href="http://www.andreafortuna.org/2013/07/22/html5-i-web-workers/">here</a></p>