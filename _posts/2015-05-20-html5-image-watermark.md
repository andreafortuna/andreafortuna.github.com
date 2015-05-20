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

![jswatermark](/images/jswatermark.PNG)
<!-- more -->

I have [already covered (in italian)](http://www.andreafortuna.org/2013/05/24/html5-utilizzare-loggetto-canvas-per/) the topic in the past, but I explained how to apply a watermark using a logo in PNG. 
Now let's see how to apply a text watermark.

The extended project can be seen on [http://jswatermark.andreafortuna.org](http://jswatermark.andreafortuna.org): it's a  client-side tool for scaling images and applying watermark.

It's started as a custom application dedicated to the volunteers of the photographic section of the "[International Journalism Festival](http://www.festivaldelgiornalismo.com/) 2015" in Perugia  and then I decided to make it available to the public.

The 'heart' of the tool is collected  in the following snippet, in which the image is reduced to a maximum size of 800x600 pixels, and is applied a translucent watermark text in the lower right of the picture:

{% highlight JavaScript %}

    // Create an image
    var img = document.createElement("img");
    // Create a file reader
    var reader = new FileReader();
    // Set the image once loaded into file reader
    reader.onload = function(e)
    {
        img.src = e.target.result;
    	img.onload = function() {
                var canvas = document.createElement("canvas");
                var ctx = canvas.getContext("2d");
                ctx.drawImage(img, 0, 0);
        
                // Set Width and Height
                var MAX_WIDTH = 800;
                var MAX_HEIGHT = 600;
                var width = img.width;
                var height = img.height;
        
                if (width > height) {
                  if (width > MAX_WIDTH) {
                    height *= MAX_WIDTH / width;
                    width = MAX_WIDTH;
                  }
                } else {
                  if (height > MAX_HEIGHT) {
                    width *= MAX_HEIGHT / height;
                    height = MAX_HEIGHT;
                  }
                }
                canvas.width = width;
                canvas.height = height;
                ctx.drawImage(img, 0, 0, width, height);
        		ctx.fillStyle = "rgba(204, 204, 204, 0.5)";
        		
          ctx.font = "30pt Calibri";
          var waterMarkText = document.getElementById("phName").value;
     	  ctx.fillText(waterMarkText, width - (waterMarkText.length * 19), height - 20);
          
          dataUrl = canvas.toDataURL("image/png");
          document.getElementById('image_preview').src = dataUrl;  
          
          document.getElementById('downloadImage').href = dataUrl; 
           document.getElementById('downloadImage').click();
    		if (fileIndex < allFiles-1) {
    			fileIndex ++;
    			doUploadW(fileIndex);
    		} else {
    			location.reload();
    		}
      }    
        
    }
    // Load files into file reader
    reader.readAsDataURL(file);

{% endhighlight %}

The full source code is available on my git repository on bitbucket: [https://bitbucket.org/andreafortuna/watermarktool/](https://bitbucket.org/andreafortuna/watermarktool/src).

