---
layout: post
title: "[Vue.js] webpack 모듈 번들러 프로젝트 시 index 라우터 문제"
date: 2019-01-23
---  
<br/>

Vue.js 웹 페이지를 만들기 위해 webpack 모듈 번들러 프로젝트를 설치했다.(Node.js는 사전에 미리 설치)
<br/>

그러면 로컬에 다음과 같이 웹 개발에 필요한 폴더가 설치된다.
<br/>

![190123_1](https://user-images.githubusercontent.com/29648470/51576031-f3599300-1ef7-11e9-8592-7d1796515c2b.PNG)
<br/>

src > router > index.js 파일을 선택하면 다음과 같은 화면이 뜬다. 참고로 index.js 파일은 웹 페이지에서 url경로를 설정해주는 역할을 하는 파일이다. 
<br/>

![190123_2](https://user-images.githubusercontent.com/29648470/51576200-b04bef80-1ef8-11e9-961b-bdb32108752e.PNG)
<br/>

src > components 폴더에 pages 폴더를 하나 더 생성하고 MyComponent.vue라는 파일을 하나 만들었다. 그리고 이제 index.js파일에서 이 경로를 추가하기 
위해 다음과 같이 설정했다.
<br/>

![190123_3](https://user-images.githubusercontent.com/29648470/51576311-10429600-1ef9-11e9-9524-9714c412ecac.PNG)
<br/>

그러나 실제 CLI에서 npm run dev 명령어로 웹페이지를 실행해보면 기존의 HelloWorld 페이지만 나타난다. localhost:8080/mycomponent 주소를 입력해도
MyComponent 페이지가 나오지 않는다. 어떻게 된 걸까? **원인은 index.js파일의 mode 설정을 하지 않은 것에 있다**
<br/>

![190123_4](https://user-images.githubusercontent.com/29648470/51576438-91019200-1ef9-11e9-8ba0-43642d991af3.PNG)
<br/>

위와같이 
```
mode: 'history'
```
라고 설정해 주지 않으면 하나의 페이지만 보여진다. 그래서 HelloWorld.vue 페이지만 보여졌던 것이다. 
이제 다시 웹페이지를 실행해보면 localhost:8080/mycomponent 에서 MyComponent.vue페이지가 나오는 걸 확인할 수 있다. 
<br/>
