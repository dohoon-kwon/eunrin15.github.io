---
title:  "[MySQL] 문자열 결합하는 법 :: CONCAT()"
excerpt: "문자열 결합하는 법을 알아보자"

categories:
  - MySQL
tags:
  - [CONCAT()]

toc: true
classes: wide

sidebar:
  nav: "docs"

date: 2022-02-01
last_modified_at: 2022-02-01
---

### 1️⃣ CONCAT() 이란?
---

전달받은 문자열을 모두 결합하여 하나의 문자열로 반환합니다.<br>
만약 전달받은 문자열 중 하나라도 NULL이 존재하면, NULL을 반환합니다.

### 2️⃣ 예시
---

```
SELECT CONCAT('Ora', 'cle Cor', 'poration'), 
CONCAT('Oracle', NULL, 'Corporation');
```

실행결과 >>
```
Oracle Corporation
NULL
```

```
공부하고 참고하여 기록해두는 개인 기록용 포스팅입니다!
🤔 부족한 부분이 많으니 감안하여 봐주시길 바랍니다. 🤔
```

[맨 위로 이동하기](#){: .btn }{: .align-right}