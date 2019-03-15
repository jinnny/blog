---
title: "[HTML5] fieldset tag 와 legend tag"
date: 2019-02-23 13:00:00 -0400
categories: HTML5
tags: HTML5 fieldset legend
---

form 구성요소 fieldset와 legend tag
=======

form을 구성하기 위해서는 마크업적으로 고려해야할 사항이
꽤 많습니다.

그 중에서도 fieldset tag와 legend tag 에 대해 포스팅하고자 합니다.

먼저, fieldset tag는  같은 목적을 가진 위젯들을 편리하게 그룹화 하는 태그입니다.<br>
그룹화한 주위에 박스를 그리는 특징을 가지고 있으며,
이 태그는 legend 와 함께 쓰입니다.

legend tag는 fieldset 요소에 대한 캡션을 정의합니다. <br>
table tag와 함께 사용하는 caption tag 과 비슷하다고 생각하시면 이해가 더 쉬울 것 같습니다.


사용법
-------

```
<form>
  <fieldset>
    <legend>Personalia:</legend>
    Name: <input type="text"><br>
    Email: <input type="text"><br>
    Date of birth: <input type="text">
  </fieldset>
</form>
```


참고 URL
------
[HTML fieldset Tag](https://www.w3schools.com/tags/tag_fieldset.asp)

