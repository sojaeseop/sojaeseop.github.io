---
layout: post
title:  "gdb: watchpoint 설정"
date:   2016-11-15 20:00:00 +0900
categories: dev-tools
tags: gdb,linux
excerpt: "GDB에서 watchpoint 설정하기"
---


- watch [-l|-location] expr [thread threadnum] [mask maskvalue]
	- 프로그램에서 변수를 write하는 시점에서 break 됨
- rwatch [-l|-location] expr [thread threadnum] [mask maskvalue]
	- 프로그램에서 변수를 read하는 시점에서 break 됨
- awatch [-l|-location] expr [thread threadnum] [mask maskvalue]
	- 프로그램에서 변수를 read/write 하는 시점에서 break 됨
- info watchpoints [n...]
	- watchpoint로 설정된 목록을 출력함

참고: <https://sourceware.org/gdb/onlinedocs/gdb/Set-Watchpoints.html>

