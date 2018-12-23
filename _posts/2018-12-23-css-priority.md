---
title: "[CSS] CSS 적용 우선순위"
date: 2018-12-23 23:00:00 -0400
categories: CSS
---

CSS 적용 우선순위
=======

CSS는 선언하는 방법이 여러가지 입니다.
그렇기 때문에 이방법 사이에 충돌이 날 수 있으며 이는 예상치 못한 CSS 가 적용되는
결과를 낳을 수 있습니다. 그래서 CSS를 작성할때, 우선순위를 인지하는 것이 중요합니다.


적용 우선순위
------
1. 속성뒤에 !important를 기입
```
div {
  color:gray !important;
}
``` 
2. inline에 직접 기입(style) 
```
 <div id="one" style="color:gray" class="two"> 
```
3. id선택자 
```
#one {
  color:gray
}
``` 
4. class선택자 
```
.two {
  color:gray
}
```
5. type 
```
div {
  color:gray
}
```

만약 같은 순위에 있다면, 부모-자식 관계가 많을때 우선되고, 나중에 선언한 것이 우선시 됩니다.

아래는 선택자 우선순위 계산법입니다.

![image](/blog/assets/images/css_specificity.png)


참고 URL
------
[CSS우선순위](https://opentutorials.org/module/484/4149)

