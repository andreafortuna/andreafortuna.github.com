---
layout: post
title: "Tips: using PV instead of CP to copy large files"
description: ""
category: Tips
tags: 
- Bash
- Linux
---
{% include JB/setup %}
*Pv* (Pipe Viewer) is a command line utility that allows us to monitor the progress of data through a pipe.

It could be used to monitor some long operations performed by utility that not display a progress output  (like *DD*).

![Linux Console](http://icons.iconarchive.com/icons/graphicpeel/utilize/512/Terminal-icon.png)

<!-- more -->


With a simple trick, can be used also to display a progress bar and speed monitoring when copying a very large file, with this command:

```bash
pv /oldfolder/file > /newfolder/file
```


Some other usage of PV:

<iframe width="640" height="480" src="//www.youtube.com/embed/mTwBlPqRZO8" frameborder="0" allowfullscreen></iframe>

[PV man page](http://linux.die.net/man/1/pv)