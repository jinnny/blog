---
title: "[HTML5] 웹표준을 준수하는법! HTML5 Style Guide 3"
date: 2019-01-27 13:05:00 -0400
categories: HTML5 웹표준 
tags: HTML5 웹표준
---

지난번 포스팅에 이은 HTML5 Style Guide 마지막 포스팅입니다.


HTML5 Style Guide and Coding Conventions
=======


HTML Comments
-----
html 주석

Short comments should be written on one line, like this:
```
<!-- This is a comment -->
```
짧은 주석은 이처럼 한 라인에 쓰여져야합니다. 

Comments that spans more than one line, should be written like this:
```
<!-- 
  This is a long comment example. This is a long comment example.
  This is a long comment example. This is a long comment example.
-->
```
한줄보다 긴 주석은 이처럼 쓰여져야합니다.

Long comments are easier to observe if they are indented two spaces. <br>
긴 주석은  2칸이 들여쓰기되어져있다면 보기 쉬울겁니다. 

Style Sheets
-----
스타일시트

Use simple syntax for linking to style sheets (the type attribute is not necessary):
```
<link rel="stylesheet" href="styles.css">
```
스타일 시트를 링크시키기 위해 간단한 문법을 사용해야합니다.(타입 속성은 필요하지 않습니다)

Short rules can be written compressed, on one line, like this:
```
p.intro {font-family: Verdana; font-size: 16em;}
```
짧은 법칙은 한 줄에 압축되어 쓰여질 수 있습니다.

Long rules should be written over multiple lines:
```
body {
  background-color: lightgrey;
  font-family: "Arial Black", Helvetica, sans-serif;
  font-size: 16em;
  color: black;
}
```
긴 법칙은 여러줄에 쓰여져야 합니다.

Place the opening bracket on the same line as the selector<br>
Use one space before the opening bracket<br>
Use two spaces of indentation<br>
Use semicolon after each property-value pair, including the last<br>
Only use quotes around values if the value contains spaces<br>
Place the closing bracket on a new line, without leading spaces<br>
Avoid lines over 80 characters<br>
여는 괄호를 선택자와 같은 줄에 위치하세요.<br>
여는 괄호 전에 띄어쓰기를 한번 하세요.<br>
들여쓰기로 두번 띄어쓰세요.<br>
마지막을 포함해 각각 속성과값 짝 뒤에는 세미콜론(;)을 사용하세요<br>
값이 빈공간을 포함하고 있을때만 값주위에 따옴표를 사용하세요("값 들")<br>
닫는 괄호는 여백없이 다음줄(새로운줄)에 위치시키세요.<br>
라인에 80개의 글자이상을 피하세요.

Loading JavaScript in HTML
-----
HTML 안에 Javascript 로딩시키기.

Use simple syntax for loading external scripts (the type attribute is not necessary):
```
<script src="myscript.js">
```
외부 스크립트를 로딩하기위해 짧은 문법을 사용하세요.(type 속성은 필요하지않습니다.)

Accessing HTML Elements with JavaScript
----
Javascript와 HTML 요소에 접근

A consequence of using "untidy" HTML styles, might result in JavaScript errors.<br>
These two JavaScript statements will produce different results:<br>
정돈되지않은 HTML 스타일 사용의 결과는 JavaScript 오류를 야기할지도 모릅니다.<br>
이 두개의 JavaScript 표현은 다른 결과를 만들어 낼겁니다.
```
Example
var obj = getElementById("Demo")
var obj = getElementById("demo")
```

Use Lower Case File Names
--------
파일이름들은 소문자를 사용하세요.

Some web servers (Apache, Unix) are case sensitive about file names: "london.jpg" cannot be accessed as "London.jpg".<br>
몇몇 웹 서버들(Apache, Unix)은 파일이름에 대해 까다로운 경우가 있습니다. "london.jpg"는 "London.jpg"로 접근될 수 없습니다.<br> 
Other web servers (Microsoft, IIS) are not case sensitive: "london.jpg" can be accessed as "London.jpg" or "london.jpg".<br>
다른 웹서버들(Microsoft, IIS)은 파일이름에 대해 까다로운 경우가 없습니다. "london.jpg"는 "London.jpg"나 "london.jpg"로 접근이 가능합니다.<br>
If you use a mix of upper and lower case, you have to be extremely consistent.<br>
당신이 대문자와 소문자를 섞어서 사용한다면, 반드시 극도로 일관성이 있어야합니다(한글자라도 틀리면 안됩니다.)<br>
If you move from a case insensitive to a case sensitive server, even small errors will break your web!<br>
만약 당신이 민감하지않은 웹서버에서 민감한 웹서버로 옮긴다면, 엄~청 나게 작은 에러가 당신의 웹을 망칠 수 있습니다.<br> 
To avoid these problems, always use lower case file names.<br>
이러한 문제들을 피하기 위해, 항상 파일이름에는 소문자를 사용하세요.

File Extensions
----
파일 확장자들

HTML files should have a .html or .htm extension.<br>
CSS files should have a .css extension.<br>
JavaScript files should have a .js extension.<br>
HTML 파일들은 반드시 .html 이나 .htm 확장자를 가져야합니다.<br>
css 파일들은 .css 확장자를 가져야합니다.<br>
JavaScript파일은 .js 확장자를 가져야합니다.


Differences Between .htm and .html
----
.htm 과 .html 사이에 차이점

There is no difference between the .htm and .html extensions. <br>
Both will be treated as HTML by any web browser or web server.<br>
.html과 .html 사이에는 차이점이 없습니다.<br>
둘다 어느 웹 브라우저나 웹 서버에 의해 HTML로 대접되어집니다. <br>

The differences are cultural:
.htm "smells" of early DOS systems where the system limited the extensions to 3 characters.<br>
차이점은 문화적입니다.
.html은 3개의 확장자로 제한된 초기의 도즈시스템에 가깝습니다.<br>
.html "smells" of Unix operating systems that did not have this limitation.<br>
.html은 이런 제한이 없는 Unix operating system에 가깝습니다. 


Technical Differences
-----
기술적인 차이점들

When a URL does not specify a filename (like http://www.w3schools.com/css/), the server returns a default filename. Common default filenames are index.html, index.htm, default.html, and default.htm.<br>
If your server is configured only with "index.html" as default filename, your file must be named "index.html", not "index.htm."<br>
URL이 파일명으로 명시되지 않았을때, 서버는 파일명으로 default를 반환합니다.<br>
보통 default 파일명은 index.html, index.htm , default.html, default.htm 입니다.<br>
만약, 당신의 서버가 보통 기본파일명이 "index.html" 으로만 설정된다면, 당신의 파일은 index.htm이 아니라 무조건 "index.html"로 명시되어야합니다.<br>

However, servers can be configured with more than one default filename, and normally you can set up as many default filenames as needed.<br>
Anyway, the full extension for HTML files is .html, and there's no reason it should not be used.<br>
하지만, 서버들은 하나보다 더 많은 default 파일명으로 설정될 수 있습니다. 그리고 보통, 당신은 필요에따라 많은 파일명을을 설정할 수 있습니다.<br> 
어쨌든, HTML 파일을 위한 확장자는 .html이고, 사용되어선 안될 이유가 없습니다.(.html을 사용해달라)



참고 URL
------
[HTML5 Style Guide](https://www.w3schools.com/html/html5_syntax.asp)
