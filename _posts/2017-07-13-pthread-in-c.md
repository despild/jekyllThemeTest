---
layout: post
title:  "C에서 pthread를 사용했을때 컴파일 에러나는 경우"
date:   2017-07-13 12:44:32 +0900
categories: jekyll update
tag: study c programing
---

pthread를 C에서 사용하고 그냥 gcc로 컴파일 할 경우 **undefined reference to `pthread_join'** 라는 에러가 뜨면서 컴파일이 안되는 경우가 있음

옵션으로 -lpthread 넣어주면 해결 됨
