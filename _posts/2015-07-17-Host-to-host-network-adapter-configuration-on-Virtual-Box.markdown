---
layout: post
title: Host to host network adapter configuration on Virtual Box
date: 2015-07-17 12:58 
categories: 
---

{% highlight bash %}
sudo /etc/network/interfaces

auto eth1
iface eth1 inet static
	address 192.168.56.102
	netmask 255.255.255.0
	network 192.168.56.0
	broadcast 192.168.56.255

sudo reboot
{% endhighlight %}