---
title: "Nvidia Screen Resolution Problem in Ubuntu 14.04"
layout: post
date: 2016-09-30
image: /assets/images/markdown.jpg
headerImage: false
tag:
- linux
- nvidia
category: blog
author: mkarayel
description: Nvidia Screen Resolution Problem in Ubuntu 14.04
---

1) Open the terminal.Type the below code in terminal and hit enter
{% highlight bash %}
$ sudo gedit /etc/default/grub
{% endhighlight %}
2) Edit GRUB_GFXMODE and add GRUB_GFXPAYLOAD
{% highlight bash %}
GRUB_GFXMODE=1024x768
GRUB_GFXPAYLOAD_LINUX=keep
{% endhighlight %}
3) Update grub 
{% highlight bash %}
$ sudo update-grub2
{% endhighlight %}
4) Reboot the system.
{% highlight bash %}
$ sudo reboot 
{% endhighlight %}
5) Now grub boot screen should have the resolution 1024x768.