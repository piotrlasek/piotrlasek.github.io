---
layout: post
title: How to get back your WiFi key
date: 2015-07-14 08:40 
categories: 
---
{% highlight bash%}
netsh wlan show profile name=YourWiFi key=clear
{% endhighlight %}