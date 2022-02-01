---
title:  "[MySQL] 레코드의 개수 구하기(COUNT())"
excerpt: "레코드의 개수 구하기(COUNT())"

categories:
  - MySQL
tags:
  - [MySQL, COUNT]

toc: true
classes: wide

sidebar:
  nav: "docs"

date: 2022-01-28
last_modified_at: 2022-01-28
---

### 전체 행 갯수 가져오기

```
SELECT COUNT(*) FROM 테이블;
```

### 컬럼 데이터 갯수 가져오기

```
SELECT COUNT(컬럼) FROM 테이블;
```

### 쿼리

```
SELECT COUNT(*) as cnt FROM hero_collection;
```

```
공부하고 참고하여 기록해두는 개인 기록용 포스팅입니다!
🤔 부족한 부분이 많으니 감안하여 봐주시길 바랍니다. 🤔
```