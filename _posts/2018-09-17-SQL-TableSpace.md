---
title: "Oracle SQL에서 tablespace 확인하기"
date: 2018-09-17
categories: articles
---

ORACLE을 사용하다보면 다음과 같은 에러가 생기는 경우가 있다.  
```
ORA-01652: 1024(으)로 테이블 공간 USERS에서 임시 세그먼트를 확장할 수 없습니다
```  
한마디로 테이블 공간이 꽉 찼다는 뜻이니까, DB에 얼마나 여유공간이 남아있는지 확인을 해야 한다.  
이럴 때 사용하는 **테이블 스페이스 확인 쿼리** 는 다음과 같다.  

```
1. sysdba 계정으로 접속 
sqlplus sys/tiger as sysdba

2. 테이블 스페이스 확인 쿼리 
SQL> select distinct d.file_id  file#,
  2  d.tablespace_name  ts_name,
  3  d.bytes/1024/1024  mb,
  4  d.bytes/8192       total_blocks,
  5  sum(e.blocks)      used_blocks,
  6  to_char(nvl(round(sum(e.blocks)/(d.bytes/8192),4),0)*100,'09.99')||'%'pct_used
  7  from dba_extents e, dba_data_files d
  8  where d.file_id=e.file_id(+)
  9  group by d.file_id, d.tablespace_name, d.bytes
 10  order by 1,2;
```  

![6767](https://user-images.githubusercontent.com/29648470/45612743-edadf580-ba9e-11e8-9457-611581be6156.png)  

결과를 보면 USERS의 테이블 스페이스가 97.05%로 거의 차있다는 것을 알 수 있다.  
필요없는 테이블을 삭제해 테이블 스페이스 공간을 확보해야한다. 
