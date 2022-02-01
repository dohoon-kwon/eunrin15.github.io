---
title:  "[MySQL] 테이블에 레코드 추가하는 법 :: INSERT"
excerpt: "DB에서 테이블에 레코드 추가하는 법을 알아보자"

categories:
  - MySQL
tags:
  - [INSERT]

toc: true
classes: wide

sidebar:
  nav: "docs"

date: 2022-02-01
last_modified_at: 2022-02-01
---

### 1️⃣ INSERT문 이란?
---

TABLE에 새로운 레코드값을 추가하고자 할때 사용하는 문법입니다.<br>
INSERT INTO 문과 함께 VALUES 절을 사용하여 해당 테이블에 새로운 레코드를 추가할 수 있습니다.

### 2️⃣ 레코드 값 추가하는 법
---

```
INSERT INTO 테이블이름
VALUES (데이터값1, 데이터값2, 데이터값3, ...)
```

### 3️⃣ 특정 칼럼만 값을 넣어 레코드 추가
---

특정 칼럼과 값의 순서를 매칭시켜 레코드를 추가할 수 있습니다.

```
INSERT INTO 테이블이름(필드이름1, 필드이름2, 필드이름3, ...)
VALUES (데이터값1, 데이터값2, 데이터값3, ...)
```

### 4️⃣ 제외할 수 있는 칼럼 값 예시
---

생략할 수 있는 필드는 다음과 같습니다.<br>

1. NULL을 저장할 수 있도록 설정된 필드<br>
2. DEFAULT 제약 조건이 설정된 필드<br>
3. AUTO_INCREMENT 키워드가 설정된 필드

```
공부하고 참고하여 기록해두는 개인 기록용 포스팅입니다!
🤔 부족한 부분이 많으니 감안하여 봐주시길 바랍니다. 🤔
```

[맨 위로 이동하기](#){: .btn }{: .align-right}