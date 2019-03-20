---
title: "[HTML5] Semantic Element Article 과 Section"
date: 2019-01-28 15:00:00 -0400
categories: HTML5 웹표준
tags: HTML5 웹표준 Semantic
---

HTML5에서 가장 중요한 것은 무엇일까요?<br>
개인적으로 Semantic Element를 적재적소에 맞게 사용하는 것이라 생각합니다.<br>
사실 Semantic 이라는 의미 자체가 의미론적이라 그 경계가 모호합니다.<br>
W3C에서도 무조건 사용하면 안된다 라고 이야기 하지 않고, 예시를 들어가며
이러하게 쓰는게 맞는 방식이다 라고 권고안을 제시하고 있습니다.
그래서 참 애매한 경우가 많습니다.

특히 오늘 포스팅할 Article 과 Section 이 그러합니다.

Article 과 Section
=======

```
The article element represents a complete, or self-contained, composition in a document,
page, application, or site. This could be a magazine, newspaper, technical or 
scholarly article, an essay or report, a blog or other social media post.

번역) article 요소는 문서, 페이지, 응용 프로그램 또는 사이트의 완전한 또는 자체 포함 된 구성을 나타냅니다. 
이것은 잡지, 신문, 기술 또는 학술 논문, 에세이 또는 보고서, 블로그 또는 기타 소셜 미디어 게시물 일 수 있습니다.
```
위는 HTML 5.2 권고안의 article 정의입니다.
요약하자면, article 은 그부분만 따로 독립적으로 분리해도, 그 자체만으로 완전한 것을 의미합니다.


```
The section element represents a generic section of a document or application. 
A section, in this context, is a thematic grouping of content. 
Each section should be identified, typically by including a heading (h1-h6 element) as a child of the section element.

번역) 섹션 요소는 문서 또는 응용 프로그램의 일반적인 섹션을 나타냅니다. 
이 컨텍스트의 섹션은 주제별로 그룹화 된 콘텐츠입니다. 
각 섹션은 일반적으로 섹션 요소의 하위 항목으로 제목 (h1-h6 요소)을 포함시켜 식별해야합니다.
```

section은 내용과 서로 관계가 있는 경우에 사용되고 그 자체로는 완전하지 않은 것을 의미합니다.


위 사실을 두고, section안에 무조건 article 이 있어야 한다 라고 생각한 적이 있는데
사실은 여러개의 section이 article 로 묶일수도 있고, 여러개의 article 을 section으로 묶을 수 도 있는 것입니다.

``` 
<article class="film_review">
  <header>
    <h2>Jurassic Park</h2>
  </header>
  <section class="main_review">
    <p>Dinos were great!</p>
  </section>
  //각각 리뷰를 묶는역할
  <section class="user_reviews">
    <article class="user_review">
      <p>Way too scary for me.</p>
      <footer>
        <p>
          Posted on <time datetime="2015-05-16 19:00">May 16</time> by Lisa.
        </p>
      </footer>
    </article>
    <article class="user_review">
      <p>I agree, dinos are my favorite.</p>
      <footer>
        <p>
          Posted on <time datetime="2015-05-17 19:00">May 17</time> by Tom.
        </p>
      </footer>
    </article>
  </section>
  <footer>
    <p>
      Posted on <time datetime="2015-05-15 19:00">May 15</time> by Staff.
    </p>
  </footer>
</article>
```

위와 같은 예시를 보면 어떻게 쓰는지 감이 오실 듯 합니다.
독립적으로 사용하는 부분은 article을 각각의 요소들을 하나로 묶을땐 section을 사용하시면 됩니다.
그러나 관계가 있는 요소들을 하나로 묶는데, 이를 독립적으로 사용할땐 어떤 태그를 사용해야할지 좀 애매할때가 있습니다.
그럴때 section만 사용했는데, 이 글을 정리하다보니 section으로 묶고 이를 article 로 묶으면 되지 않나 생각이 됩니다.





참고 URL
------
[HTML 5.2](https://www.w3.org/TR/html52)<br>
[article](https://developer.mozilla.org/ko/docs/Web/HTML/Element/article)
