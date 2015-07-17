---
layout: post
title: "How to install vboxsf on Ubuntu machine"
date: 2015-05-11 12:00:00
categories: 
---

{% highlight bash%}
Mount disk: VBoxGuestAdditions.iso
sudo mount /dev/cdrom /mnt
sudo VBoxLinuxAdditions.run
sudo apt-get install dkms
sudo /etc/init.d/vboxadd setup
sudo mount -t vboxsf -o uid=$UID,gid=$(id -g) Shared ~/Shared
{% endhighlight %}