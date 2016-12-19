---
layout: post
title:  "ffmpeg: 디인터레이스 필터 사용하기"
date:   2016-12-19 15:21:00 +0900
categories: linux
tags: [linux,ffmpeg,deinterlace]
excerpt: "ffmpeg에서 필터 사용하는 방법"
---
## 디인터레이스
참고: <https://ko.wikipedia.org/wiki/%EB%94%94%EC%9D%B8%ED%84%B0%EB%A0%88%EC%9D%B4%EC%8A%A4>

## ffmpeg
<https://ffmpeg.org/>

### 필터 사용하기
<https://ffmpeg.org/ffmpeg-filters.html>
* libavfilter를 통해서 필터 기능을 사용함.
* 예제
{% highlight bash %}
ffmpeg -i INPUT -vf "split [main][tmp]; [tmp] crop=iw:ih/2:0:0, vflip [flip]; [main][flip] overlay=0:H/2" OUTPUT
{% endhighlight %}

### yadif

* mode
	* 0: send_frame - 매 프레임마다 프레임을 출력
	* 1: send_field - 매 필드마다 프레임을 출력
	* 2: send_frame_nospatial - send_frame과 비슷하다는데 모르겠음
	* 3: send_field_nospatial - send_frame과 비슷하다는데 모르겠음
* parity
	* 0: top field first
	* 1: bottom field first
	* -1: 자동
* deint
	* 0: all
	* 1: interlaced

{% highlight bash %}
ffmpeg -i input -vf "yadif=0:-1:0" output 
# 0: mode=send_frame
# -1: parity=auto
# 0: deint=all
{% endhighlight %}

