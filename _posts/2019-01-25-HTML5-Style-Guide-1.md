---
title: "[HTML5] 웹표준을 준수하는법! HTML5 Style Guide 1"
date: 2019-01-25 15:30:00 -0400
categories: HTML5 웹표준
tags: HTML5 웹표준 
---

작성자의 ~카더라 보다는 직접 원문을 보고 해석해서 보고 싶었기에 저는 이 부분을 직접 번역해 보기로 결심했습니다.
W3CSchool의 내용 중에서 오늘은 HTML5 전체 구성에 대한 대략적인 HTML5 Style Guide을 살펴보도록 하겠습니다.
내용이 꽤 많아서 두번정도 나누어 올리겠습니다.


HTML5 Style Guide and Coding Conventions
=======

HTML Coding Conventions
-----
HTML5 스타일 안내서 , 코딩 관습

Web developers are often uncertain about the coding style and syntax to use in HTML.<br>
웹 개발자들은 보통 html 문법과 코딩 스타일을 정확히 모르고 있습니다.(확신이 부족합니다.)

Between 2000 and 2010, many web developers converted from HTML to XHTML.<br>
2000년-2010년 사이에, 많은 웹개발자들은 HTML에서 XHTML로 변형시켰습니다(HTML말고, XHTML을 사용하기 시작했다는 뜻 같네요).

With XHTML, developers were forced to write valid and "well-formed" code.<br>
XHTML에서, 개발자들은 유효하고 "체계적인(잘 구성된)"코드를 쓰도록 강요받았습니다. 

HTML5 is a bit more sloppy when it comes to code validation.<br>
HTML5는코드 유효성에 있어서, 약간더  헐렁합니다.(XHTML 보다 유연하다는 느낌)


Be Smart and Future Proof<br>
---------
깔끔해지고 미래에도 경쟁력 있다

A consistent use of style, makes it easier for others to understand your HTML.<br>
style의 일관된 사용은 당신의 HTML을 다른이가 더 쉽게 이해하도록 만듭니다.

In the future, programs like XML readers, may want to read your HTML.<br>
미래에, XML reader들과 같은 프로그램은 아마 당신의 HTML을 읽고싶을 겁니다(미래에는 여러 프로그램이 HTML파일을 읽을 것이라는 뜻입니다.)

Using a well-formed-"close to XHTML" syntax, can be smart.<br>
"XHTML과 가까운"  문법 규칙에 맞는 문법의 사용은 깔끔해 질 수 있습니다.

*Always keep your code tidy, clean, and well-formed.<br>
항상 당신의 코드를 잘정리하고, 깔끔하고, 규칙에 맞게 유지하세요.



Use Correct Document Type
-------
맞는 문서 타입을 사용하세요

Always declare the document type as the first line in your document:<br>
문서타입은 항상 당신의 문서 첫번째 줄에 정의해야합니다
```
<!DOCTYPE html>
```

If you want consistency with lower case tags, you can use:<br>
소문자 태그들로 일관성을 유지하고 싶으시면 사용하실 수 있습니다.
```
<!doctype html>
```

Use Lower Case Element Names
-----
소문자 요소 이름 사용하기

HTML5 allows mixing uppercase and lowercase letters in element names.<br>
HTML5는 대문자와 소문자를 요소이름으로 섞는 것을 허용하지만...

We recommend using lowercase element names because:<br>
우리(W3C)는 요소이름에 소문자를 사용하는 것을 권고합니다. 왜냐하면

Mixing uppercase and lowercase names is bad<br>
소문자와 대문자 이름을 섞어쓰는 것은 좋지않으며,

Developers normally use lowercase names (as in XHTML)<br>
개발자들은 보통 소문자를 사용하고, (XHTML 에서) 써왔기때문에

Lowercase look cleaner<br>
소문자는 깔끔해 보이며

Lowercase are easier to write<br>
소문자는 쓰기 쉽기 때문입니다. (고로 소문자를 사용하세요~)

1.Bad
```
<SECTION> 
  <p>This is a paragraph.</p>
</SECTION>
```

2.Good
```
<section> 
  <p>This is a paragraph.</p>
</section>
```


Close All HTML Elements
-----
모든 HTML 요소를 닫으세요(열고 닫기를 잘하세요)

In HTML5, you don't have to close all elements (for example the <p> element).<br>
HTML5에서, 당신은 모든 요소를 닫을 닫을 필요가 없었습니다(예를 들면, <p>요소같은 것들)

We recommend closing all HTML elements.<br>
우리는 모든 HTML 요소닫기를 권고합니다.(이제) 


Close Empty HTML Elements
-----
무의미한 HTML 요소를 닫으세요

In HTML5, it is optional to close empty elements.<br>
HTML5에서, 무의미한 요소를 닫는 것은 선택사항입니다.

```
Allowed: 허용됨
<meta charset="utf-8">
Also Allowed: 또한 허용됨
<meta charset="utf-8" />
```

However, the closing slash (/) is REQUIRED in XHTML and XML.<br>
하지만, 닫는 슬러쉬(/)는 XHTML 과 XML 에 필요합니다.

If you expect XML software to access your page, it is a good idea to keep the closing slash!<br>
당신은 당신의 페이지가  XML 소프트웨어에 접속될 것이라고 예상한다면, 닫는 슬러쉬를 유지하는 것은 좋은 생각입니다!


Quote Attribute Values
-----
요소 값에 따옴표 사용하기

HTML5 allows attribute values without quotes.<br>
HTML5는 따옴표 없이 요소 값을 허용합니다.

We recommend quoting attribute values because:<br>
(하지만)우리는 요소값에 따옴표를 붙이는 것을 권고합니다. 왜냐하면

Mixing uppercase and lowercase values is bad<br>
대문자와 소문자 값이 섞이는 것은 좋지않으며,

Quoted values are easier to read<br>
따옴표가 붙은 값이 읽기 쉽고

You MUST use quotes if the value contains spaces<br>
값이 띄어쓰기(space)를 포함하고 있다면 당신은 무조건!! 따옴표를 사용해야하기 때문입니다.


Image Attributes
----
이미지 요소들

Always add the "alt" attribute to images. This attribute is important when the image for some reason cannot be displayed. Also, always define image width and height. It reduces flickering because the browser can reserve space for the image before loading.<br>
이미지들에는 항상 alt 요소를 붙이세요. 어떤 이유로 앞을 볼 수 없을 때, 이 요소는 중요합니다. 또한, 항상 이미지의 넓이와 높이를 정하세요.  그것은 깜빡거림을 감소해줍니다. 왜냐하면, 브라우저는 로딩 전에 이미지의 공간을 남겨둘 수 있기 때문입니다. ( 미리 값을 정해놓으면 바로 그 자리에 이미지가 들어와 깜빡임이 줄어든다는 의미)

1.Bad
```
<img src="html5.gif">
```

2.Good
```
<img src="html5.gif" alt="HTML5" style="width:128px;height:128px">
```


참고 URL
------
[HTML5 Style Guide](https://www.w3schools.com/html/html5_syntax.asp)

