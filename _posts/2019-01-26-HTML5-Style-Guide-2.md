---
title: "[HTML5] 웹표준을 준수하는법! HTML5 Style Guide 2"
date: 2019-01-26 11:00:00 -0400
categories: HTML5 웹표준 
---

지난번 포스팅에 이은 HTML5 Style Guide 두번째 포스팅입니다.


HTML5 Style Guide and Coding Conventions
=======

Spaces and Equal Signs
----
공간과 등호<br>

HTML5 allows spaces around equal signs. But space-less is easier to read, and groups entities better together.<br>
HTML5는 등호 주위에 공간을 허용합니다. 하지만, 공간이 적은 것이 읽기가 더 쉽고, 더 잘 그룹화합니다.

Avoid Long Code Lines
----
긴 코드줄을 피하세요.

When using an HTML editor, it is inconvenient to scroll right and left to read the HTML code.
Try to avoid code lines longer than 80 characters.<br>
HTML 편집기를 사용할때, 오른쪽이나 왼쪽으로 스크롤이 생기는 것은 HTML 코드를 읽기 불편합니다. 80개의 캐릭터들보다 긴 코드 작성을 피하도록 노력하세요.

Blank Lines and Indentation
-----
빈 줄과 들여쓰기

Do not add blank lines without a reason.<br>
이유없이 빈 줄을 만들지 마세요.

For readability, add blank lines to separate large or logical code blocks.<br>
읽기 쉬움을 위해, 크거나 논리적인 코드 블록들을 분리하기 위해 빈줄을 추가하세요.

For readability, add two spaces of indentation. Do not use the tab key.
Do not use unnecessary blank lines and indentation. It is not necessary to indent every element:<br>
읽기 쉬움을 위해, 들여쓰기 두칸을 하세요. tab키(키보드의 키)를 사용하지마세요.<br>
불필요한 빈 줄과 들여쓰기를 하지마세요. 들여쓰기가 필요없는 모든 요소입니다.


Omitting <html> and <body>?
-------------
html 과 body를 생략하는 것?

In the HTML5 standard, the html tag and the body tag can be omitted.<br>
The following code will validate as HTML5:<br>
HTML5 표준에서(따르면) , html 태그와 body 태그는 생략될 수 있습니다.<br>
다음의 코드는 HTML5로써 유효할 것입니다.<br>


```
<!DOCTYPE html>
<head>
  <title>Page Title</title>
</head>

<h1>This is a heading</h1>
<p>This is a paragraph.</p>
```


However, We do not recommend omitting the html and body tags. <br>
The html element is the document root. It is the recommended place for specifying the page language:<br>
하지만 우리는 html태그와 body태그를 생략하는 것을 권고하지 않습니다.<br>
html요소는 문서의 뿌리입니다. 페이지언어를 열기위해 권고되는 위치입니다.<br>

```
<!DOCTYPE html>
<html lang="en-US">
```

Declaring a language is important for accessibility applications (screen readers) and search engines.<br>
언어를 선언하는 것은 검색엔진과 접근가능한 어플리케이션 (스크린 리더)에게 중요합니다.

Omitting html or body can crash DOM and XML software.<br>
Omitting body can produce errors in older browsers (IE9).<br>
html나 body를 생략하는 것은 돔과 XML 소프트웨어가 충돌할 수 있습니다.<br>
body를 생략하는 것은 오래된 브라우저(IE9 같은..)에게 오류들을 띄울 수 있습니다.


Meta Data
------------

The title element is required in HTML5. Make the title as meaningful as possible:<br>

```
<title>HTML5 Syntax and Coding Style</title>
```

HTML5에서 title 요소는 필수입니다.<br>
타이틀을 가능한한 의미있게 만듭니다.(최대한 의미있음..)

To ensure proper interpretation, and correct search engine indexing, both the language and the character encoding should be defined as early as possible in a document:<br>
제대로된 해석을 보장하고  검색 엔진 인덱싱을 바로잡기 위해, 언어와 형태 인코딩은 문서에서 가능한 한 빨리 정의되어야 합니다.(meta 태그가 우선적으로 적용되어야한다.)


Setting The Viewport
-------
뷰포트 설정하기

HTML5 introduced a method to let web designers take control over the viewport, through the meta tag.<br>
HTML5는  웹디자이너가 메타 뷰포트를 통제할 방법을 소개했습니다.

The viewport is the user's visible area of a web page. It varies with the device, and will be smaller on a mobile phone than on a computer screen.<br>
뷰포트는 웹페이지에서 사용자 기기의 보이는 영역입니다. 기기에 의해 변합니다. 그리고 컴퓨터 스크린보다 휴대폰에서 작을 것입니다.

You should include the following meta viewport element in all your web pages:<br>
당신은 모든 당신의 웹페이지안에  다음의 meta 태그와 같은 뷰포트 요소를 포함해야합니다.

```
<meta name="viewport" content="width=device-width, initial-scale=1.0">
```


A meta viewport element gives the browser instructions on how to control the page's dimensions and scaling.<br>
meta 뷰포트 요소는 브라우저에게 페이지의 크기와 크기조정을 컨트롤할 방법을 줍니다.

The width=device-width part sets the width of the page to follow the screen-width of the device (which will vary depending on the device).<br>
width=device-width 부분은 (디바이스에 따라 다양한)디바이스의 스크린 넓이에 따른 웹페이지의 넓이를 설정합니다.

The initial-scale=1.0 part sets the initial zoom level when the page is first loaded by the browser.<br>
initial-scale=1.0 부분은 브라우저에 페이지가 처음으로 로딩되었을때 초기의 줌값을 설정합니다.

Here is an example of a web page without the viewport meta tag, and the same web page with the viewport meta tag:<br>
여기에 뷰포트태그가 없눈 웹페이지와 뷰포트태그가 있는 웹페이지의 예가 있습니다.


![image](/blog/assets/images/viewport.png)


Tip: If you are browsing this page with a phone or a tablet, you can click on the two links below to see the difference.
팁: 당신이 이 페이지를 폰이나 태블릿과 브라우징하고싶으시다면 차이점을ㅡㅡ 아래 두 링크를 클릭할 수 있습니다


참고 URL
------
[HTML5 Style Guide](https://www.w3schools.com/html/html5_syntax.asp)
