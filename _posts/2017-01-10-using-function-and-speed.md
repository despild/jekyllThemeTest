---
layout: post
title:  "C 에서 User Defined function의 사용과 실행 속도"
date:   2017-01-10
categories: jekyll update
---

Thread안의 While Loop에서 switch를 사용하여 State에 따라 각각 다른 Function을 수행하도록 되어있다.
3D 프린터의 경우 Gcode를 전송 받으면 ok라는 문구를 되돌려줘 해당 gcode의 수신 여부를 알려주는데, 이 ok를 파싱해서 체크하는 루틴을 function으로 만들어 사용하고 있었음.

처음에는 링 버퍼를 okCheck 함수 내에서 직접 체크해서 길이가 좀 길어 따로 함수를 만들어 사용하였으나 후에 serial read하는 부분에서 read와 동시에 체크를 하고 체크한 카운터의 수만 증가시켜 단순 if문이 되도록 하여 해당 함수를 만들어 사용하는게 더 비효율 적이었다.

함수를 새로 정의해서 함수를 찾아 들어가고 나오는데에 소모되는 시간이 gcode 전송에는 생각보다 많은 영향을 미치더라