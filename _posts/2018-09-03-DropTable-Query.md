---
title: "Oracle SQL : 테이블 모두 삭제하기"
date: 2018-09-03
categories: articles
---

SQL을 사용하다보면 생성된 테이블을 한꺼번에 삭제하고 싶을 때가 있다.  
그럴때 모든 테이블에 일일이 **'Drop table [테이블명]';** 을 쳐서 삭제하기엔 번거로운 일이 아닐 수 없다.  
이럴 때 다음과 같은 쿼리를 쓰면 훨씬 편하게 테이블을 삭제 할 수 있다.  

```  
SELECT 'DROP TABLE ' || TABLE_NAME || ';'  
FROM USER_ALL_TABLES  
```

만약 **특정 이름**을 가진 테이블만 삭제하고 싶다면  
```  
SELECT 'DROP TABLE ' || TABLE_NAME || ';'  
FROM USER_ALL_TABLES  
WHERE TABLE_NAME LIKE '%[특정테이블명]%';  
```  


