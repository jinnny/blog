---
title: "[CSS] 나눔시리즈 경량화 웹폰트와 CDN"
date: 2019-03-14 16:00:00 -0400
categories: CSS 폰트경량화 웹폰트 CDN 나눔바른고딕 나눔스퀘어 나눔스퀘어라운드
---

나눔시리즈 폰트로 웹폰트 경량화 진행하기
=======


작업에 앞서..
---

웹폰트와 최적화에 대한 포스팅을 했었지만, 
웹폰트에 대한 고민은 늘 하고 있기에 나눔시리즈를 대상으로 웹폰트와 CDN을 진행하고자 포스팅을 하게 되었습니다.  
폰트를 웹에 적용하는 것은 참 쉽지 않은 작업 같습니다.    
한글은 한자와 함께 폰트가 만들어지는 경우가 많기때문에 그 용량이 어마어마하기 때문입니다.  

그러나 자주사용하는 한글에 대한 웹폰트를 서브셋으로 만들게 되면 커뮤니티와 같이 사용자가 어떤 글자를 쓸지 모를 상황에서 난감한 것 같습니다.  
한자를 사용할 경우에도 마찬가지입니다.    
현재 존재하는 커뮤니티 성격을 띄는 사이트를 살펴보니 굴림체, 돋움체와 같은 기본 폰트를 쓰는 것을 쉽게 찾아 볼 수 있었습니다.  
사용자가 글을 쓰는 게시판 부분에는 기본 폰트를 사용하고, 그 외 부분에는 기본 폰트가 아닌 다른 폰트를 사용하는 것도 하나의 방법이라 생각도 들었는데,
그런 경우에는 이질감이 생길 우려도 있는 것 같습니다.

그래서 기본적으론 서브셋을 만들되, 사이트의 목적에 따라 서브셋을 사용하지 않는 쪽이 좋을 것 같습니다.  

이번에 웹폰트로 만들어 CDN 으로 공유할 나눔시리즈는 아래와 같습니다.

1. '나눔바른고딕'
2. '나눔스퀘어'
3. '나눔스퀘어라운드'

서브셋 작업은 용량이 큰 '나눔바른고딕' 만 진행했습니다.


---

1. 나눔바른고딕
----
나눔바른고딕은 한글 11,172자, 한자 4,888자, 영문 94자, KS약물 986자 로 구성되어있으며,
ttf 기준 용량은 4.2MB ~ 4.9MB 입니다.  
서브셋 경량화 작업을 통해 용량은 1.3MB ~ 1.8MB 로 줄었습니다.

**1. 지원 언어**    
 1. 영어
 2. 한국어 (한자 불포함)
  
**2. 종류**  
1. UltraLight
2. Light
3. Regular 
4. Bold

**3. 서브셋 지정 글자**  
  
```
KS X 1001 완성형 한글 2,340자
        +   
노민지, 윤민구 “KS 코드 완성형 한글의 추가 글자 제안” 추가 글자 224자
        +
현대 한글의 낱자 51자
        +
Basic Latin 95자
       +
KS X 1001의 특수 문자 942자
```

**4. CDN 사용법**  

```
@import url('https://jinnny.github.io/publish_source/webfont/NanumBarunGothic/fonts.css');
```

```
font-family: 'NanumBarunGothic', Dotum ,'돋움', sans-serif;
```


2. 나눔스퀘어 (NanumSquare)
----
나눔스퀘어는 한글 2,350자, 영문 94자, KS약물 986자로 구성되어있으며,
ttf 기준 용량은 724KB ~ 751KB 입니다.

**1. 지원 언어**    
 1. 영어
 2. 한국어 (한자 불포함)
  
**2. 종류**  
1. Light
2. Regular 
3. Bold
4. ExtraBold

**3. CDN 사용법**  

```
@import url('https://jinnny.github.io/publish_source/webfont/NanumSquare/fonts.css');
```

```
font-family: 'NanumSquare', Dotum ,'돋움', sans-serif;
```


3. 나눔스퀘어라운드 (NanumSquareRound)
----
나눔스퀘어라운드는 한글 2,350자, 영문 94자, KS약물 986자로 구성되어있으며,
ttf 기준 용량은 1MB ~ 1.1MB 입니다.

**1. 지원 언어**    
 1. 영어
 2. 한국어 (한자 불포함)
  
**2. 종류**  
1. Light
2. Regular 
3. Bold
4. ExtraBold

**3. CDN 사용법**  

```
@import url('https://jinnny.github.io/publish_source/webfont/NanumSquareRound/fonts.css');
```

```
font-family: 'NanumSquareRound', Dotum ,'돋움', sans-serif;
```


* Weight의 경우  
    * ultralight = 100
    * thin = 200
    * light = 300
    * normal = 400
    * medium = 500
    * bold = 700
    * black/extrabold = 800

---


양식이 맞지 않아 통일하는데 커밋을 너무 많이 해버렸습니다 ㅜ  
최대한 여러브라우저에서 확인했지만, 간혹 변환기 오류로 확인이 안되는 경우가 발생합니다.  
피드백 주시면 개선하도록 하겠습니다.  



참고 URL
------
[onlinefontconverter](https://onlinefontconverter.com/)  
[nonria님의 블로그 - 웹 폰트로 사용하기 위한 서브셋 지정](https://nonria.com/post/96/)

