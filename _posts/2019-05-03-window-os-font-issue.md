---
title: "[CSS] 윈도우 OS 폰트 깨짐 이슈"
date: 2019-05-03 11:30:00 -0400
categories: CSS 웹폰트
tags: 윈도우 웹폰트 폰트깨짐 폰트찌그러짐 webfont
---

윈도우 운영체제에서 폰트가 깨져보이는 현상에 대해
======

최근에 **나눔바른고딕**을 웹폰트로 사용하다가 윈도우 OS 에서 폰트가 찌그러져? 보인다는 사실을 알게 되었습니다.  
폰트 사이즈가 작게 들어가기도 했구요.  

예전에는 이런현상을 인지 못했을까 하며 구글링과 작업물을 훑어보았는데..
전에 작업했던 폰트들은 폰트 사이즈가 크거나 NotoSans 여서 상대적으로 덜했던 것 같습니다.

물론 NotoSans였던 작업물도 폰트 사이즈를 줄였을 경우 이슈가 발생했구요.
거의 20px 이하에서 뭉개짐, 거친표현, 라인이 맞지 않는 등을 확인할 수 있었습니다.


------
MAC OS에서 보이는 화면(실제 디자인과 가장 흡사)

1. 나눔바른고딕   
![image](/blog/assets/images/mac_nanum.png)

2. NotoSansKR  
![image](/blog/assets/images/mac_notosans.png)

-----

------
윈도우에서 폰트가 뭉개짐, 거친표현 현상
  
1. 크롬 브라우저
   1. 나눔바른고딕  
   ![image](/blog/assets/images/before_window_nanum.png)
   2. NotoSansKR  
  ![image](/blog/assets/images/before_window_notosans.png)

2. IE 브라우저
   1. 나눔바른고딕  
   ![image](/blog/assets/images/before_window_ie_nanum.png)
   2. NotoSansKR  
   ![image](/blog/assets/images/before_window_ie_notosans.png)

------

자세히 보시면 겹치는 모음(ㄹ)과 같은 부분이 뭉개져서 보이는걸 아실 수 있으실 겁니다.  
사실 폰트가 커져도 거친표현은 그대로 남아있긴하나 상대적으로 덜해보이는 것입니다. 

이 이슈를 완벽히 종료시킬 방법은 현재 존재 하지 않는 것 같지만(있다면 알려주세요), 상대적으로 폰트가 부드럽게 보일 수 있는 방법은 존재합니다.

바로 CSS **transform** 속성을 이용하는 것입니다.
정확히 하면 transform의 rotate 를 통해 폰트를 살짝, 미세하게 돌려?주는 것입니다.

transform 의 rotate 수치를 확인하면서 작업했는데 -0.2 정도가 적당한 것 같았습니다.

```
-webkit-transform: rotate(-0.2deg);
-moz-transform: rotate(-0.2deg);
-ms-transform: rotate(-0.2deg);
-o-transform: rotate(-0.2deg);
transform: rotate(-0.2deg);
```

하지만 transform 속성(2D기준)은 IE 9 이상부터 지원하기 때문에 그외 하위 브라우저에서는 사용할 수 없습니다.  
또, 약간 폰트가 희미해 보이는 이슈도 존재합니다.
그리고 위 속성은 inline 요소에는 동작하지 않으니, inline-block를 추가해주시거나 block요소에 사용하셔야 합니다.  


-----
transform 속성을 적용한 경우

1. 윈도우
    1. 크롬 브라우저  
        1. 나눔바른고딕  
        ![image](/blog/assets/images/after_window_nanum.png)
        2. NotoSansKR  
        ![image](/blog/assets/images/after_window_notosans.png)
    2. IE 브라우저  
        1. 나눔바른고딕  
        ![image](/blog/assets/images/after_window_ie_nanum.png)
        2. NotoSansKR  
        ![image](/blog/assets/images/after_window_ie_notosans.png)

2. Mac  
   1. 크롬브라우저  
      1. 나눔바른고딕  
      ![image](/blog/assets/images/after_mac_notosans.png)
      2. NotoSansKR  
      ![image](/blog/assets/images/after_mac_notosans.png)   

-----


그래서 저는 ua-parser.js 라이브러리를 이용해 윈도우 OS에만 적용하도록 스크립트를 적용했습니다.


```
js 

var parser = new UAParser();
var result = parser.getOS();

if(result.name === 'Windows') {
    var body = document.getElementsByTagName('html')[0];
    body.classList.add('only-window');
}

Sass
.only-window {
  .for-window--text {
    -webkit-transform: rotate(-0.2deg);
    -moz-transform: rotate(-0.2deg);
    -ms-transform: rotate(-0.2deg);
    -o-transform: rotate(-0.2deg);
    transform: rotate(-0.2deg);
  }
}
```

이런 이슈에 대한 대비?가 안되있었기 때문에 코드를 적용하는데 애를 먹긴했지만
기획팀과 운영팀의 판단하에 폰트 뭉개짐은 상대적으로 예방할 수 있었습니다.  

다른 곳은 이러한 이슈에 대해 어떻게 대응하는지 궁금하고.. 네이버나 다음 등의 경우 주메뉴만 이미지로 처리한 이유가 이러한 이유와 관계가 있지는 않을까 했습니다.
(물론 하위브라우저와의 호환성 때문일 수도 있지만)

참고 URL
------
[Can i use transform?](https://caniuse.com/#search=transform)  
