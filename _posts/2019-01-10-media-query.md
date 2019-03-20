---
title: "[React] Media query Orientation, Media query로 가로세로 방향이 체크가 가능할까?"
date: 2019-01-10 11:30:00 -0400
categories: CSS 
tags: CSS 미디어쿼리 MediaQuery
---

Media query  Orientation
=============

다양한 디바이스들이 출시되면서 그에 대응하기 위한 기술들이 많이 사용되었습니다.
그 중 하나가 흔히 @media 규칙이라 부르는 Media query입니다. 

기존에 CSS Media query는 인쇄매체를 제외하고는 사용이 불가했지만, CSS3 에서는 인쇄매체 외에도 사용이 가능하며
기능이 확장되었습니다. (뷰포트의 너비와 높이, 장치의 너비와 높이, 방향 (가로 또는 세로 모드의 태블릿 / 휴대전화),해결)
이로인해 Media query의 사용은 데스크톱, 랩톱, 태블릿 및 휴대 전화 (예 : iPhone 및 Android )에 맞춤 스타일 시트를 제공하는 데 널리 사용되는 기술이 되었습니다.

간단한 Media query 사용법에 대해 알아보고, 요소중 하나인 방향에 대해 이야기하겠습니다,

코드
----
```
@media not|only mediatype and (expressions) {
  CSS-Code;
}
(ex) 
@media screen and (max-width: 600px) {
  .row {
    flex-direction: column;
  }
}

<link rel="stylesheet" media="mediatype and|not|only (expressions)" href="print.css">
(ex) 
<link rel="stylesheet" media="screen and (max-width: 600px)" href="print.css">
```

기본적으로 위와 같이 작성하며, 전자의 표현은 css파일 내부에 작성하는 경우이고,
후자의 표현은 css 파일 전체에 Media query 가 적용되도록 작성하는 경우입니다.
두 방법다 좋다 나쁘다는 없지만, 개인적으로는 최근 홈페이지들이 Responsive Web 으로 제작되는 것을 고려했을 때 첫번째
표현이 효율적인 코드 관리 방법이라 생각됩니다.


Media query로 가로세로 방향이 체크가 가능할까? 
----
네 가능합니다.
Orientation 을 이용하면 됩니다.
이 표현은 viewport의 방향을 지정합니다. 
가로방향(브라우저 윈도우의 높이가 가로보다 큰 경우에만 적용)일때는 landscape를, 
세로방향일땐 portrait를 지정할 시 참을 반환합니다.


```
@media all and (orientation: landscape) and (max-width: 500px) {
  body {
    background-color: lightblue;
  }
}
//viewport 가로가 500이하이고, 가로일때 작동
```

위와 같이 작성하시면 되며,
이 값은 반드시 일치 하지는 않는 예외의 경우들이 존재합니다(소프트키보드)



참고 URL
-------
[CSS3 CSS Media Queries - Examples](https://www.w3schools.com/css/css3_mediaqueries_ex.asp)

[CSS미디어 쿼리에 대해](https://developer.mozilla.org/ko/docs/Web/Guide/CSS/Media_queries)
