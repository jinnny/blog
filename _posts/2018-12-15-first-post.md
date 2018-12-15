---
title: "[HTML5] H1 태그는 몇번 사용할 수 있을까?"
date: 2018-12-15 17:15:00 -0400
categories: HTML5 update
---

H1 태그는 몇번 사용할 수 있을까?
=============

예전, H1태그에 대해 의문을 품었던 적이 있습니다.
어디서는 한번만 사용해야한다. 아니다. 여러번 사용이 가능하다.
라고 되어있어 혼란스러웠습니다.

그래서 W3C 권고안을 읽고 공부하게 되면서 무엇이 맞는지 정리가 되었습니다.

아래는 W3C HTML5 Recommendation에서, h1-h6까지의 내용입니다.


> These elements represent headings for their sections. 
The semantics and meaning of these elements are defined in the section on headings and sections. 
These elements have a rank given by the number in their name. The h1 element is said to have the highest rank, the h6 element has the lowest rank, and two elements with the same name have equal rank. 
h1-h6 elements must not be used to markup subheadings, subtitles, alternative titles and taglines unless intended to be the heading for a new section or subsection. Instead use the markup patterns in the Common idioms without dedicated elements section of the specification.


살펴보자면, 사용 횟수 제한에 대한 내용은 존재 하지 않고, 섹션에 따라 정의 하면 된다고 나와있습니다.
무엇보다 중요한 것은 .. h1 부터 h6까지 순차적으로 잘 사용하였나 여부인 것 같습니다. 중간에 태그를 생략하고 다음 우선순위의 태그를 사용한다던지에 대한 것이요.
살펴보니, HTML5에 대한 W3C의 권고안도 계속 업데이트 되는 중이더군요. 앞으로 계속 살피며 연구해야 할 것 같습니다.


참고url
------------------
<https://www.w3.org/TR/2011/WD-html5-20110525/sections.html> <br>
<https://developer.mozilla.org/en-US/docs/Web/Guide/HTML/Using_HTML_sections_and_outlines>
