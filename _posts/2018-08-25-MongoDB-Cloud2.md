---
title: "MongoDB에서 데이터 추출해 wordcloud만들기(2)"
date: 2018-08-25
categories: articles
---

[MongoDB에서 데이터 추출해 wordcloud만들기(1)](https://soohyunii.github.io/articles/MongoDB-Cloud/)포스팅에 이어 wordcloud를 본격적으로 만들어 보겠다.  

---
**1. 파이썬에서 필요한 모듈 설치**  
먼저 파이썬을 실행한 뒤 Counter, Twitter, pytagcloud를 설치해주어야한다. (필자의 경우 IDE는 스파이더(Spyder)를 사용했다)  
그외에도 필요한 설치파일이 있을 수 있다. 필요한 경우 **pip install [설치할 모듈이름]**로 설치한다.  
```
from collections import Counter
from konlpy.tag import Twitter
import pytagcloud
```  


**2. 파이썬에서 csv파일 가져오기**  
csv파일을 가져오는 코드는 아래와 같다.  
```
f = open('text.csv','rt',encoding='UTF-8')
data = f.read()
```  


**3. csv파일로 wordCloud 만들기**  
파이썬에서 불러온 csv파일을 wordCloud로 만드는 코드는 아래와 같다.   
```
nlp = Twitter()
nouns = nlp.nouns(data)
count = Counter(nouns)
tags2 = count.most_common(40)
taglist = pytagcloud.make_tags(tags2, maxsize=80)
pytagcloud.create_tag_image(taglist, 'wordcloud3.jpg', size=(900, 600), fontname='SourceHanSerifk-Medium', rectangular=False)
f.close()
```  

이때, 6번째 줄에 있는 fontname='SourceHanSerifk-Medium' 은 직접 다운받은 글씨체로,  
패키지가 한글을 지원하도록 [글씨체를 다운받고](https://github.com/adobe-fonts/source-han-serif/blob/release/OTF/Korean/SourceHanSerifK-Medium.otf), [font.json파일의 설정도 수정](https://thinkwarelab.wordpress.com/2016/08/30/%ED%8C%8C%EC%9D%B4%EC%8D%AC-%ED%98%95%ED%83%9C%EC%86%8C-%EB%B6%84%EC%84%9D%EC%9C%BC%EB%A1%9C-%EC%9B%8C%EB%93%9C%ED%81%B4%EB%9D%BC%EC%9A%B0%EB%93%9C-%EA%B7%B8%EB%A6%AC%EA%B8%B0/)해주어야 한다.  
참고로 필자는 C:\Anaconda\Lib\site-packages\pytagcloud\fonts 경로에서 다운받은 폰트(SourceHanSerifk-Medium)를 추가하고,  
아래와 같이 font.json파일에도 폰트를 추가해주었다.  
![234234](https://user-images.githubusercontent.com/29648470/44616747-47e8db80-a890-11e8-9062-c5c3fa3f9f42.png)  
![123123](https://user-images.githubusercontent.com/29648470/44616722-ddd03680-a88f-11e8-84b3-04530729c151.png)  


**4. 최종정리 및 결과**  
자, 지금까지 살펴본 내용을 종합하면 다음과 같다.  
- 전체 코드 : 파일명 testword2.py
```
from collections import Counter
from konlpy.tag import Twitter
import pytagcloud
f = open('text.csv','rt',encoding='UTF-8')
data = f.read()
nlp = Twitter()
nouns = nlp.nouns(data)
count = Counter(nouns)
tags2 = count.most_common(40)
taglist = pytagcloud.make_tags(tags2, maxsize=80)
pytagcloud.create_tag_image(taglist, 'wordcloud3.jpg', size=(900, 600), fontname='SourceHanSerifk-Medium', rectangular=False)
f.close()
```  
- C:\Anaconda\Lib\site-packages\pytagcloud\fonts에 한글 폰트 다운받은 후 같은 경로의 font.json파일에 폰트 추가  
- testword2.py 실행  
![345345](https://user-images.githubusercontent.com/29648470/44616778-2fc58c00-a891-11e8-8519-71677549259c.png)  
콘솔창에 다음과 같은 결과가 뜨면서 위의 경로에 wordcloud3.jpg 파일이 생성된다.  
- wordcloud3.jpg확인  
![456456](https://user-images.githubusercontent.com/29648470/44616787-55eb2c00-a891-11e8-9977-6834adae1887.png)  


최종적으로 위와같은 wordCloud를 출력할 수 있다. 







