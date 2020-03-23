---
layout: post
comments: true
date: 2020-03-23
title: "깃허브(Github)로 블로그 만들기 일지"
description: "Github 설치 및 jekyll 테마 적용하기"
subject: blog
tags:
  - jekyll
  - github
---

개발자로서 하루하루 공부하는 것들을 그냥 스치듯 넘기지 않고 기록해 둘 만한 나만의 블로그가 필요했다. 네이버 블로그는 너무 개인의, 일상 이야기만 있어서 개발자로서의 이야기를 담기에는 분위기가 너무 달랐다. 그래서 깃허브를 이용한 기술블로그를 만들기로 결심했다.

> **0. 깃허브 저장소 만들고, github desktop 설치하기**

우선 깃허브에서 저장소를 만들어야 하는데,
블로그를 만들기 위해서는 저장소 이름을
<code>아이디.github.io</code>로 만들어야 한다.
또한 github desktop을 설치한 후,
file > clone repository > URL를 통해 내 컴퓨터 내에 설치할
경로를 선택한 후 clone을 눌러주면 내 컴퓨터 내에
<code>아이디.github.io</code>라는 폴더가 생겼음을 알게 된다.
검색창에 아이디.github.io를 치면 새롭게 생성된 블로그가 확인된다.

> **1. jekyll 테마 적용하기**

jekyll에서 마음에 드는 테마를 고른 후, 해당 테마를 내 블로그에 가져와야 한다. 테마를 적용하는 방법은 여러가지가 있지만, 이 방법 저 방법 다 써본 필자로서 가장 쉬운 방법이 2가지가 있다.

1. 해당 테마의 깃허브에서 포크(Fork)하여 가져온 뒤, 저장소 이름을
   <code>아이디.github.io</code>로 만들기
2. 또는 해당 테마의 깃허브에서 전체 파일을 다운 받아 내 컴퓨터에 설치되었던 <code>아이디.github.io</code>내에 옮겨주면
   github desktop의 changes에 업데이트 내역이 뜨는데, Summery 부분에 적당히 적어주고, commit to master를 누른 후,
   상단 탭에서 Pull origin과 Fetch origin을 눌러주면
   깃허브 사이트 내의 내 저장소에도 업데이트 되고,
   내 블로그에도 테마가 적용됨을 알 수 있다.
