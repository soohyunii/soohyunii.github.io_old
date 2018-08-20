---
title: "MongoDB에서 데이터 추출해 wordcloud만들기(1)"
date: 2018-08-20
categories: articles
---

MongoDB에 쌓인 데이터를 csv파일 형식으로 추출해 wordcloud를 만드는 포스팅을 1,2탄으로 나눠 올릴 예정이다.  
이번 포스터에는 MongoDB에서 csv파일을 추출하는 방법까지만 설명하려한다  

참고로 이 포스팅의 전제조건은..  
* MongoDB에 데이터가(이왕이면 텍스트데이터) 쌓여있어야 한다    
* wordcloud를 만드는 데 사용한 언어는 파이썬이며, IDE는 스파이더(Spyder)를 사용했다    

---
  
  
**1. MongoDB에서 csv파일을 추출한다.**   
MongoDB 실행파일이 있는 bin 폴더로 이동해서 다음과 같은 명령어를 입력한다.  
```
mongoexport --db [db이름] --collection [컬렉션이름] --type csv --out [csv파일을 생성할 폴더경로] --fields [csv에 넣을 필드]
```
![py01](https://user-images.githubusercontent.com/29648470/44334509-ae46b600-a4ac-11e8-8daf-0750c10bac2e.png)  
cmd창에서 위와 같은 명령어를 입력하면 MongoDB의 cosy_db에서 collection 'posts'의 id, text값을   
C:\Users\happy\Desktop\textPy\text.csv 파일 형식으로 저장한다. 즉, csv파일이 추출된다. 


**2. csv파일을 열어 데이터를 확인**  
![1212](https://user-images.githubusercontent.com/29648470/44334801-7d1ab580-a4ad-11e8-92e2-48ba03e0971c.png)  
1번에서 path를 설정한대로 csv파일이 생성되어 있는 것을 확인할 수 있다.  
하지만 여기서 엑셀파일로 열게 되면 한글이 깨져서 보인다 *(이유는 저도 잘..아시는 분은 답글로 부탁드립니다!)*  
  
  
엑셀 파일 대신 **메모장** 으로 열어야 데이터가 제대로 보인다.  
![image](https://user-images.githubusercontent.com/29648470/44335014-13e77200-a4ae-11e8-8e0d-d1e997b28c19.png)  









