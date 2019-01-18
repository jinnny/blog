---
title: "[CSS] CSS 적용 우선순위 계산"
date: 2019-01-18 14:30:00 -0400
categories: CSS
---

CSS 적용 우선순위 계산하기
=======

지난 포스팅에서 CSS 적용 우선순위를 작성한 적이있습니다.
부족한 점이 있는지라, 이번 포스팅에서는 예시를 들어 자세히 작성해보려합니다.

우선순위는 1000, 100, 10, 1 단위로 계산이 가능합니다.
오름차순으로 갈수록 그 단위가 낮습니다.

우선순위
----------
1.inline style 을 선언할 경우 (1000)
```
ex) h1 style="font-size: 15px;"
```

2.ID 를 이용해 선언할 경우 (100)
```
ex) #test { font-size: 15px; }
```

3.Class를 이용해 선언
- class를 이용해 선언할 경우 (10)
```
ex) .test { font-size: 15px; }
```

- 가상클래스(pseudo-class)를 이용해 선언할 경우  (10)
```
ex) :active  :checked  :disabled  :empty  :enabled
:first  :first-child  :first-of-type :focus
:hover  :last-child  :last-of-type  :left
:link  :nth-child()  :nth-last-child()
:nth-last-of-type()  :nth-of-type()
:only-child  :only-of-type
:read-only  :read-write
:required :right :target :valid :visited 등등
```
- 속성 선택자를 이용해 선언할 경우 (10)
```
ex) input[type="submit"] { font-size: 15px;}
```

4. Element 를 이용해 선언
- element를 이용해 선언할 경우(1)
```
ex) h1 { font-size: 15px; }
```

- 가상엘리먼트(pseudo element)를 이용해 선언할 경우(1)
```
ex) ::after, ::before 등
```

※ !important 는 같은상황에서 가장 강력합니다.
 (사실 이 속성은 강제적이기 때문에 특별한 경우를 제외하고는 사용을 지양하시는 것이 좋습니다).
※ :not()과, *, +, > , ~ 는 아무 효과가 없습니다(0). 
계산에서 제외됩니다.

위를 바탕으로 계산을 해보겠습니다.
```
ex) ul.tab li.on #btn
▶ ID -> 1(100) , class -> 2(10*2=20) , element -> 2(1*2=2) 로 총 122입니다.
```
참고로 class 나 ID값을 element와 같이 배치하더라도, element 값까지 더 해야 합니다.

감안해야할게 많고 저도 종종 헷갈리지만, 계산이 가능하다면 보다 명확하게 style 을 줄 수 있습니다.
아래 사이트를 참고했으며, 보다 자세한 설명이 영어로 준비되어 있습니다



참고 URL
------
[Specifics on CSS Specificity](https://css-tricks.com/specifics-on-css-specificity/)

