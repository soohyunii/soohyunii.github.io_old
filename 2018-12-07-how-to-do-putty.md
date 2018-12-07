---
layout: post
title: "누구나 알 것 같은 putty 사용법"
date: 2018-12-07
---  
<br/>

*시작하기전에 - putty란?  
물리적으로 떨어져 있는 서버에 내 PC로 접속하기 위한 가상 단말기 프로그램  
더 자세한 설명은 [https://dololak.tistory.com/24](https://dololak.tistory.com/24)참고*
<br/>

어느날 회사에서 구글 드라이버로 **ppk파일**과 **아마존 ubuntu 서버 IP**를 공유받았다.  
그래서, 이게 뭐에 쓰이는거라고?  
<br/>
![git1](https://user-images.githubusercontent.com/29648470/49653503-7de55080-fa78-11e8-87d8-40aaa36f6768.png)  
![git2](https://user-images.githubusercontent.com/29648470/49653535-97869800-fa78-11e8-9dff-c8ff966e3a2a.png)  
<br/>

<h2>1.구글 드라이브에 있는 ppk파일을 다운받는다</h2>
  어떤 경우에는 ppk파일을 다운받아 특정 폴더에 두면 PuTTY가 인식을 못하는 경우가 있다.<p>
  그러니 초보라면 안전하게 바탕화면에 파일을 두는 게 상책이다.  
<br/>

<h2>2.PuTTY 프로그램에 접속한다</h2>
  PuTTY에 접속하면 아래와 같은 화면이 나타나는데, <b>Host Name</b>에 공유받은 ubuntu 서버 IP주소를 입력했다.<p>
  Port번호는 그대로 22번을 쓰면 된다고 안내받아 별 다른 고민없이 Port는 22번으로 설정했다. 하지만 다른 상황에서는 혹시 모르니 확인이 필요할 것  
  <br/>  

![git4](https://user-images.githubusercontent.com/29648470/49654000-f7ca0980-fa79-11e8-9c35-d076815d08ac.png)

<h2>3.Connection > SSH > Auth</h2>
  왼쪽 카테고리에서 Connection > SSH > Auth를 차례대로 클릭하면 이런 화면이 나올 것이다.<p>
  무슨 말인지 모를 영어가 많이 써져 있지만 침착하게 'Browse..'버튼을 누르면 된다.
  <br/>
  
  ![git5](https://user-images.githubusercontent.com/29648470/49654176-7b83f600-fa7a-11e8-82a1-9d5a7e5d371a.png)  
  
  <i>여기서 잠깐 - SSH란?  
  Secure Shell의 약자이고 원격 로그인 프로그램이다. 더 자세한 설명은 [생활코딩 SSH 강의](https://opentutorials.org/module/432/3738)를 참고 </i>
<br/>

<h2>4.ppk파일 선택 후 열기</h2>
  'Browse..'버튼을 누르고 아까 전 바탕화면에 다운받아 둔 ppk파일을 선택한 후 '열기'를 누르면 끝난다.<p>   
  
  ![git6](https://user-images.githubusercontent.com/29648470/49654718-f3065500-fa7b-11e8-94ca-d6da9130f171.png)  
  ![git7](https://user-images.githubusercontent.com/29648470/49654746-04e7f800-fa7c-11e8-86ba-cebe8f61daa4.png) 
  
  <br/>
  이제 마지막으로 오른쪽 하단의 'Open'버튼을 누르면 외부 서버와 접속이 된 걸 확인할 수 있다. 만세! <p>
  
  ![git8](https://user-images.githubusercontent.com/29648470/49654754-0ca79c80-fa7c-11e8-8f6d-e02f1afaa7f1.png)  
  



  

  

  

  
  






