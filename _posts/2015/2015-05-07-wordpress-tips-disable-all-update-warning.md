---
layout: post
title: "Wordpress tips: disable all update notifications without plugins"
description: "Disable Update Notifications and Maintenance Nags in WordPress"
category: Programming
tags: 
- Wordpress
- PHP
- Tips


---
{% include JB/setup %}
In some configurations with special customizations, updating wordpress cannot/must be made.

How to disable the update messages without using a [special plug-in](https://wordpress.org/plugins/disable-wordpress-updates/)?

![Wordpress](http://www.andreafortuna.org/images/wordpress.jpg)
<!-- more -->

With a simple snippet! Paste this code in ***function.php*** of the active theme:

{% highlight PHP %}

function remove_core_updates(){
   global $wp_version;
   return(object) array('last_checked'=> time(),'version_checked'=> $wp_version,);
}
add_filter('pre_site_transient_update_core','remove_core_updates');
add_filter('pre_site_transient_update_plugins','remove_core_updates');
add_filter('pre_site_transient_update_themes','remove_core_updates');

{% endhighlight %}
