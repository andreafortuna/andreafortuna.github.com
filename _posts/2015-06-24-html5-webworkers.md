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

{% highlight JavaScript %}

  var myWorker = new Worker('/path/operazioniDaEseguire.js');
    myWorker.onmessage = function(event) {
        console.log('Fatto, ecco i dati!', event.data);
    };
    
{% endhighlight %}    

Nothing complicated: the code in the file stepsToBeMade.js are executed and the return data are written in a log.
The data are sent back to the parent process (stepsToBeMade.js) by using the *postMessage* function:

{% highlight JavaScript %}

//stepsToBeMade.js
postMessage("So long, and thanks for all the fish.");

{% endhighlight %}    

All on one page?
--

We can choose not to use an external file to define the code of our webworker, packing up everything on a single page using a [Blob](https://developer.mozilla.org/en-US/docs/Web/API/Blob).

Then we declare a *script* element containing the code to be executed (a simple counter):


{% highlight JavaScript %}

<script id="myWorker">
    var i = 0;
    setInterval(function() {
        i++;
        postMessage(i);
    }, 1000);
</script>

{% endhighlight %}    


and then we create and start the WebWorker from a blob filled with the contents of the *script* tag:

{% highlight JavaScript %}

Blob([document.getElementById('myWorker').textContent], {
    type: "text/javascript"
});

myWorker = new Worker(window.URL.createObjectURL(workerData));
    myWorker.onmessage = function (e) {
        console.log('Counting...', event.data);
    };

{% endhighlight %}  

Putting it all together
--

Let's see the complete example:

<iframe width="100%" height="300" src="//jsfiddle.net/AndyFor/VdEzw/3/embedded/" allowfullscreen="allowfullscreen" frameborder="0"></iframe>

<p style="font-size:0.6em;float:right;">Italian version <a href="http://www.andreafortuna.org/2013/07/22/html5-i-web-workers/">here</a></p>