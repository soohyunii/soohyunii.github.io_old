---
title: "[생활코딩] 리눅스 복습 및 정리_01"
date: 2018-10-07
categories: Linux
---

리눅스를 예전부터 사용하고 있었지만 주먹구구 식으로 배워 이론적인 지식이 부족하다. 
그래서 앞으로 [생활코딩 리눅스](https://opentutorials.org/course/2598) 강의를 듣고 복습 차원에서 종종 강의 정리 내용을 올릴 예정이다. 

---  

* **리눅스에서 중요한 두가지는 터미널과 디렉토리다**  
  * 콘솔(Console)은 터미널의 일종이다. 
  * 콘솔은 CLI(Command Line Interface) 환경이며, CLI란 텍스트를 통해 사용자와 컴푸터가 상호작용하는 방식이다.  
  * 디렉토리(Directory)는 파일들이 정리되어 있는 파일 시스템 공간 정도로 생각하면 된다.  
 
 <br/>
 
* **상대경로와 절대경로**   
  * 상대경로는 현재 디렉토리의 위치를 기준으로하고, 절대경로는 최상위 디렉토리를 기준으로 경로를 표현  
  ![default](https://user-images.githubusercontent.com/29648470/46578308-f78c9e00-ca37-11e8-99b2-c90662dce4c1.PNG)  
  (사진 1 : 상대경로 예시)   
  ![default](https://user-images.githubusercontent.com/29648470/46578312-0ecb8b80-ca38-11e8-8a03-bafcb54e30f7.PNG)  
  (사진 2 : 절대경로 예시)  
   
 <br/>  

* **명령어**   
  * rm [파일명] : 파일이나 디렉토리를 삭제 (디렉토리 삭제 시 rm -r [디렉토리명])  
  ![rm](https://user-images.githubusercontent.com/29648470/46578445-57387880-ca3b-11e8-8d62-9dacf66bb6b0.PNG)  
  (사진 3 : groot 파일 삭제)  
  ![rm](https://user-images.githubusercontent.com/29648470/46578449-6fa89300-ca3b-11e8-8551-e27061bf71ee.PNG)  
  (사진 4 : IamGroot 폴더 삭제) 
  * --help , man 명령어 : man 명렁어가 좀 더 상세한 내용 제공  
  
  
<br/>    
    
* **etc**  
  * 리눅스에서 숨겨진 파일은 파일명 앞에 '.'이 붙는다. ex) .IamGroot
  


  


