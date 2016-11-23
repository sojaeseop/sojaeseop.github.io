---
layout: post
title:  "ctags: 사용법"
date:   2016-11-15 19:00:00 +0900
categories: dev-tools
tags: ctags,vi,linux
excerpt: "ctags 간단 사용법: ctags -R"
---
## tag 파일 생성하기
### 현재 디렉토리에서 tag 파일 생성하기

{% highlight bash %}
ctags *
{% endhighlight %}

### 하위폴더를 포함하여 tag 파일 생성하기

{% highlight bash %}
ctags -R
{% endhighlight %}

## vi에서 사용하기

|---
|vi -t tag|"tag"를 검색해서 해당 태그의 위치(파일,라인)에서 vi를 시작
|:ta tag|vi에서 "tag"를 검색
|Ctrl-]|커서 위치의 태그를 검색
|Ctrl-t|태그로 점프하기 전 위치로 돌아옴
|===
{:.tablestyle}

---

참고:

- ctags manual: <http://ctags.sourceforge.net/ctags.html>
