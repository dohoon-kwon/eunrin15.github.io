---
title:  "[MySQL] 테이블의 레코드를 삭제하는 법 :: DELETE"
excerpt: "DB에서 테이블의 레코드를 삭제하는 법을 알아보자"

categories:
  - MySQL
tags:
  - [DELETE]

toc: true
classes: wide

sidebar:
  nav: "docs"

date: 2022-02-01
last_modified_at: 2022-02-01
---

### 1️⃣ DELETE문 이란?
---

DB에서 레코드를 지우고 싶은 경우 사용하는 문법입니다.<br>
DELETE 문은 해당 테이블에서 WHERE 절의 조건을 만족하는 레코드만을 삭제합니다.<br>
즉, 테이블에서 명시된 필드와, 그 값이 일치하는 레코드만을 삭제해 줍니다.<br>
만약 WHERE 절을 생략하면, 해당 테이블에 저장된 모든 데이터가 삭제됩니다.

### 2️⃣ 전체 레코드 삭제
---

다음 예시는 해당 테이블의 모든 레코드를 삭제하는 법입니다.

```
DELETE FROM 테이블이름;
```



### 3️⃣ 특정 조건의 레코드 삭제
---

다음 예시는 해당 테이블에서 WHERE 절의 조건을 만족하는 레코드의 값만을 삭제합니다.

```
DELETE FROM 테이블이름
WHERE 필드이름=데이터값
```

### 4️⃣ 테이블까지 삭제하는 법
---

이때 테이블에 저장된 모든 데이터가 삭제되더라도 테이블은 여전히 남아있게 됩니다.<br>
해당 테이블까지 삭제하고 싶을 때는 DROP TABLE 문을 사용해야 합니다.

```
공부하고 참고하여 기록해두는 개인 기록용 포스팅입니다!
🤔 부족한 부분이 많으니 감안하여 봐주시길 바랍니다. 🤔
```

[맨 위로 이동하기](#){: .btn }{: .align-right}