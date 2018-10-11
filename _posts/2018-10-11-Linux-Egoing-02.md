---
title: "[생활코딩] 리눅스 복습 및 정리_02"
date: 2018-10-11
categories: Linux
---

* **sudo**
  * sudo(super user do, 슈퍼 유저가 하는 일)  
  * 여러 사람이 한 컴퓨터를 나눠 쓸 때 생기는 문제들을 방지하기 위해 권한(permission) 부여
  * super user 또는 root user
  * 프로그램 설치 시 super user 사용 ex) 우분투에서 apt-get install git 

<br/>

* **파일편집(nano)**
  * 편집기 : nano , vi 
  * nano 편집기는 파일 확장자의 문법에 따라 '컬러링'을 해 줌  
  ![nano color](https://user-images.githubusercontent.com/29648470/46775281-89025580-cd41-11e8-9a49-c6bef85efe8f.PNG)  

<br/>

* **패키지 매니저**
  * 운영체제에 기본적으로 설치되어 있지 않은 프로그램을 쉽게 설치할 수 있는 방법 ex) 앱스토어
  * 리눅스에서 대표적인 패키지 매니저는 apt, yum이 있다
  * sudo apt-get update : 최신상태의 소프트웨어 목록 다운로드
  * sudo apt-cache search [프로그램명] : 특정 프로그램 검색
  * sudo apt-get install [프로그램명] : 특정 프로그램 설치 
  * sudo apt-get upgrade [프로그램명] : 특정 프로그램 업그레이드 (sudo apt-get upgrade : 모든 프로그램 업그레이드)
  * sudo apt-get remove [프로그램명] : 특정 프로그램 삭제 

<br/>

* **왜 CLI(Command Line Interface)인가?**
  * GUI vs CLI
  * 컴퓨터에 드는 에너지 : GUI >> CLI
  * 서버 컴퓨터, 데이터 분석에 어울리는 인터페이스 : GUI << CLI
  * 순차적인 작업에 효율적인 인터페이스 : GUI(한번에 하나씩 실행) << CLI(한번에 여러작업 실행)
  * CLI 순차적으로 실행 : ';'으로 명령어를 이어서 입력 가능 ex) $ mkdir why;cd why  
  * 파이프라인('|') : 여러 명령을 혼합해서 사용할 때 한 명령의 결과가 다른 명령으로 전송되는 통로 
  * 파이프라인 예시 ex) ls --help | grep sort : ls 명령어의 사용설명서 중 'sort'라는 텍스트만 포함된 문장을 출력   
  ![grep sort](https://user-images.githubusercontent.com/29648470/46775468-61f85380-cd42-11e8-9727-c809892c21c1.PNG)

<br/>

* **IO Redirection**
  * 직역하면 '입출력의 방향바꾸기'
  * Standard Output=표준출력=1 / Standard Error=표준에러=2
  * '>' 부호를 사용 : Standard Output ex) ls -l > redirection.txt 
  * [강의에 나오는 슬라이드 쇼는 이 링크에서 확인할 수 있음 (7페이지)](http://slideplayer.com/slide/5126304)
  * rm remove2.txt 1> result.txt 2> error.txt : 명령어가 성공하면 result.txt에 기록, 실패하면 에러사항(No such file or directory)을 error.txt에 기록
  * 하나의 프로그램은 여러개의 프로세스(Process)를 가질 수 있다

<br/>  
  
  
  
  
  
  
  
  
  
  
  
  
  
