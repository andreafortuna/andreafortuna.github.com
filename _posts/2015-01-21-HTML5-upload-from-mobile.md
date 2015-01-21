---
layout: post
title: "HTML5: take a photo and upload them from mobile phone browser"
description: "Simple tutorial: take a photo and upload them from mobile phone browser"
category: Programming
tags: 
- HTML5
- PHP
- Javascript
---
{% include JB/setup %}
Yesterday, a colleague asked me: 

>"Andy, I need to make a simple mobile application that takes a picture and sends it to my webserver. It's too difficult?"

Obviously no, with a little bit of HTML5. ;-)

![HTML5](/images/HTML5Common.png)

<!-- more -->
Let's start making an HTML page with a simple form that permits the user to select or take a photo using the phone camera:

{% highlight html %}
<!DOCTYPE html>
<html>
<head>
    <title>Take or select photo(s)</title>
    <script type="text/javascript">
      function fileSelected() {
        var count = document.getElementById('fileToUpload').files.length;
              document.getElementById('details').innerHTML = "";
              for (var index = 0; index < count; index ++)
              {
                     var file = document.getElementById('fileToUpload').files[index];
                     var fileSize = 0;
                     if (file.size > 1024 * 1024)
                            fileSize = (Math.round(file.size * 100 / (1024 * 1024)) / 100).toString() + 'MB';
                     else
                            fileSize = (Math.round(file.size * 100 / 1024) / 100).toString() + 'KB';
                     document.getElementById('details').innerHTML += 'Name: ' + file.name + '<br>Size: ' + fileSize + '<br>Type: ' + file.type;
                     document.getElementById('details').innerHTML += '<p>';
              }
      }
      function uploadFile() {
        var fd = new FormData();
              var count = document.getElementById('fileToUpload').files.length;
              for (var index = 0; index < count; index ++)
              {
                     var file = document.getElementById('fileToUpload').files[index];
                     fd.append('myFile', file);
              }
        var xhr = new XMLHttpRequest();
        xhr.upload.addEventListener("progress", uploadProgress, false);
        xhr.addEventListener("load", uploadComplete, false);
        xhr.addEventListener("error", uploadFailed, false);
        xhr.addEventListener("abort", uploadCanceled, false);
        xhr.open("POST", "savetofile.php");
        xhr.send(fd);
      }
      function uploadProgress(evt) {
        if (evt.lengthComputable) {
          var percentComplete = Math.round(evt.loaded * 100 / evt.total);
          document.getElementById('progress').innerHTML = percentComplete.toString() + '%';
        }
        else {
          document.getElementById('progress').innerHTML = 'Upload error!';
        }
      }
      function uploadComplete(evt) {
        alert(evt.target.responseText);
      }
      function uploadFailed(evt) {
        alert("Error sendin file...");
      }
      function uploadCanceled(evt) {
        alert("Upload cancelled by the user or network error!");
      }
    </script>
</head>
<body>
  <form id="form1" enctype="multipart/form-data" method="post" action="savetofile.php">
    <div>
      <label for="fileToUpload">Take or select photo(s)</label><br />
      <input type="file" name="fileToUpload" id="fileToUpload" onchange="fileSelected();" accept="image/*" />
    </div>
    <div id="details"></div>
    <div>
      <input type="button" onclick="uploadFile()" value="Upload" />
    </div>
    <div id="progress"></div>
  </form>
</body>
</html>
{% endhighlight %}

We use the attribute 

> "accept="image/*" 

to say to mobile browser to set the INPUT tag to accept images from camera roll or camera app, and some javascript to display a simple upload progress.

Server side, the PHP script is dramatically simple:

{% highlight php %}

<?php
if (isset($_FILES['myFile'])) {
    // Example:
    move_uploaded_file($_FILES['myFile']['tmp_name'], "uploads/" . $_FILES['myFile']['name']);
    echo 'Upload completed!';
}
?>
{% endhighlight %}

That's all!

The [complete source](http://git.andreafortuna.org/html5-mobile-upload/src) is available on my [GIT repository](http://git.andreafortuna.org/).

