---
title: "[CSS] :(single colon)과 ::(double colon)의 차이"
date: 2018-12-25 12:00:00 -0400
categories: CSS
tags: CSS colon
---

:(single colon)과 ::(double colon)의 차이
=======

pseudo-classes(가상클래스)나 pseudo-elements(가상엘리멘트)를 사용할 때 : 와 ::을 본 적이 있어, 그 둘의 차이가 무엇인지
궁금했었고 그 내용을 포스팅하려합니다.

간단히 말하자면, 이 둘은 브라우저 지원에 따라 달리 쓰이는 것입니다.
모든 브라우저는 ::(double colon)을 지원하지만, IE 8의 경우 :(single colon)만 지원합니다.

아래는 그 차이점을 찾았던 사이트의 원문 내용입니다.

css-tricks
------
> Every browser that supports the double colon (::) CSS3 syntax also supports just the (:) syntax, but IE 8 only supports the single-colon, so for now, it's recommended to just use the single-colon for best browser support. 
   :: is the newer format indented to distinguish pseudo content from pseudo selectors. If you don't need IE 8 support, feel free to use the double-colon.

> 모든 브라우저들은 :: (double colon)을 지원하고, CSS3 문법 에서는 :(single colon)또한 지원합니다.
  하지만, IE 8는 오직 :(single colon)만을 지원하기때문에, 현재는 :(single colon)을 사용하는것이 최상의 방법입니다. 
  그렇지만, :: (double colon)은 가상선택자와 가상컨텐츠를 구별할 수 있는 더 새로운 포멧입니다.
  (여기는 컨텐츠로 되어있는데, 사실 가상클래스 ex: hover,focus 등을 구분하기 위함입니다. ) 


W3Cschool
------
이 내용에서 W3Cschool에 있는 내용을 덧붙이자면,

> The double colon replaced the single-colon notation for pseudo-elements in CSS3. This was an attempt from W3C to distinguish between pseudo-classes and pseudo-elements. 
  The single-colon syntax was used for both pseudo-classes and pseudo-elements in CSS2 and CSS1. 
  For backward compatibility, the single-colon syntax is acceptable for CSS2 and CSS1 pseudo-elements.

> W3C는 pseudo-classes(가상 클래스)와 pseudo-elements(가상 엘리먼트)의 구분을 위한 시도로 ::(double colon)을 도입했다


위 내용을 종합해보면..
가상클래스는 :(single colon)을 사용하고, 가상엘리먼트또한 :(single colon)을 사용하기때문에,
이를 구분하기위해 W3C에서는 가상엘리먼트에 ::(double colon)을 사용하도록 제안한 것이라는 결론이 납니다.

하지만, IE8 에서는 ::(double colon) 를 지원하지 않기때문에, 제 생각에는
IE8까지 호환성이 필요한 경우에만 이를 :(single colon)를 사용하고, 나머지 경우에는 ::(double colon)를 구분해서 사용하는게 좋을 것 같습니다.
* 가상엘리먼트의 경우입니다.


참고 URL
------
[css-tricks](https://css-tricks.com/almanac/selectors/a/after-and-before/)
[W3Cschool CSS Pseudo-elements](https://www.w3schools.com/css/css_pseudo_elements.asp)

