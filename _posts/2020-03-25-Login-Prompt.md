---
layout: post
title: javaScript Study <Prompt와 If문으로 Login구조 만들기>
tags:
  - javaScript
---

아래 Schema에 나온 알고리즘을 이용해 간단한 Prompt창을 띄워 
If문에 맞게 로그인 구조를 만들 수 있다. 
아무것도 입력하지 않았을 경우는 ""이나 null을 응용해 보면 된다. 
단, undefined는 값이 할당되지 않았을 때 컴퓨터 내에서 알려주는 값이므로 
빈 값을 인위적으로 할당할 때에는 null을 이용해야 한다. 


# 문제
브라우저 창을 열면 바로 "누구신가요?"창이 뜨며 (default값은 아무 값도 없음).
<ol style="font-size:0.9rem">
  <li>Admin 이라는 올바른 답을 적으면 패스워드 묻는 창으로</li>
  <li>아무것도 입력하지 않았거나 취소를 누르면 "취소되었습니다."가 출력됨.</li>
  <li>틀린 값을 넣으면 "아이디가 틀렸습니다."가 출력됨</li>
</ol>

1번대로 올바른 답을 적었을 때 <u>패스워드를 묻는 창</u>에서
<ol style="font-size:0.9rem">
  <li>Master라는 올바른 답을 적으면 "환영합니다!"가 출력됨</li>
  <li>아무것도 입력하지 않았거나 취소를 누르면 "취소되었습니다."</li>
  <li>틀린 값을 넣으면 "패스워드가 틀렸습니다."</li>
</ol>

**The Schema:**
<br>
<img src="https://user-images.githubusercontent.com/61853524/77509803-be0c5480-6eb0-11ea-97ff-bf58c61f52c0.png" style="text-align:center"></img>

출처: [https://javascript.info/task/check-login](#)

# 해답

```css
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
```
