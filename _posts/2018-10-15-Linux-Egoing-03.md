---
title: "[생활코딩] 리눅스 복습 및 정리_03"
date: 2018-10-15
categories: Linux
---  
<br/>  

* **쉘과 커널**  
  * 커널(Kernel) : 하드웨어(메모리,ssd,cpu 등)를 직접적으로 제어하는 부분  
  * 쉘(Shell) : 사용자가 입력(명령)하는 대상
  * 하드웨어 → 커널 → 쉘 → 어플리케이션 
  * 현재 쉘 종류를 알기위한 명령어 : echo $0
  * 쉘의 종류 : 'bash' vs 'zsh' 간의 차이 
  * bash쉘에서 cd + Tab키를 누르면 숨김파일(.[파일명]/)까지 나타난다  
  * zsh쉘에서 cd + Tab키를 누르면 숨김파일은 나타나지 않는다
  * 사용자가 자신의 편의성에 맞게 쉘을 선택할 수 있다  
<br/>

* **쉘 스크립트(Shell Script)**  
  * 쉘에서 순차적으로 실행되어야 하는 명령어들을 저장하는 곳 
  * chmod +x backup : 'backup'이라는 파일을 실행하도록 권한을 줌
<br/>    

* **디렉토리의 구조**  
  * [참고 사이트 : 디렉토리 구조](http://dev-random.net/linux-directory-structure-explained/)  
  * /sbin : 시스템 관리자 
  * /etc : 설정 파일 (Configuration Files)
  * /var : 프로그램을 실행하면서 변할 수 있는 성질의 파일을 모아둔 곳 ex) log파일 
  * /home : 홈 디렉토리로 바로 갈 수 있는 명령어는 '~'이다  
  ![home](https://user-images.githubusercontent.com/29648470/46938011-a0bd3f00-d09d-11e8-80be-b4a216be8a82.PNG)  
<br/>  

  

