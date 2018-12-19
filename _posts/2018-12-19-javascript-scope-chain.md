---
layout: post
title: "자바스크립트 스코프체인(scope chain)"
date: 2018-12-19
---  
<br/>

요즘 ['인사이드 자바스크립트'](http://www.hanbit.co.kr/store/books/look.php?p_code=B6479856408)라는 책으로 javascript에 대해 공부하고 있다. 
내용 복습 겸 스코프 체인(scope chain)에 대해 공부한 내용을 적어둔다. 
<br/>

스코프체인을 알기 전에, 먼저 스코프(scope)란 무엇인지 알아보도록 한다. 
사전에서 scope를 검색하면 크게 **기회, 범위**라는 뜻이 주로 나온다.
<br/>
![1](https://user-images.githubusercontent.com/29648470/50193978-40d46480-037c-11e9-90ff-9af728492ab6.PNG)

<br/>

자바스크립트에서의 스코프란 **유효범위** 를 뜻하고, 이 유효 범위 안에서 변수와 함수가 존재한다. 이 유효범위를 넘어서는 곳에 ({ }범위 안에서 선언된) 변수를 
사용하면 접근이 불가능해 컴파일 에러가 발생한다. C언어와 같은 언어에서는 함수의 중괄호({ })뿐만 아니라 if, for문의 중괄호도 한 블록으로 묶여서, 그 안에
선언된 변수는 밖에서 접근이 불가능하다. 하지만 자바스크립트는 for, if문과 같은 구문은 유효범위가 없다. **오직 함수만이 유효 범위의 한 단위가 된다.**

<br/>

이 유효범위를 나타내는 스코프(scope)가 **[[scope]]** 프로퍼티로 각 함수 객체 내에서 연결 리스트 형식으로 관리되는데, 이를 **스코프체인** 이라고 한다. 
<br/>
![2](https://user-images.githubusercontent.com/29648470/50195061-ea1d5980-0380-11e9-8b60-821e7a3fda28.png)

<br/>

**각각의 함수는 [[scope]] 프로퍼티로 자신이 생성된 실행 컨텍스트의 스코프 체인(scope chain)을 참조한다.**
결국, 요약하면 **스코프 체인 = 현재 실행 컨텍스트의 변수 객체 + 상위 컨텍스트의 스코프 체인** 이라고 할 수 있다.

<br/>
이해를 돕기 위해 예제를 들어보도록 하자. 
<br/>

![3](https://user-images.githubusercontent.com/29648470/50195401-3d43dc00-0382-11e9-80c8-5a700bf9fbd5.PNG)
<br/>

위의 코드를 실행하면 다음과 같이 나온다. 
<br/>

![4](https://user-images.githubusercontent.com/29648470/50195443-65333f80-0382-11e9-88ec-c7844c085942.PNG)
<br/>

![5](https://user-images.githubusercontent.com/29648470/50195520-c8bd6d00-0382-11e9-9284-555dd9d5316d.PNG)
<br/>

위의 그림처럼 value변수를 **2: printValue변수 객체**에서 먼저 탐색하고, 없으면 **1: printFunc변수 객체**에서 찾으므로 결과값은 printFunc()함수에서 
정의한 var value="value2"가 된다.
<br/><br/>
<hr/>

**출처** 
<br/>
도서 : 인사이드 자바스크립트 (송형주, 고현준 지음 / 한빛미디어)
<br/>
스코프 체인 설명 이미지 : [http://juheejin.tistory.com/entry/%EC%9E%90%EB%B0%94%EC%8A%A4%ED%81%AC%EB%A6%BD%ED%8A%B8-%EC%8A%A4%ED%84%B0%EB%94%945-%EC%8B%A4%ED%96%89%EC%BB%A8%ED%85%8D%EC%8A%A4%ED%8A%B8%EC%99%80-%ED%81%B4%EB%A1%9C%EC%A0%80](http://juheejin.tistory.com/entry/%EC%9E%90%EB%B0%94%EC%8A%A4%ED%81%AC%EB%A6%BD%ED%8A%B8-%EC%8A%A4%ED%84%B0%EB%94%945-%EC%8B%A4%ED%96%89%EC%BB%A8%ED%85%8D%EC%8A%A4%ED%8A%B8%EC%99%80-%ED%81%B4%EB%A1%9C%EC%A0%80)
<br/>
네이버 사전 : [https://endic.naver.com/search.nhn?sLn=kr&dicQuery=scope&x=0&y=0&query=scope&target=endic&ie=utf8&query_utf=&isOnlyViewEE=N](https://endic.naver.com/search.nhn?sLn=kr&dicQuery=scope&x=0&y=0&query=scope&target=endic&ie=utf8&query_utf=&isOnlyViewEE=N)
<br/>






