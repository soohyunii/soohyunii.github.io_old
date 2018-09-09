---
title: "Node.js : Mysql Update 쿼리문 사용하기"
date: 2018-09-09
categories: articles
---

Node.js로 CRUD기능을 만들던 중 update에서 헷갈렸던 부분이다.   
Insert와 마찬가지로 update도 모든 파라미터(프런트에 보낼 정보들)를 하나의 변수에 묶어  
conn.query에서 sql문장을 수행할 수 있을 줄 알았던 것.  
이해를 돕기 위해 실제 내가 코딩한 Insert문을 예로 들어보면,  

![my01](https://user-images.githubusercontent.com/29648470/45261008-8c987900-b431-11e8-9363-03b5d95a87d4.png)  

모든 파라미터는 **data** 라는 변수에 담겨 한꺼번에 실행되는 것을 볼 수 있다.  

**그러나 UPDATE는 INSERT처럼 파라미터를 data 변수 안에 묶어서 conn.query()문을 실행 할 수 없다**  

만일 UPDATE문을 INSERT처럼 var data={ } 에 파라미터를 담는 방식으로 코딩하면 다음과 같은 에러가 날 것이다.  

![my02](https://user-images.githubusercontent.com/29648470/45261057-054c0500-b433-11e8-9f1a-57ce29a9fa3d.png)  

당연히 INSERT와 같은 방식이겠거니 생각했던 나에게는 당황스러운 에러였다.  

무작정 이 에러에 대해 서치하다가 어쩌면 당연한(!) 이유를 발견했는데,  

UPDATE문은 data 변수를 사용해 한꺼번에 넘기는대신 일일이 conn.query()로 넘겨줘야 한다는 것이 내가 간과했던 부분이었다.  

![my03](https://user-images.githubusercontent.com/29648470/45261079-dbdfa900-b433-11e8-8a0b-02a9db48e42d.png)  
(출처 : <https://github.com/mysqljs/mysql/issues/1831> )  

그래서! 아래와 같이 모든 파라미터를 conn.query()문에 직접 넘겨주는 방식으로 짜보니 정상적으로 실행되는 걸 확인할 수 있었다.  
앞으론 '당연하게' 생각한 부분도 한번쯤 짚고 넘어가보자. 지금처럼 조금은 부끄러운 실수일 수도 있으니  


![my04](https://user-images.githubusercontent.com/29648470/45261168-67f2d000-b436-11e8-95e0-de7a51c6ae6c.png)  

![my05](https://user-images.githubusercontent.com/29648470/45261170-7e009080-b436-11e8-9ced-7ae3c9e34431.png)  












