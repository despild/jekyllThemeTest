---
layout: post
title:  "Mac에서 .DS_Store 처리하는 법"
date:   2017-01-10
categories: jekyll update
---

.DS_Store 파일은 폴더 및 파일 정보(아이콘 모양, 위치 등)를 가지고 있는 파일이라고 한다.
굳이 없어도 문제 없다.

일괄 삭제
{% highlight bash %}
sudo -s
find / -type f -name .DS_Store -print -delete
{% endhighlight %}

생성 방지

{% highlight bash %}
defaults write com.apple.desktopservices DSDontWriteNetworkStores true
{% endhighlight %}
