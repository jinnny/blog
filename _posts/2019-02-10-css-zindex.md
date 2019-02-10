---
title: "[CSS] CSS z-index"
date: 2019-02-10 11:00:00 -0400
categories: CSS z-index
---

CSS z-index Property
=======

z-index는 순서를 조정해주는 Property입니다. 
2차원이 아닌 3차원 이며, x,y,z의 z값이라고 생각하시면 됩니다. 
z-index는 0에서 양수 음수 값을 모두 가질 수 있습니다.

Style을 잡을때 자주 사용하지만,
의외로 무분별? 하게 사용될 때가 많습니다.

무조건 값을 높게 잡는다면 그 위에 다른 요소를 올려야 할때 값을 조정해야할 가능성이 높아지고
그 개수가 늘 때마다 그럴 가능성이 높아집니다.
그래서 z-index는 차곡차곡 쌓아가는 것이 중요하다고 생각합니다.
처음 사용할때부터 1씩 값을 올려가거나 자릿수별로 값을 주는 등의 규칙성을 이용해 작업하는 것을 선호합니다.

주의 하실 점이 있습니다. 

! z-index only works on positioned elements (position:absolute, position:relative, or position:fixed).
z-index는 오직, position값이 absolute, relative , fixed 로 되어있을때만 작동이 가능합니다.

만약, z-index값을 설정했는데도 작동되지 않는다..하시면 position 값을 봐주시면 됩니다!

사용법은 아래와 같습니다.

사용법
-------

```
div {
 position: relative;
 z-index: 20;
}
```

지원브라우저
-----

![image](/blog/assets/images/zindex.png)

지금 사용하는 거의 대부분의 브라우저를 지원하고 있으니 사용하실 때 어려움은 없을 것입니다.


참고 URL
------
[CSS z-index Property](https://www.w3schools.com/cssref/pr_pos_z-index.asp)

