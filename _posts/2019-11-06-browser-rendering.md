---
title: "브라우저 렌더링 성능 최적화"
date: 2019-11-06 12:20:00 -0400
categories: 브라우저 렌더링
tags: 성능최적화
---


브라우저 렌더링 과정  
------
바이트-> 문자 -> 토큰 -> 노드 -> 객체모델   
HTML 마크업은 DOM으로 변환, CSS 마크업은 CSSOM 으로 변환됩니다.  

DOM 과 CSSOM은 렌더링 트리(렌더링에 필요한 노드만 포함: 스크립트,메타태그 생략됨)를 형성(거를거 거르고, 일치하는 CSSOM 규칙 적용시킴) -> 
Reflow (layout: 정확한 위치및 크기 계산) -> Repaint (페인팅:픽셀을 화면에 렌더링) -> Composite (합성: 여러가지로 나뉜 레이어를 정확한 순서로 그리는 일)

HTML 마크업 처리후 DOM 트리 빌드 -> CSS 마크업 처리 후 CSSOM 트리 빌드 -> DOM 트리와 CSSOM 트리를 결합해 렌더링 트리 형성 -> 렌더링 트리에서 레이아웃 실행해 각 노드의 기하학적 형태 계산 -> 개별 노드를 화면에 페인트

렌더링 성능 최적화는 위 단계의 시간을 최소화 하는 것.
------

기하적인 영향을 주는 CSS 속성값(아래 참조)을 변경하는 경우 Reflow (layout: 정확한 위치및 크기 계산) 과정을 다시 수행한다. Reflow가 일어나면 전체 픽셀을 다시 계산해야하기 때문에 부하가 큽니다.   
그래서 꼭 필요한 경우가 아닌 경우에는 렌더링 성능 최적화를 위해 지양해야 합니다.  
반대로 위치나, 높이 등의 기하적인 영향을 주지않는 CSS 속성값을 변경하는 경우에는 브라우저는 Repaint 부터 다시 수행합니다.
  
속성
------

1. Reflow가 일어나는 대표적인 속성  

```
 Position, width, height, left, top, right, bottom, margin, padding, border, border-width, clear, display, float, font-family, font-size, font-weight, line-height, min-height, overflow, text-align, vertical-align, white-space 등 
 위치를 설정할때 사용되는 속성이 대부분 포함됩니다.
```

2. Repaint만 일어나는 대표적인 속성
```
 Background, background-image, backgound-position, background-repeat, background-size, border-radius, border-style, box-shadow, color, line-style, outline, outline-color, outline-style, outline-width, text-decoration,  visibility 등
 위치와 관계없이 형태만을 변경 시키는 속성들이 대부분 포함됩니다.
```

3. reflow와 repaint 과정 없이 일어나는(Composite 만 일어남) 대표적인 속성
```
  Transform, opacity, cursor, orphans, perspective 등 
```

* 브라우저 렌더링은 브라우저 엔진마다 내용이 다르기 때문에, 속성별 렌더링 과정여부는 아래 URL을 참조하시는 것이 더욱 정확합니다.

https://csstriggers.com/

reflow 최소화하기
----

앞서 말씀드린대로 불필요한 경우에는 지양해야하지만 꼭 필요한 경우에 reflow 성능 문제를 최소화하는 방법을 소개하고자 합니다.  


1. 자식이 없는 엘리먼트에 해당 속성 추가하기(최하단)  
   : 자식이 있는 엘리먼트에 속성을 추가하게 되면 그 부모가 reflow되면서 자식까지 영향을 미치게 되기 때문에 성능이 떨어지게 됩니다.

2. reflow가 발생할 속성을 사용한 애니메이션의 경우 해당 요소만 적용이 되도록 position값을 absolute 나 fixed 로 적용하기  
   : 해당 요소만 적용이 되기때문에 성능 문제를 최소화 할 수 있습니다.


이 글은 아래 참고 URL의 내용을 요약한 짧은 형태입니다.  보다 자세한 내용은 참고 URL을 참조하세요.


참고 URL
------
[브라우저 렌더링 성능 최적화 - Repaint가 일어나지 않는 CSS 속성](https://boxfoxs.tistory.com/409)
[객체 모델 생성](https://developers.google.com/web/fundamentals/performance/critical-rendering-path/constructing-the-object-model?hl=ko)
[컴포지터(compositor) 전용 속성 고수 및 레이어 수 관리](https://developers.google.com/web/fundamentals/performance/rendering/stick-to-compositor-only-properties-and-manage-layer-count)
[CSS 애니메이션 성능 개선 방법(reflow 최소화, will-change 사용)](https://wit.nts-corp.com/2017/06/05/4571)
