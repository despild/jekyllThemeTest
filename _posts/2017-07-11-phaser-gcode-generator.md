---
layout: post
title:  "[구상]Phaser Gcode Generator"
date:   2017-07-11 18:17:19 +0900
categories: jekyll update
---

Phaser를 이용해서 탑다운 뷰로 캐릭터를 이동 시켜 툴패스를 만들어보자

필요하다고 생각 되는 기능은 다음과 같음
- 움직이는 경로에 대한 마킹
- 패스 최적화(Smoothing / polygonize)
- Extrude amount 계산
- File writing
- Extrude Enable Push Key
- Layer Shift Key
- Generate Button
- Cursor Character
- Output Download
- Build Plate Setting
- Nozzle Size Setting
- Nozzle Temp / Bed Temp Setting
- Done Key
- Start Key

우선적으로 주어진 패스에 대한 압출량을 계산해서 Gcode로 파싱하는 모듈 또는 함수가 필요할거 같음

------- 추후에 계속 -------
