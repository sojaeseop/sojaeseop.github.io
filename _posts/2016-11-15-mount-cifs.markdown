---
layout: post
title:  "mount: cifs 마운트 하기"
date:   2016-11-15 21:00:00 +0900
categories: linux
tags: linux,mount,cifs
excerpt: "cifs 마운트 하기"
---

### 명령어

{% highlight bash %}
mount.cifs {service} {mount-point} [-o options]
{% endhighlight %}

### 예제

{% highlight bash %}
mount -t cifs -o user='username',password='password' //site/path /mnt/smb
{% endhighlight %}

참고: <https://www.samba.org/samba/docs/man/manpages-3/mount.cifs.8.html>

