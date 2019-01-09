---
layout: post
title: "[javascript] 함수형 프로그래밍 : map() "
date: 2019-01-09
---  
<br/>
오늘은 자바스크립트의 함수 중 하나인 'map()'함수에 대해 설명하겠습니다.<br/>
설명하기에 앞서, map()함수를 가리키는 '자바스크립트에서의 함수형 프로그래밍' 이 무엇인지 잠깐 얘기해보겠습니다. js뉴비인 저는 잘 몰랐기 때문에..<br/>
함수형 프로그래밍은 말 그대로 함수의 조합으로 작업을 수행하는 것입니다. 
중요한 것은 이 작업이 이루어지는 동안 작업에 필요한 <strong>데이터와 상태는 변하지 않는다는</strong> 점입니다.<br/>
<br/>
map()함수는 함수형 프로그래밍 중에서도 <strong>반복 함수</strong>에 속합니다. 반복함수에는 <strong>each() 함수, map() 함수, reduce() 함수</strong>
등이 있습니다. <br/>
map()함수는 주로 배열에 많이 사용되는 함수입니다. 배열의 각 요소를 꺼내서 사용자 정의 함수를 적용시켜 새로운 값을 얻은 후, 새로운 배열에 넣을 수
있습니다. 이해를 위해 코드로 예시를 보여드리겠습니다.<br/>
<br/>

```
Array.prototype.map=function(callback){
	var obj=this;
	var value,mapped_value;
	var A = new Array(obj.length);

	for(var i=0;i<obj.length;i++){
		value=obj[i];
		mapped_value=callback.call(null,value);
		A[i]=mapped_value;
	}
	return A;
};

var arr=[1,2,3];
var new_arr=arr.map(function(value){
	return value*value;
});

console.log(new_arr);  //(출력값) [1,4,9]
```
<br/>
<br/>
<hr/>
<strong>출처</strong>
<br/>
[책 '인사이드 자바스크립트' (송영주,고현주 저 / 한빛미디어)](http://www.hanbit.co.kr/store/books/look.php?p_code=B6479856408) 
<br/>
<br/>








