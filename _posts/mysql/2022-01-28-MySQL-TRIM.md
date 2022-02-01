---
title:  "[MySQL] 특정 문자를 제거하는 법 :: TRIM()"
excerpt: "DB에서 특정 문자를 제거하는 법을 알아보자"

categories:
  - MySQL
tags:
  - [COUNT()]

toc: true
classes: wide

sidebar:
  nav: "docs"

date: 2022-02-01
last_modified_at: 2022-02-01
---

### TRIM() 이란? ✨
---
전달받은 문자열의 앞이나 뒤, 또는 양쪽 모두에 있는 특정 문자를 제거합니다.<br>
TRIM() 함수에서 사용할 수 있는 지정자는 다음과 같습니다.<br>
|이름|설명|
|:----:|:----:|
|BOTH|전달받은 문자열의 양 끝에 존재하는 특정 문자를 제거합니다.(기본 설정)|
|LEADING|전달받은 문자열 앞에 존재하는 특정 문자를 제거합니다.|
|TRAILING|전달받은 문자열 뒤에 존재하는 특정 문자를 제거합니다.|
만약 지정자를 명시하지 않으면, 자동으로 BOTH로 설정됩니다.<br>
또한, 제거할 문자를 명시하지 않으면, 자동으로 공백을 제거하게 됩니다.

### 사용 예시 ✨
---
```
SELECT TRIM('   !!!MySQL PHP HTML Java!!!    '), 
TRIM(LEADING '!' FROM '!!!MySQL PHP HTML Java!!!')

실행 결과 >>
!!!MySQL PHP HTML Java!!!
MySQL PHP HTML Java!!!
```

```
공부하고 참고하여 기록해두는 개인 기록용 포스팅입니다!
🤔 부족한 부분이 많으니 감안하여 봐주시길 바랍니다. 🤔
```

[맨 위로 이동하기](#){: .btn }{: .align-right}