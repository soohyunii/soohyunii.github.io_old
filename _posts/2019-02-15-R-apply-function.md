---
layout: post
comments: true
title: "[R] apply 계열 함수 정리"
date: 2019-02-15
--- 
<br/>

R에는 벡터, 행렬 또는 데이터 프레임에 임의의 함수를 적용한 결과를 얻기 위한 apply 계열 함수가 있다. 
이 함수들은 데이터 전체에 함수를 한 번에 적용하는 벡터 연산을 수행하므로 속도가 빠르다. 
<br/>

**01.apply()**
<br/>
apply()는 행렬의 행 또는 열 방향으로 특정 함수를 적용하는데 사용한다.
```
apply(
  배열 또는 행렬,
  함수를 적용하는 방향 (행:1, 열:2),
  적용할 함수
  )
```  

![apply_01](https://user-images.githubusercontent.com/29648470/52836263-663bdf80-312d-11e9-87a6-f7708adf5534.PNG)
<br/>

위의 내용은 행렬 d의 행별 합계를 나타낸 것이다.
<br/><br/>

**02.lapply()**
<br/>

lapply()는 리스트를 반환하는 특징이 있는 apply 계열 함수이다. 벡터, 리스트, 표현식, 데이터 프레임 등에 함수를 적용하고 그 결과를 리스트로 반환한다.
아래는 lapply()를 적용한 예시이다. 참고로 unlist()함수는 리스트 구조를 보기 쉽게 벡터로 변환하는 함수이다.
<br/>

![lapply_01](https://user-images.githubusercontent.com/29648470/52836561-77d1b700-312e-11e9-9ab7-d04187fd4451.PNG)
<br/><br/>

**03.sapply()**
<br/>

sapply()는 lapply()와 유사하지만 리스트 대신 행렬, 벡터 등의 데이터 타입으로 결과를 반환하는 특징이 있다. 아래의 예시를 보면, lapply()는 리스트로
결과를 반환하지만, sapply()는 벡터로 결과를 반환하는 것을 볼 수 있다. 
<br/>

![sapply-03](https://user-images.githubusercontent.com/29648470/52837164-0ba48280-3131-11e9-86d6-d03cd94d5987.PNG)
<br/>

sapply()에서 반환한 벡터는 as.data.frame()을 사용해 데이터 프레임으로
변환할 수 있다. 이때 t(x)를 사용해 벡터의 행과 열을 바꿔주지 않으면 기대한 것과 다른 모양의 데이터 프레임을 얻게된다.
<br/>

![sapply-04](https://user-images.githubusercontent.com/29648470/52837314-938a8c80-3131-11e9-8321-65d5dd8737c3.PNG)
<br/>

만약 sapply()함수에서 함수의 출력의 길이가 1보다 큰 벡터들이라면 sapply()는 행렬을 반환한다. 다음 예에서는 아이리스 데이터의 숫자형 값들에 대해 각 값이 
3보다 큰지 여부를 판단한다. sapply()에 넘긴 함수의 반환 값이 길이가 1보다 큰 벡터이므로 수행 결과가 행렬로 나타난다. 
<br/>

![sapply-05](https://user-images.githubusercontent.com/29648470/52838892-8bcde680-3137-11e9-87ee-b1a5b6f83a61.PNG)
<br/><br/>

**04.tapply()**
<br/>

tapply()는 **그룹별로 함수를 적용**하기 위한 apply 계열 함수이다. 벡터 등에 저장된 데이터를 주어진 기준에 따라 그룹으로 묶고 각 그룹에 함수를 적용,
결과를 반환한다.

```
tapply(
  벡터,
  데이터를 그룹으로 묶을 색인,
  각 그룹마다 적용할 함수
  )
```

![tapply-01](https://user-images.githubusercontent.com/29648470/52839090-380fcd00-3138-11e9-9525-66f2dec46afe.PNG)
<br/>

위 코드에서 rep(1,10)은 1을 10회 반복하는 것을 뜻한다. 따라서 1:10까지 동일한 소속번호 1을 부여한 것이다.<p>
그렇다면 아이리스 데이터에서 Species(꽃의 종)별 Sepal.Length(꽃받침의 길이)를 구한다면 어떻게 해야 할까? 답은 아래와 같다. 
<br/>

![tapply-02](https://user-images.githubusercontent.com/29648470/52839233-ad7b9d80-3138-11e9-8a37-b481ac81dac7.PNG)
<br/><br/>

<hr/>

<strong>출처<strong/>
* R을 이용한 데이터 처리&분석 실무 : [https://www.gilbut.co.kr/book/view?bookcode=BN001023](https://www.gilbut.co.kr/book/view?bookcode=BN001023)
<br/><br/>














