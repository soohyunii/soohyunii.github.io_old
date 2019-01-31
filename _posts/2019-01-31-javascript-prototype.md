---
layout: post
comments: true
title: "[javascript] 프로토타입 이해하기"
date: 2019-01-31
--- 
<br/>

* 자바스크립트의 모든 객체는 자신의 부모 역할을 하는 객체와 연결되어 있다. 그리고 이것은 마치 객체지향의 상속 개념과 같이 부모 객체의 프로퍼티를
마치 자신의 것처럼 쓸 수 있는 것 같은 특징이 있다. 자바스크립트에서는 이러한 부모 객체를 **프로토타입** 이라고 부른다
<br/>

* 프로토타입(Prototype)은 크게 Prototype Object와 Prototype Link로 이루어져 있다
<br/>

* **Prototype Object** : 'prototype 속성'이라고도 하며 자바스크립트에서 함수가 정의될 때 같이 생성된다 
<br/>

* **Prototype Chain** : ```_proto_```를 통해 상위 프로토타입과 연결되어 있는 성질이다
<br/><br/>
<hr/>

<strong>출처</strong><br/>
* 인사이드 자바스크립트: [http://www.hanbit.co.kr/store/books/look.php?p_code=B6479856408](http://www.hanbit.co.kr/store/books/look.php?p_code=B6479856408)
<br/><br/>

  

