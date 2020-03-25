---
layout: post
title: javaScript Study "Prompt와 If문으로 Login구조 만들기"
tags:
  - javaScript
---

> **문제**
> 브라우저 창을 열면 바로 "누구신가요?"창이 뜨며 (default값은 아무 값도 없음).

1. Admin 이라는 올바른 답을 적으면 패스워드 묻는 창으로
2. 아무것도 입력하지 않았거나 취소를 누르면 "취소되었습니다." 가 출력됨.
3. 잘못된 값을 넣으면 "아이디가 틀렸습니다."가 출력됨

1번대로 올바른 답을 적었을 때 패스워드가 묻는 창에서

1. Master라는 올바른 답을 적으면 "환영합니다!"가 출력됨
2. 아무것도 입력하지 않았거나 취소를 누르면 "취소되었습니다."
3. 잘못도니 값을 넣으면 "패스워드가 틀렸습니다."

The Schema:{: .center}
출처: [https://javascript.info/task/check-login]#

> **해답**
> '''css

<script>
      let login = prompt("누구신가요?", "");
      if (login === "Admin") {
        let pwd = prompt("비밀번호를 입력해 주세요.", "");
        if (pwd === "Master") {
          alert("환영합니다!");
        } else if (pwd === "" || pwd === null) {
          alert("취소되었습니다.");
        } else {
          alert("패스워드가 틀렸습니다.");
        }
      } else if (login === "" || login === null) {
        alert("취소되었습니다.");
      } else {
        alert("아이디가 틀렸습니다.");
      }
    </script>

'''
