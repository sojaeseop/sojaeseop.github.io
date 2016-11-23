---
layout: post
title:  "minicom: linewrap on/off"
date:   2016-11-15 22:00:00 +0900
categories: linux
tags: linux,minicom,linewrap
excerpt: "minicom에서 linewrap on/off 하는 방법: ctrl-a, w"
---

- minicom으로 serial을 연결하여 console 출력을 할 경우에 화면을 넘어가서 잘리는 경우가 발생함
- minicom 옵션에서 linewrap을 on으로 변경하면 colum width를 넘어가는 내용이 줄바꿈되어 출력됨

### linewrap on/off 단축키
{% highlight bash %}
CTRL-A W
{% endhighlight %}

단축키(ctrl-a w)로 on/off 할 경우에 하단 상태표시줄에 Linewrap ON/Linewrap OFF 메시지가 일시적으로 출력되니 on/off 상태를 참고하면 됨
