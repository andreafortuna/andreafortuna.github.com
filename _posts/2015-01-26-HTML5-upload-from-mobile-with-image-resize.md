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
Today, the same colleague of [previous post](/programming/2015/01/21/HTML5-upload-from-mobile/), tell me: 

>"Your script works great, but if i take a very big image, the upload with 3G data network is sooooo slow! It's possible to resize the image BEFORE the upload?"

Yes, it's possible!

![HTML5](/images/resize.jpg)

<!-- more -->
Using the [File API](https://developer.mozilla.org/en-US/docs/Using_files_from_web_applications), and processing the images with the [canvas element](https://developer.mozilla.org/en-US/docs/Web/API/Canvas_API/Tutorial/Using_images), we can resize the image before upload it.

Here a small snippet:

{% highlight javascript %}

function doUpload() {
        var file = document.getElementById('fileToUpload').files[0];
        var dataUrl = "";
        // Create an image
        var img = document.createElement("img");
        // Create a file reader
        var reader = new FileReader();
        // Set the image once loaded into file reader
        reader.onload = function(e)
        {
            img.src = e.target.result;
    
            var canvas = document.createElement("canvas");
            //var canvas = $("<canvas>", {"id":"testing"})[0];
            var ctx = canvas.getContext("2d");
            ctx.drawImage(img, 0, 0);
    
            // Set Width and Height
            var MAX_WIDTH = 400;
            var MAX_HEIGHT = 300;
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
            var ctx = canvas.getContext("2d");
            ctx.drawImage(img, 0, 0, width, height);
    
            dataUrl = canvas.toDataURL("image/png");
            document.getElementById('image_preview').src = dataUrl;    
            
            // Post the data
            var fd = new FormData();
            fd.append("image", dataUrl);
    
            var xhr = new XMLHttpRequest();
            xhr.upload.addEventListener("progress", uploadProgress, false);
            xhr.addEventListener("load", uploadComplete, false);
            xhr.addEventListener("error", uploadFailed, false);
            xhr.addEventListener("abort", uploadCanceled, false);
            xhr.open("POST", "savetofile.php");
            xhr.send(fd);
            
        }
        // Load files into file reader
        reader.readAsDataURL(file);
      }

{% endhighlight %}

In this example, the size of image is forced to 400x300 pixels.

It's required also a simple change on **savetofile.php**:

{% highlight javascript %}
<?php
if (isset($_POST['image'])) {
    file_put_contents("uploads/".rand().".png",base64_decode(str_replace("data:image/png;base64,","", $_POST['image'])));
    echo 'Upload completed!';
}
?>
{% endhighlight %}

In this version of the script, the image is posted to the form as base64 array, and needs to be decoded when it arrives on server.

The [updated source](http://git.andreafortuna.org/html5-mobile-upload/src) is available on my [GIT repository](http://git.andreafortuna.org/).

