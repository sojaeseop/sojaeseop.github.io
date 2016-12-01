---
layout: post
title:  "gdb: print 설정"
date:   2016-12-01 14:20:00 +0900
categories: dev-tools
tags: gdb,linux
excerpt: "GDB에서 구조체 출력을 보기 쉽게 변경하기 (set print pretty on)"
---

gdb를 사용하면 변수의 내용을 확인할 때, print 명령을 사용한다.
print를 이용하여 구조체의 내용을 출력할 수 있는데, 기본 설정은 구조체 내용이 한 줄에 출력되어 보기에 어렵다.

구조체 내용을 출력 할 때 set print pretty를 사용하여 출력 포맷을 변경할 수 있다.

### 출력 관련된 명령어들

- set print pretty on
	- 구조체 내용을 각 줄에 출력하고 indent도 추가하여 알아보기 쉽다.
	- 다만, 여러줄에 걸쳐 출력되기 때문에 한눈에 보기 어려울 수 있다.

{% highlight bash %}
$1 = {
	next = 0x0,
	flags = \{
		sweet = 1,
		sour = 1
	},
	meat = 0x54 "Pork"
}
{% endhighlight %}

- set print pretty off
	- 구조체 내용을 한줄에 출력해 준다. (기본 포맷)

{% highlight bash %}
$1 = {next = 0x0, flags = {sweet = 1, sour = 1}, \\
meat = 0x54 "Pork"}
{% endhighlight %}

- set print array on
- set print array off
- set print union on
- set print union off


자세한 내용을 아래 링크를 참고하면 된다.

참고: <http://ftp.gnu.org/old-gnu/Manuals/gdb/html_node/gdb_57.html>

