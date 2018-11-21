---
layout: post
title: "[생활코딩] 리눅스 복습 및 정리_06"
date: 2018-11-19
---  
<br/>

* **웹서버 (아파치)**  
  * Web Broswer : IE, Chrome etc..  
  * Web Server : Apache, nginx  etc..  
  * 웹서버 설치 → 쉘에서 웹 브라우저로 접속 → elinks  
  * 한 대의 컴퓨터에 웹 브라우저와 웹 서버가 모두 설치되어 있다면, ip addr 명령어 대신 localhost를 사용해 웹서버에 접속할 수 있다  
  * configuration(.conf, 환경설정) → /etc/apache2 : 웹서버는 어디에서 웹 브라우저가 원하는 파일을 불러오는가?  
  * log파일 : 접속현황, 동작을 기록   
<br/>

* **원격제어 (ssh)**  
  * SSH란? (참고자료 : [http://baked-corn.tistory.com/52](http://baked-corn.tistory.com/52))  
<br/>

* **포트 (port)**  
  * 포트 포워딩 : 공유기를 사용하는 특정 기기에 접속하기 위한 포트를 알고, 이에 따라 접속하면 공유기는 할당된 포트 번호대로 내부 IP에 연결해주는 행위 (참고자료 : [http://awesometic.tistory.com/55](http://awesometic.tistory.com/55))  
  * default gateway    
  * default gateway를 알아내기 위한 명령어 : ip route  
  * 내부 IP를 알아내기 위한 명령어 : ip addr  
  * 현재 사용하고 있는 공유기의 IP (public ip)를 알아내는 방법 : [https://ipinfo.io/ip](https://ipinfo.io/ip) 에 접속  
<br/>

* **도메인 (domain)**    
  * host파일 : 운영체제가 호스트 이름을 IP주소에 매핑할 때 사용하는 컴퓨터 파일  
  * DNS 서버 : 사용자가 입력한 도메인 이름을 IP주소로 변환해주는 시스템이자 라우팅 정보를 제공하는 분산형 데이터베이스 시스템 (DNS 서버 >> host 파일) 
  * 서브 도메인 : 본진 도메인에서 파생된 여러 부속 도메인. 서브 도메인이 있어 모든 서버마다 1:1로 도메인을 구입하지 않아도 된다  
  * DNS의 동작 원리 : 분산 & 계층적 & 트리구조 (자세한 내용은 [http://www.ktword.co.kr/abbr_view.php?m_temp1=264](http://www.ktword.co.kr/abbr_view.php?m_temp1=264) 참고)  
<br/>

* **인터넷을 통한 서버간 동기화 (rsync)**  
  * 예) 두 폴더의 내용을 동기화 시키는 경우  
  * rsync -av [동기화 할 폴더경로]  
<br/>

* **로그인 없이 로그인하기 (ssh key)**  
  * 비공개키(private key) VS 공개키(public key) : 비공개키는 타인(외부)에게 절대 노출하면 안되는 키다. 반면에 공개키는 외부에 공개가능(ssh-copy-id). 공개키를 사용해 로그인 없이 계정에 접속할 수 있다
  * RSA : 공개키 암호시스템의 하나. 개인키(private key)와 공개키(public key) 두 개의 키를 사용하는데, 일반적으로 공개키는 모두에게 알려져 있으며 메시지를 암호화(encrypt)하는데 쓰이고 개인키는 복호화(decrypt)에 주로 쓰인다. 하지만 RSA 공개키 알고리즘은 이러한 제약조건이 없다. 즉, 개인키로 암호화하여 공개키로 복호화 할 수도 있다. 이러한 방식을 '비대칭 암호화 기법'이라고 한다.  
<br/>  
  
