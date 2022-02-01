---
title:  "[MySQL] 레코드를 선택하는 법 :: SELECT"
excerpt: "DB에서 레코드를 선택하는 법을 알아보자"

categories:
  - MySQL
tags:
  - [SELECT]

toc: true
classes: wide

sidebar:
  nav: "docs"

date: 2022-02-01
last_modified_at: 2022-02-01
---

### 1️⃣ SELECT문 이란?
---
SELECT 문을 사용하여 테이블의 레코드를 선택할 수 있습니다.
다음은 기본 형식 예시입니다.

```
SELECT 필드이름
FROM 테이블이름
[WHERE 조건]
```

FROM 절은 레코드를 선택할 테이블의 이름을 명시합니다.<br>
해당 테이블에서 선택하고 싶은 필드의 이름을 SELECT 키워드 바로 뒤에 명시하면 됩니다.<br>
이때 WHERE 절을 사용하면, 선택할 레코드의 조건을 좀 더 상세히 설정할 수 있습니다.<br>

### 2️⃣ 테이블의 모든 필드 선택
---

SELECT 문과 함께 별표(*) 기호를 사용하면, 해당 테이블의 모든 필드를 선택할 수 있습니다.

```
SELECT *
FROM 테이블명;
```

### 3️⃣ 특정 조건의 레코드 선택
---
SELECT 문과 함께 WHERE절을 사용하면, 검색할 레코드의 조건을 설정할 수 있습니다.<br>
이러한 WHERE 절은 테이블의 크기가 매우 크거나, 특정 조건에 맞는 레코드만을 선택하고 싶을 때 유용하게 사용됩니다.<br>

```
SELECT *
FROM 테이블명
WHERE Name = '찾는 조건';
```

이러한 WHERE 절에는 여러 개의 조건을 같이 명시할 수도 있습니다.<br>
이때 여러 개의 조건은 AND나 OR 연산자를 이용하여 연결합니다.

```
SELECT *
FROM 테이블명
WHERE ID <= 3 AND ReserveDate > '2016-02-01';
```

### 4️⃣ 특정 필드만을 선택
---

SELECT 키워드 다음에 필드 이름을 명시하면, 해당 테이블의 특정 필드만을 불러올 수 있습니다.<br>
이때 쉼표(,)를 사용하여 여러 개의 필드 이름을 한 번에 명시할 수 있습니다.

```
SELECT 칼럼1, 칼럼2
FROM 테이블명;
```

### 5️⃣ 중복되는 값 제거 ❌
---

만약 같은 필드에 중복되는 값을 가지는 레코드가 있다면, DISTINCT 키워드를 사용하여 그 값이 한 번만 선택되도록 설정할 수 있습니다.<br>
DISTINCT 키워드를 사용하면 중복된 값은 단 한 번만 선택됩니다.

```
SELECT DISTINCT 칼럼명
FROM 테이블명;
```

### 6️⃣ 선택한 결과의 정렬
---

SELECT 문으로 선택한 결과를 ORDER BY 절을 사용하여 정렬할 수 있습니다.<br>
ORDER BY 절의 기본 설정은 오름차순이며, ASC 키워드를 사용하여 직접 오름차순을 명시할 수도 있습니다.<br>
만약 내림차순으로 정렬하고자 할 때는 맨 마지막에 DESC 키워드를 추가하면 됩니다.

```
SELECT * 
FROM 테이블명
ORDER BY 정렬할 칼럼명;

/* 내림차순 */
SELECT * 
FROM 테이블명
ORDER BY 정렬할 칼럼명DESC;

/* 종합 */
SELECT *
FROM 테이블명
ORDER BY 정렬할 칼럼명1 DESC, 정렬할 칼럼명2 ASC;
```

### 7️⃣ 별칭(alias)을 이용한 처리

---

MySQL에서는 테이블과 필드에 임시로 별칭(alias)을 부여하고, 해당 별칭을 SELECT 문에서 사용할 수 있습니다.<br>
이러한 별칭(alias)은 복잡한 테이블 이름이나 필드의 이름을 좀 더 읽기 쉽도록 만들어 줍니다.<br>
첫 번째 문법은 해당 필드에 새로운 별칭을 부여하고, 두 번째 문법은 해당 테이블에 새로운 별칭을 부여하는 문법입니다.

```
1. SELECT 필드이름 AS 별칭
	 FROM 테이블이름;

2. SELECT 필드이름
	 FROM 테이블이름 AS 별칭;
```

### 8️⃣ Reservation 테이블의 RoomNum 필드와 Name 필드에 하나의 새로운 별칭을 부여하는 예제
---

```
SELECT ReserveDate, CONCAT(RoomNum, " : ", Name) AS ReserveInfo
FROM Reservation;
```

![https://s3-us-west-2.amazonaws.com/secure.notion-static.com/fedacde3-c7cf-4f00-ab4f-1c6860bbe2e8/Untitled.png](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/fedacde3-c7cf-4f00-ab4f-1c6860bbe2e8/Untitled.png)

CONCAT() 함수는 인수로 전달받은 문자열을 모두 결합하여 하나의 문자열로 반환하는 함수입니다.

```
공부하고 참고하여 기록해두는 개인 기록용 포스팅입니다!
🤔 부족한 부분이 많으니 감안하여 봐주시길 바랍니다. 🤔
```

[맨 위로 이동하기](#){: .btn }{: .align-right}