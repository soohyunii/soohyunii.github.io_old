---
layout: post
title: "[생활코딩] 리눅스 복습 및 정리_04"
date: 2018-10-25
categories: Linux
---  
<br/>  

* **프로세스**  
  * 컴퓨터의 구조 : 스토리지(Storage), 메모리(Memory), 프로세서(Processor)  
  * 스토리지(예:SSD,HDD)와 메모리(예:RAM)는 저장장치 역할을 한다  
  * 스토리지 : 가격↓, 용량↑, 속도↓ (메모리는 스토리지와 가격/용량/속도 반대)  
  * 프로그램을 실행시키면 : 스토리지에 저장되어 있는 프로그램이 메모리에 적재되고 CPU가 메모리에 있는 프로그램을 실행시킨다  
  * 프로세스 모니터링 명령어 : ps, top, htop  

<br/>

* **파일을 찾는 법**  
  * locate [파일명] : mlocate라는 데이터베이스에서 파일을 찾기 때문에 원하는 파일을 빠르게 찾을 수 있다  
  * find [파일명] : 디렉토리에서 찾기 때문에 locate 명령어 보다는 빠르지 않지만, '현재상태'의 파일을 찾을 수 있으며 
  여러 옵션을 붙일 수 있다는 것이 장점  
  * whereis : '실행파일'을 찾아주는 명령어  
  ![whereis](https://user-images.githubusercontent.com/29648470/47469943-7ce8be80-d83e-11e8-8e1e-baf2a89ea190.PNG)  
  * $PATH : 환경변수  
  
<br/>  

* **백그라운드 실행**  
  * 멀티태스킹(multitasking)  
  * Ctrl + Z : 프로그램을 종료하지 않고 background로 빠짐  
  * jobs : 현재 background에 존재하는 프로그램을 보여주는 명령어  
  * fg : background 프로그램을 forward로 불러와서 실행하는 명령어  
  * &가 명령어 뒤에 붙으면 명령어가 실행될 때 백그라운드로 실행된다

<br/>

* **항상 실행(daemon, service)**  
  * 냉장고, 도어락처럼 항상 켜져 있어야 하는 프로그램을 daemon 이라고 한다  
  * daemon의 대표적인 예로는 '서버(server)'가 있다 ex) apache2  
  * daemon 프로그램은 대부분 /etc/init.d 디렉토리에 존재하고 start, stop 명령어로 프로그램을 on/off 해야 한다 ex) sudo service apache2 stop  
  * '자동실행'은 링크의 이름을 불러들여 실행한다  
  ![default](https://user-images.githubusercontent.com/29648470/47471499-7ad62e00-d845-11e8-983b-b18a8d4e1538.PNG)  
  
<br/>  

* **정기적으로 실행(cron)**  
  * 백업, 메일보내기, 시간조정 등 정기적으로 시스템이 실행되어야 할 때  
  * 명령어 : crontab -e  

<br/>  

* **쉘을 시작할 때 실행**  
  * 리눅스 기본 쉘 = bash   
  * 명령어에 별명 붙여주기 : 'alias' ex) alias groot='ls-al'  
  ![alias](https://user-images.githubusercontent.com/29648470/47472193-b9211c80-d848-11e8-88d1-9f669c50b7a7.PNG)  
  
<br/>  

  
  
  
  
  
  
  
  
  
  
  
  
  
  
  

  
