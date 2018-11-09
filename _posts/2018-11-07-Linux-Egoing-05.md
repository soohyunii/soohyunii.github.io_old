---
layout: post
title: "[생활코딩] 리눅스 복습 및 정리_05"
date: 2018-11-07
---  
<br/>

* **다중 사용자**  
  * 유닉스 계열은 '권한'을 달리하는 다중사용자 시스템이다.    
  * id : 나는 누구인가? , who : 현재 누가 접속해 있는가?  
<br/>

* **관리자와 일반 사용자**  
  * super(root) user : 관리자 , user : 일반유저  
  * super user가 되기 위한 명령어 → 일반적인 리눅스 운영체제 : su - root, 우분투 : sudo passwd -u root 후에 su - root  
<br/>

* **사용자의 추가**  
  * sudo useradd -m [추가할 사용자이름]  
  * 추가한 사용자 패스워드 설정 : sudo passwd [추가할 사용자이름]  
  * 추가한 사용자가 sudo 명령어를 쓸 수 있게 설정 : sudo usermod -a -G sudo [추가할 사용자이름]  
<br/>

* **권한(permission)**  
  * rwx : '읽기','쓰기','실행' 권한  
  * 권한을 변경하는 방법(chmod)  
  ![1](https://user-images.githubusercontent.com/29648470/48106528-11134680-e27f-11e8-87df-e9bd85c8b807.PNG)  
  → other(작성자 외의 다른 사용자)의 r(읽기)권한을 없애고 싶을 때 명령어 : chmod o-r [파일명 또는 디렉토리명]  
  → other(작성자 외의 다른 사용자)의 w(쓰기)권한을 추가하고 싶을 때 명령어 : chmod o+w [파일명 또는 디렉토리명]  
  * 실행(execute)의 개념과 권한 설정  
  ![2](https://user-images.githubusercontent.com/29648470/48106812-69971380-e280-11e8-9bd7-8632926f2700.PNG)  
  * chmod 사용법 정리 - 간편하게 사용하기  
  ![3](https://user-images.githubusercontent.com/29648470/48107160-cf37cf80-e281-11e8-862a-75b17c395f22.PNG)  
  ![4](https://user-images.githubusercontent.com/29648470/48107167-d959ce00-e281-11e8-9582-5a29d581aa61.PNG)  
  ex) chmod 111 perm.txt , chmod a=r abc.txt  
  * -R : 재귀적 명령어 
<br/>

* **인터넷, 네트워크 그리고 서버**    
  * domain name : google.com과 같은, 일반적인 사람들이 알고 있는 웹브라우저 주소  
  * ip address : 172.21.25.78과 같은, 실질적인 웹 브라우저 주소    
  * DNS Server : 모든 웹 브라우저의 domain name과 ip address를 알고 있는 거대한 전화번호부  
  * public address : 대표번호. 명령어는 curl ipinfo.io/ip    
  * private address : 공유기(Router)를 통해 나온 사설ip. 같은 공유기로 묶인 기기는 사설 ip로 통신할 수 있다. 명령어는 ip addr  
<br/>  


  
  
  
  

