---
title: "[HTML] \<head> 태그 내부에 사용하는 \<meta> 태그에 대해"
date: 2019-03-24 21:00:00 -0400
categories: HTML 
tags: meta 
---

\<meta> tag (메타 태그)
======

메타 태그는 head 태그 내부에서 사용됩니다.   
주로 문서에 대한 내용, 키워드, 작성자 등 문서에 대한 정보를 담고 있습니다.  
보다 정확한 설명?을 위해, 메타 태그에 대한 문서를 두가지 살펴보겠습니다.  
W3C의 **HTML5: Edition for Web Authors** 와 W3schools의 **HTML meta tag**  입니다.

meta element 에 대한 문서
------

1. W3C The meta element  

The meta element represents various kinds of metadata that cannot be expressed using the title, base, link, style, and script elements.  
메타 요소는 제목, 베이스, 링크, 스타일과 스크립트 요소를 사용해 표현할 수 없는 다양한 종류의 메타데이터를 나타냅니다.  
The meta element can represent document-level metadata with the name attribute, pragma directives with the http-equiv attribute, and the file's character encoding declaration when an HTML document is serialized to string form (e.g. for transmission over the network or for disk storage) with the charset attribute.  
메타 요소는 HTML 요소가 charset 속성과 문자열 형식으로 직렬화 될 때 name 속성, http-equiv 속성이 있는 pragma 지시문 및 파일의 문자 인코딩 선언 (예: 네트워크 또는 디스크 저장 장치를 통한 전송의 경우)을 이용해 문서수준의 메타데이터 나타낼 수 있습니다.  
Exactly one of the name, http-equiv, and charset attributes must be specified.  
name 속성, http-equiv 속성, charset 속성 중 정확히 하나가 지정 되어야 합니다.  
If either name or http-equiv is specified, then the content attribute must also be specified. Otherwise, it must be omitted.  
name 속성 이나 http-equiv 속성이 지정된다면, 콘텐츠 속성 또한 반드시 지정되어야 합니다. 그렇지 않으면 생략되어야합니다.  
The charset attribute specifies the character encoding used by the document. This is a character encoding declaration. 
charset 속성은 문서에 사용되는 문자 인코딩을 지정합니다. 이 것이 charset 인코딩 선언 입니다.  
If the attribute is present in an XML document, its value must be an ASCII case-insensitive match for the string "UTF-8" (and the document is therefore forced to use UTF-8 as its encoding).  
속성이 XML 문서로 나타나면,  그 값은 “UTF-8” 문자열에 대한  ASCII 대/소문자 구분 없는 일치해야 합니다.(따라서 문서는 UTF-8을 인코딩으로 사용해야 합니다).  

Note: The charset attribute on the meta element has no effect in XML documents, and is only allowed in order to facilitate migration to and from XHTML.  
메타 요소안에 charset 속성은 XML 문서에 영향을 미치지 않고, 오직 XHTML로의 마이그레이션을 용이하기 위해서만  허용됩니다.   


There must not be more than one meta element with a charset attribute per document.  
문서당 charset 속성을 가진 메타 요소가 하나 이상 있어선 안됩니다.  
The content attribute gives the value of the document metadata or pragma directive when the element is used for those purposes.   
콘텐츠 속성은 요소가 그러한 목적으로 이용되었을 때 문서 메타데이터의 값이나 pragma 지시문의 값을 제공합니다.   
The allowed values depend on the exact context, as described in subsequent sections of this specification.  
허용된 값은  이 규격의 후속 절에서 설명한 정확한 문맥에 의존합니다.   
If a meta element has a name attribute, it sets document metadata.   
메타요소가 name 속성을 가지게 되면,  문서 메타데이터를 설정합니다.  
Document metadata is expressed in terms of name/value pairs, the name attribute on the meta element giving the name, and the content attribute on the same element giving the value.   
문서 메타데이터는 name 요소를 부여하는 메타 요소의 name 속성과 value를 부여하는 같은 요소의 콘텐츠 속성의 name/value 쌍의 용어로 표현됩니다.   
The name specifies what aspect of metadata is being set; valid names and the meaning of their values are described in the following sections.   
name은 설정중인 메타데이터의 측면을 지정합니다. 유효한 name과 해당 값의 의미는 다음 부분에서 설명 됩니다.  
If a meta element has no content attribute, then the value part of the metadata name/value pair is the empty string.  
메타 요소가 콘텐츠 속성을 가지고 있지 않다면, 메타데이터  name/value 쌍의 value 부분은 빈 문자열 입니다.  
The name and content IDL attributes must reflect the respective content attributes of the same name. The IDL attribute httpEquiv must reflect the content attribute http-equiv.  
name과 콘텐츠 IDL 속성은 같은 name의 콘텐츠 속성을 반드시 반영해야 합니다. IDL 속성 httpEquiv은 콘텐츠 속성 http-equiv를 반드시 반영해야 합니다.  


**4.2.5.1 Standard metadata names**  
4.2.5.1 메타데이터 names 표준화  

This specification defines a few names for the name attribute of the meta element.  
이 규격은 메타 요소의 name 속성에 대한 몇 몇 name들을 정의합니다.    
Names are case-insensitive.  
name들은 대소문자를 구분하지 않습니다.  


1. application-name  
The value must be a short free-form string giving the name of the Web application that the page represents.  
값은 페이지가 나타내는 웹 애플리케이션의 이름을 제공하는 짧은 자유 양식 문자열이어야 합니다.  
If the page is not a Web application, the application-name metadata name must not be used.   
페이지가 웹 애플리케이션이 아니라면, application-name 메타데이터의 name을 사용해서는 안됩니다.  
There must not be more than one meta element with its name attribute set to the value application-name per document.  
Name 속성이 문서 당 application-name값으로 설정된 메타요소가 둘 이상 있어서는 안됩니다.  

2. author  
작성자
The value must be a free-form string giving the name of one of the page's authors.  
값은 페이지의 저자 중 하나의 이름을 가지고 있는 자유 양식 문자열 이어야 합니다.   

3. description  
설명  
The value must be a free-form string that describes the page.   
값은 페이지가 설명된 자유 양식 문자열 이어야 합니다.  
The value must be appropriate for use in a directory of pages, e.g. in a search engine.   
값은 페이지 디렉토리에 사용하기에 적합해야합니다 (예: 검색엔진에서)   
There must not be more than one meta element with its name attribute set to the value description per document.  
name 속성이 문서당 설명값이 설정된 하나 이상의 메타 요소가 있어서는 안됩니다.  

4. generator  
생성자  
The value must be a free-form string that identifies one of the software packages used to generate the document.   
값은 문서를 생성하는데 사용된 소프트웨어 패키지 중 하나를 식별하는 자유 양식 문자열이어야 합니다.  
This value must not be used on hand-authored pages.  
이 값은 직접 작성한 페이지에서는 사용되서는 안됩니다.  


5. keywords  
The value must be a set of comma-separated tokens, each of which is a keyword relevant to the page.  
이 값은 반드시 구분된 토큰 집합이어야 하며 각 토큰은 페이지와 관련된 키워드입니다.   
Note: Many search engines do not consider such keywords, because this feature has historically been used unreliably and even misleadingly as a way to spam search engine results in a way that is not helpful for users.  
많은 검색 엔진들은 키워드와 같은 것을 고려하지 않습니다. 왜냐하면 이는 역사적으로 신뢰할 수 없게 사용자에게 도움이 되지 않는 방식으로 검색 엔진 결과를 스팸하는 방법으로 오해하기 쉽기 때문입니다.  


**4.2.5.2 Other metadata names**  
4.2.5.2. 다른 메타데이터 name들  

Extensions to the predefined set of metadata names may be registered in the WHATWG Wiki MetaExtensions page. [WHATWGWIKI]  
미리 정의된 메타데이터 name들에  대한 확장은 WHATWG Wiki MetaExtensions 페이지에 등록할 수 있습니다.  
Anyone is free to edit the WHATWG Wiki MetaExtensions page at any time to add a type. These new names must be specified with the following information:  
언제든 누구나 WHATWG Wiki MetaExtensions 페이지를 편집해 유형을 추가 할 수 있습니다. 새 name들은 다음 정보와 함께 지정되어야 합니다.  

1. Keyword  
The actual name being defined. The name should not be confusingly similar to any other defined name (e.g. differing only in case).  
실제 name이 정의됩니다. name은 다른 정의된 name과 혼동스럽게 유사해서는 안됩니다. (경우에 따라 다른이름)   

2. Brief description  
간결한 설명  
A short non-normative description of what the metadata name's meaning is, including the format the value is required to be in.  
값을 입력해야 하는 형식을 포함해 메타데이터 이름의 의미에 대한 짧은 비표준 설명 입니다.   

3. Specification  
A link to a more detailed description of the metadata name's semantics and requirements. It could be another page on the Wiki, or a link to an external page.  
메타데이터 이름의 의미 및 요구 사항에 대한 자세한 설명에 대한 링크입니다. 그것은 Wiki의 다른 페이지 이거나, 외부 페이지의 링크일 수 있습니다.    

4. Synonyms
동의어
A list of other names that have exactly the same processing requirements. Authors should not use the names defined to be synonyms, they are only intended to allow user agents to support legacy content. Anyone may remove synonyms that are not used in practice; only names that need to be processed as synonyms for compatibility with legacy content are to be registered in this way.  
정확히 동일한 처리 요구 사항을 가진 다른 name의 목록. 저자는 동의어로 정의된 name을 사용해선 안되고, 사용자 에이전트가 기존 콘텐츠를 지원할 수 있도록 하기 위한 용도로만 사용됩니다. 누구나 실제로 사용되지 않는 동의어를 제거할 수 있습니다. 오직 legacy 컨텐츠와의 호환성을 위해 동의어로 처리해야될 name만이 같은 방식으로 등록됩니다.   

5. Status  
상태  
One of the following:  
다음중 하나  
    1. Proposed  
    제안된  
The name has not received wide peer review and approval. Someone has proposed it and is, or soon will be, using it.  
name은 광범위한 peer 심사 및 승인을 받지 못했습니다. 누군가 제안 했고, 사용하고 있거나 곧 사용할 것입니다.  

    2. Ratified  
    등급지정  
The name has received wide peer review and approval. It has a specification that unambiguously defines how to handle pages that use the name, including when they use it in incorrect ways.  
Name은 광범위한 peer 심사 및 승인을 받았습니다. 이것은 name을 사용하는 페이지를 잘못된 방법으로 사용하는 경우를 포함해 페이지를 처리하는 방법을 명확하게 정의하는 규격을 가집니다.     

    3. Discontinued  
    중단됨  
The metadata name has received wide peer review and it has been found wanting. Existing pages are using this metadata name, but new pages should avoid it. The "brief description" and "specification" entries will give details of what authors should use instead, if anything.  
메타데이터 name은 광범위한 peer 심사를 받았습니다. 그리고 원하는 것으로 나타났습니다. 현재 페이지는 이것의 메타데이터 name으로 사용되지만, 새로운 페이지는 이를 피해야합니다. “간결한 설명” 과 “규격” 항목은 저자가 무엇을 사용해야하는지 상세사항을 줍니다.  

If a metadata name is found to be redundant with existing values, it should be removed and listed as a synonym for the existing value.  
메타데이터 name이 현재 값과 중복된 것이 발견되면, 제거되어야 하고, 현재 값의 동의어로 나열되어야 합니다.  

If a metadata name is registered in the "proposed" state for a period of a month or more without being used or specified, then it may be removed from the registry.  
메타데이터 name이 사용되거나 지정되지 않고 한달이나 그 이상의 기간 동안 “제안된” 상태로 등록이 된다면, 레지스터로부터 제거 될 수있습니다.  

If a metadata name is added with the "proposed" status and found to be redundant with existing values, it should be removed and listed as a synonym for the existing value. If a metadata name is added with the "proposed" status and found to be harmful, then it should be changed to "discontinued" status.  
메타데이터 name이 “제안된”에 추가되고, 현재 값과 중복된 것이 발견되면, 제거되어야하고, 현재 값의 동의어로 나열되어야 합니다. 메타데이터 name이  “제안된”상태에 추가되고, 위험이 발견된다면, “중단됨” 상태로 변경되어야 합니다.  

Anyone can change the status at any time, but should only do so in accordance with the definitions above.  
누구나 언제든 상태를 변경할 수 있지만, 오직 위의 정의에 따라 변경 해야 합니다.  

Metadata names whose values are to be URLs must not be proposed or accepted. Links must be represented using the link element, not the meta element.  
값이 URL이 될 메타데이터 name은 제안 되거나 승인되어서는 안됩니다. 링크는 meta 요소가 아닌 link 요소를 사용해 나타내야 합니다.  

---- 


W3C 의 공식 문서는 아무래도 딱딱하고 용어도 어렵지만 전체적으로 메타태그의 역할과 사용법에 대해 자세히 설명하고 있습니다.


-----

2\. W3schools HTML meta tag  

**Definition and Usage**  
정의와 사용   

Metadata is data (information) about data.  
메타데이터는 데이터에 관한 데이터(정보)입니다.  
The \<meta> tag provides metadata about the HTML document.   
메타 태그는 HTML 문서에 대한 메타데이터를 제공합니다.  
Metadata will not be displayed on the page, but will be machine parsable.  
메타데이터는 페이지에 보이지 않지만 구문 분석이 가능합니다.  
Meta elements are typically used to specify page description, keywords, author of the document, last modified, and other metadata.  
메타 요소는 전통적으로 설명,키워드, 문서의 저작자, 마지막 수정, 다른 메타데이터를 지정하는데 사용됩니다.  
The metadata can be used by browsers (how to display content or reload page), search engines (keywords), or other web services.  
메타데이터는 브라우저들(페이지를 새로 로드하거나 콘텐츠를 보여주는 방법)과 검색 엔진, 다른 웹 서비스에 의해 사용될 수 있습니다.  
HTML5 introduced a method to let web designers take control over the viewport (the user's visible area of a web page), through the \<meta>  tag (See "Setting The Viewport" example below).  
HTML5는 웹디자이너가 메타태그를 통해 뷰포트(웹 페이지의 사용자가 볼 수 있는 영역)를 제어할 수 있도록 하는 방법을 도입했습니다(아래"뷰포트 설정" 예 참조)  

*뷰포트 설정 예는 아래 메타태그의 속성을 이용해 브라우저에서 페이지의 치수나 배율을 제어할 수 있다는 것입니다.
width=device-width는 장치의 화면 너비를 따르도록 페이지 폭을 설정하는 것이며, initial-scale=1.0은 페이지를 처음 로드할 경우 초기의 확대,축소 정도(1이 기본)를 설정한다는 의미 입니다.
```
<meta name="viewport" content="width=device-width, initial-scale=1.0">
```

----

위 내용으로 메타 태그에 대한 설명은 어느정도 되셨을 것이라 생각합니다. 
앞서 말씀드렸지만 메타 태그의 종류와 속성은 다양하기 때문에 제가 주로 사용하는 메타태그 위주로 설명을 드리겠습니다.

```
<head>
  <title>Yang Eun Jin's Blog</title>
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <meta http-equiv="X-UA-Compatible" content="IE=edge">
  <meta name="theme-color" content="#6B58A7">
  <link href="/assets/images/global/favi.ico" rel="shortcut icon">
  <meta name="naver-site-verification" content="5a3760839632bf2accaa65c28ee953451801fbbc">
  <meta name="description" content="안녕하세요. jinnny의 블로그에 와주셔서 감사합니다.">
  <meta name="keywords" content="jinnny, jinnny블로그">
  <meta name="author" content="jinnny">
  <meta property="og:type" content="website">
  <meta property="og:title" content="Yang Eun Jin's Blog">
  <meta property="og:description" content="안녕하세요. jinnny의 블로그에 와주셔서 감사합니다.">
  <meta property="og:image" content="https://jinnny.github.io/blog/logo.svg">
  <meta property="og:url" content="https://jinnny.github.io/blog/">
  <link rel="canonical" href="https://jinnny.github.io/blog/">
  <meta name="twitter:card" content="안녕하세요. jinnny의 블로그에 와주셔서 감사합니다.">
  <meta name="twitter:title" content="Yang Eun Jin's Blog">
  <meta name="twitter:description" content="안녕하세요. jinnny의 블로그에 와주셔서 감사합니다.">
  <meta name="twitter:image" content="https://jinnny.github.io/blog/logo.svg">
  <meta name="twitter:domain" content="https://jinnny.github.io/blog/g">
</head>
```

**1. <span style="color:#f44336">\<meta charset="UTF-8"\></span>**  
  문서의 문자 코드 셋을 지정합니다. (어떤 언어로 되어있는 지에 대한 지정)  
  UTF-8은 전세계의 거의 모든 문자와 기호를 포함하고 HTML5의 기본문자 인코딩이기도 합니다.  
  *euc-kr는 영어 기반의 ASCII 방식을 확장해 한글을 사용할 수 있게 만든 방식이라, 과거에 보편적으로 사용했었습니다.  

**2. \<title>Yang Eun Jin's Blog\</title>**  
  문서의 제목을 지정합니다.  
  제목은 유니크한 것을 권장하고 그 길이가 너무 길어선 안됩니다.(지양)  

**3. \<meta name="viewport" content="width=device-width, initial-scale=1.0">**  
  뷰포트를 설정합니다.   
  위에 설명했듯이 width=device-width는 장치의 화면 너비를 따르도록 페이지 폭을 설정하는 것이며, 
  initial-scale=1.0은 페이지를 처음 로드할 경우 초기의 확대,축소 정도(1이 기본)를 설정한다는 의미 입니다.

  **4. \<meta http-equiv="X-UA-Compatible" content="IE=edge">**  
  호환성 보기 대신 사용되는 것으로, 렌더링 모드를 적용 설정합니다.  
  content="IE=edge"는 IE브라우저에서 가장 최신 표준 모드를 렌더링 하도록 설정하는 것입니다. 주로 이 속성을 사용합니다.

  **5. \<meta name="theme-color" content="#6B58A7">**  
  브라우저 요소의 색상을 설정합니다. 주소바의 영역 색상을 변경해 줍니다.  
  Android용 Chrome, 내장인터넷 등에서 적용이 가능하며 iOS의 경우는 작동하지 않습니다.
  
 **6. \<meta name="naver-site-verification" content="">**  
 네이버에 사이트 등록을 할 경우 부여받는 키 입니다.
 
**7. \<meta name="description" content="안녕하세요. jinnny의 블로그에 와주셔서 감사합니다.">**  
사이트에 대한 설명을 지정하는 것입니다. 
사이트를 요약하시면 되며 이 역시 너무 긴 문장을 사용하는 것은 지양해야 합니다.

**8.  \<meta name="keywords" content="jinnny, jinnny블로그">**  
사이트에 대한 키워드를 지정하는 것입니다.  
검색엔진에서 순위를 결정하는데 중요한 역할을 하는 것은 아니지만 중요한 주제를 함축적으로 잘표현해야합니다.

**9. \<meta name="author" content="jinnny">**  
사이트를 제작한 저자를 지정하는 것으로 자유 양식 문자열이면 큰 제약이 없습니다.

 **10. \<meta property="og:type" content="website">  
  \<meta property="og:title" content="STARPAY">  
 \<meta property="og:description" content="안녕하세요. jinnny의 블로그에 와주셔서 감사합니다.">  
  \<meta property="og:image" content="https://jinnny.github.io/blog/logo.svg">  
  \<meta property="og:url" content="https://jinnny.github.io/blog/">**  
 오픈그래프 태그로, SNS의 대부분에서 사이트가 공유될 때 우선적으로 활용됩니다.
 종류는 위와 같습니다.
 
**11.  \<meta name="twitter:card" content="안녕하세요. jinnny의 블로그에 와주셔서 감사합니다.">  
  \<meta name="twitter:title" content="Yang Eun Jin's Blog">  
  \<meta name="twitter:description" content="안녕하세요. jinnny의 블로그에 와주셔서 감사합니다.">  
  \<meta name="twitter:image" content="https://jinnny.github.io/blog/logo.svg">  
  \<meta name="twitter:domain" content="https://jinnny.github.io/blog/g">**  
  오픈그래프와 비슷하긴 하지만..위 코드는 트위터에서 공유될 콘텐츠의 정보를 설정하는 것입니다.   
  
  * 사실 트위터에서는 위의 코드가 없는 경우 오픈그래프 만으로도 수용이 가능합니다.  (twitter:card 제외)


참고 URL
------
[W3C The meta element](https://www.w3.org/TR/2011/WD-html5-author-20110809/the-meta-element.html)  
[HTML meta tag](https://www.w3schools.com/tags/tag_meta.asp)  
