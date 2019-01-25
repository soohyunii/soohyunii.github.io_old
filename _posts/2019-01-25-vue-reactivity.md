---
layout: post
title: "[Vue.js] 반응형 - 변경 감지 경고"
date: 2019-01-25
---  
<br/>

Vue.js를 사용해서 개발하던 중 문제가 발생했다. 
<br/>

![190125_03](https://user-images.githubusercontent.com/29648470/51726554-5b9ca600-20ab-11e9-93b0-76d1ee0c69f3.PNG)
<br/>

한번 등록한 정보를 수정할 때 select option을 바꿔도 화면에서 바뀌지 않는 문제였다.
<br/>

![190125_04](https://user-images.githubusercontent.com/29648470/51726563-65260e00-20ab-11e9-8286-98c32547409d.png)
<br/>
*('강사4'를 선택해도 화면은 여전히 '강사3'을 보여준다)*
<br/><br/><br/>

찾아보니 아래 코드에 문제가 있다는 것을 알게되었고..
<br/>

![190125_06](https://user-images.githubusercontent.com/29648470/51726426-b1bd1980-20aa-11e9-8eeb-6a32119f44f6.PNG)
<br/>

반응형에 대해 검색해보니 **'Vue는 이미 만들어진 인스턴스에 새로운 루트 수준의 반응 속성을 동적으로 추가하는 것을 허용하지 않는다.
그러나 Vue.set(object, key, value) 메소드를 사용해 중첩된 객체에 반응성 속성을 추가 할 수 있다.'**라고 한다.
<br/>

위의 내용을 참고해서 아래와 같이 코드를 바꿔 보니 정상적으로 돌아왔다! Vue.js로 개발을 하는 중이지만 Vue의 세계는 여전히 넓고 심오하구나 
느낄 수 있었다ㅎㅎ
<br/>

![190125_02](https://user-images.githubusercontent.com/29648470/51726530-39a32380-20ab-11e9-8100-2226291f9cff.PNG)
<br/><br/><hr/>

<strong>출처</strong><br/>

* Vue.js 공식 홈페이지 - 반응형에 대해 깊이 알아보기 : [https://kr.vuejs.org/v2/guide/reactivity.html](https://kr.vuejs.org/v2/guide/reactivity.html)






