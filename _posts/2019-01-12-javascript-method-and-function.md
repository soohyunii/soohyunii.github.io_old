---
layout: post
title: "[javascript] Array 관련 여러 메서드 정리"
date: 2019-01-12
---  
<br/>
최근 얼떨결에 맡게 된 프로젝트로 인해 지금까지 몰랐던 자바스크립트 Array 객체 메서드를 많이 알게 되었습니다.
<br/>
잊지 않기 위해 복습 차원에서 블로그에 정리해보려 합니다.
<br/><br/>
<strong>Array.prototype.forEach()</strong>
<br/>
배열 전체를 돌며 해당 배열의 요소에 각각 어떤 작업을 수행할 수 있다. 
<br/>

```
var array1 = ['a', 'b', 'c'];

array1.forEach(function(element) {
  for(var i=0; i<=array1.length; i++){
    if(array1.indexOf(element)==i-1){  
      console.log(element+i);
    }
  }
});

// "a1"
// "b2"
// "c3"
```
<br/>
<strong>Array.prototype.pop()</strong>
<br/>
배열의 가장 마지막 원소를 제거한다. 
<br/>

```
var plants = ['broccoli', 'cauliflower', 'cabbage', 'kale', 'tomato'];

console.log(plants.pop());

console.log(plants);

// "tomato"
// Array ["broccoli", "cauliflower", "cabbage", "kale"]
```
<br/>
<strong>Array.prototype.push()</strong>
<br/>
배열의 마지막에 원소를 추가한다.

```
var animals = ['pigs', 'goats', 'sheep'];

animals.push('chickens');

console.log(animals);

// Array ["pigs", "goats", "sheep", "chickens"]
```
<br/>
<strong>Array.prototype.slice()</strong>
<br/>
배열의 일부분을 선택해서 새로운 배열을 만들 수 있다. slice(start,end)로 사용할 수 있으며 start에 해당하는 요소부터 
end 바로 전의 요소까지 선택된다. 
<br/>

```
var animals = ['ant', 'bison', 'camel', 'duck', 'elephant'];

console.log(animals.slice(2));

console.log(animals.slice(1, 5));

// Array ["camel", "duck", "elephant"]
// Array ["bison", "camel", "duck", "elephant"]
```
<br/>
<strong>Array.prototype.splice()</strong>
<br/>
배열에서 특정 범위의 값들을 추출하고 그 자리에 새로운 값을 넣을 수 있다. 
또는 특정 범위의 값을 제거하거나 대체도 가능하다.
splice(start,deleteCount,item)로 사용할 수 있다. start에 해당하는 위치에서 deleteCount에 해당하는 값만큼 
삭제할 수 있으며 item의 요소로 대체/추가 할 수 있다. 
<br/>

```
var months = ['Jan', 'March', 'April', 'June'];

// 'Jan', 'March' 사이에 'Feb' 요소 넣기
months.splice(1, 0, 'Feb');

console.log(months);

// Array ['Jan', 'Feb', 'March', 'April', 'June']에서 마지막 요소를 삭제하고 'May'로 대체
months.splice(4, 1, 'May');

console.log(months);

// Array ["Jan", "Feb", "March", "April", "June"]
// Array ["Jan", "Feb", "March", "April", "May"]
```
<br/><br/><hr/>
<strong>출처</strong>
<br/>
[https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array)
<br/>
<br/>























