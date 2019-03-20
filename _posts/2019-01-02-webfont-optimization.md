---
title: "[CSS] 웹 폰트와 최적화"
date: 2019-01-02 13:00:00 -0400
categories: CSS
tags: CSS 웹폰트 webfont 최적화
---

webfont 웹 폰트?
=============

이 포스팅에서 아래 내용은 
[NAVER D2- 웹 폰트 사용과 최적화](https://d2.naver.com/helloworld/4969726?fbclid=IwAR0wq0PQnXnLHdIqpZrM8p0cxaIGQ9tP7GB7PlfzFh3NqE0UjtSq32PTGoQ) 을 기반으로
검토후 상당부분을 적용해본 경험을 바탕으로 작성 하였습니다. 
 

지난 포스팅에서 웹 폰트를 주제로 이야기를 했었습니다.
지난번에는 경량화에 대한 이야기를 배제 했었는데..
최적화와 경량화는 필수불가결한 사항이라 생각되어 그에 대해 포스팅 하고
그 외에도 웹 폰트를 이용한 최적화에 대해 더 이야기 해보고자 합니다.

경량화
----

일단, 경량화는 말 그대로 가볍게 하는 것을 의미합니다.
최근 제가 작업했던 일들은 다국어가 필수 였기 때문에 디자이너와 상의해 Noto San CJK 폰트를 사용하기로 했습니다.
그러다보니 디자인 공수는 적었지만, 위의 폰트는 한 파일당 용량이 무려 16MB(otf 기준) 였습니다. 
용량의 크기가 크다보니 자연스레 브라우저 로딩 속도가 느려졌고 이는 불편함으로 이어졌습니다.
CJK 폰트는 4개의 언어(JP, KR, SC, TC)를 포함하고있고, 이중 용량에 상당한 양을 차지하고 있는 것이 중국어임을 생각해 
언어별로(Noto Sans KR, Noto Sans JP 등) 분류해, 각각 임포트 하는 방식을 생각했습니다. ( 같은 페이지에 중국어,일본어,한국어를 보여줘야하는 구조가 아니었기때문) 

하지만, 거기에서도 용량이 1MB(Noto Sans KR의 경우)를 차지했습니다. 고대 한글뿐 아니라 현대 한글에서 사용하지 않는 글자들도 들어있었기 때문이죠.
그래서 KSX1001 + 추가한글 + 현대한글의낱자 + Basic latin 을 기준으로 경량화 폰트를 제작하게 되었습니다.

이 과정에서는 [NONRIA '웹폰트로 사용하기 위한 서브셋 지정'](https://nonria.com/post/96/)을 상당부분 참고했습니다.

[여기](https://github.com/jinnny/publish_source/tree/master/webfont/NotoSansKR/fonts)를 클릭하시면, 위를 바탕으로 제작한 Noto Sans KR 경량화 웹 폰트를 다운 받으실 수 있습니다.

WOFF 2.0
---

WOFF형식은 WOFF2 와 WOFF가 있는데, 이 둘의 차이는 용량과 IE의 지원여부 입니다.

아래 그림은
Noto Sans Regular를 변환한 것입니다.

![image](/blog/assets/images/woff2.png)

보시면 WOFF2가 용량이 적은 것을 알 수가 있습니다.
하지만 WOFF2의 경우 IE는 지원을 하지 않고, WOFF의 경우에는 IE9부터 지원을 합니다.
그러니 IE의 경우만 WOFF나 EOT를 사용하고, 나머지 브라우저에서는 WOFF2 형식을 사용하면
최적화가 가능합니다.

아래는 이같은 우선순위를 바탕으로 작성한 @font-face 입니다.

```
@font-face {
  font-family: 'Noto Sans';
  font-weight: 200;
  src: url('../fonts/NotoSansKR-Thin.eot');
  src: url('../fonts/NotoSansKR-Thin.eot?#iefix') format('embedded-opentype'),
  url('../fonts/NotoSansKR-Thin.woff2') format('woff2'),
  url('../fonts/NotoSansKR-Thin.woff') format('woff'),
  url('../fonts/NotoSansKR-Thin.otf') format('opentype');
}
```

위를 선언하고 확인해보면, IE(9이상)는 WOFF, 타 브라우저는 WOFF2를 불러오는 사실을 확인하실 수 있습니다.


렌더링 처리 방식
------

브라우저의 렌더링 방식은 FOUT 방식(Flash Of Unstyled Text) 과 FOIT 방식(Flash Of Invisible Text)으로 나뉩니다.
많은 분들이 아시는 부분이겠지만 웹 폰트를 적용할때 번쩍거리는 현상이 발생하는데, 이를 바탕으로 처리 방식이 결정됩니다.
웹 폰트가 적용될때까지 글자자체가 보이지 않다가 웹 폰트가 적용되면 번쩍이는 FOIT 방식과 웹 폰트가 적용되지 않은 Unstyled 상태에서 웹 폰트가 적용되면서 번쩍이는 FOUT 방식이 있습니다.

IE는 FOUT 처리방식을 이용하고, IE를 제외한 최신 브라우저는 FOIT 방식으로 렌더링이 처리 됩니다.
FOUT 방식은 웹 폰트 랜딩 전까지 글자 자체가 보이기는 하지만, 레이아웃이 틀어지거나 레이아웃이 변경되는 모습이 보일 수 있고,
FOIT 방식은 웹 폰트가 랜딩되기 전까지 글자 자체가 보이지 않아 해석의 여지가 발생할 수 있습니다.

NAVER도 그랬지만 저는 글의 본 목적을 해칠 수 있는 FOIT 보다는 FOUT 방식을 적용하기로 했습니다.

IE를 제외한 최신 브라우저는 FOIT 방식으로 처리하기때문에, 별도로 FOUT 방식이 적용되도록 처리를 해줘야합니다.

간단하지만, 최적화 되는 CSS의 font-display를 사용해 처리해보겠습니다.

이 속성은 auto, block, swap, fallback, optional의 옵션을 가지고 있습니다.
auto 는 말그대로 브라우저의 기본동작, block은 웹 폰트가 적용될때까지 글이 보이지 않는 동작(FOIT 방식), swap은 Unstyled 상태의 글이 보였다가 웹 폰트가
적용되면 적용되는(FOUT 방식), fallback은 100ms 동안 글이 보이지 않다가, 그 후에 글을 노출하는 옵션으로 해당 시간안에 웹 폰트가 적용되면 웹 폰트 적용상태로 보이는데 그 시간안에 웹 폰트가 업로드되지 않으면 웹 폰트가 다 업로드 되더라도 적용 되지 않습니다.
optional옵션은 100ms 동안 글이 보이지 않고, 그 이후에 Unstyled 폰트를 보여줍니다. 웹 폰트를 다운하지만 브라우저가 네트워크 상태를 파악해 웹 폰트로 전환할지 말지 여부를 판단해 적용한다는 특징을 가지고 있습니다.

여기서 이 속성을 쓰는것은 FOUT방식을 적용시키기 위함이니, swap 옵션을 사용해야 합니다.
물론 font-display 속성이 IE에서 지원하지 않는 브라우저의 제한이 있지만, 
저희가 사용하려는 swap옵션은 IE의 기본 처리방식인 FOUT 방식이기때문에 문제가 없습니다.

![image](/blog/assets/images/font_display.png)


당연하겠지만, 폰트의 용량이나 네트워크 속도로 인해 기존 레이아웃이 틀어지는 경우도 있을 것입니다.
사용하기에는 문제가 없지만 UI 측면에서 문제가 있기에...D2 는 아래의 방법을 제안합니다.


Font Style Matcher로 폰트 간 차이 줄이기
-------

[Font style matcher](https://sangziii.github.io/fontStyleMatcher/) 는 사용하기가 간단합니다.
먼저, fallback 폰트 명을 지정해주고 적용하고자 하는 웹 폰트를 선택한 뒤
슬라이더를 조절해 두 폰트 간의 차이를 줄여주시면 됩니다.
 
저는 위 방법을 몰랐기에 홈페이지가 모두 만들어진 후 적용을 해봤습니다.

그런데 이 경우에는, 기존에 적용되고 있는 line-height 값이나, letter-spacing 값을 
적용된 곳마다 수정해야하는 점이 있습니다. 
또, bootstrap 이나 semantic UI 등의 프레임워크를 사용했을 경우 또한 속성이 문제가 되었습니다.
(h 태그나 p 태그 등의 line-height 값이 적용되었을때가 문제였습니다.)

그래서 위 방법은 홈페이지를 처음 만드실 때 적용하면 아주 큰 효과를 볼 수 있을 것 같습니다.
다른 방법을 적용해보았습니다. 

preload 옵션
----

```
<link rel="preload" href="/assets/fonts/NotoSansKR-Light.woff" as="font" type="font/woff" crossorigin="anonymous">
```

link 태그에 preload 속성을 사용하면, 해당 소스가 먼저 로딩됩니다. 
그렇지만 이 속성은 IE, Firefox 는 지원하지 않는 단점이 있습니다.

![image](/blog/assets/images/css_preload.png)

그래도 이 방법이 현재 작동되고 있는 홈페이지에 적용하기 참 좋은 것 같았습니다.



참고 URL
-------
[NAVER D2- 웹 폰트 사용과 최적화](https://d2.naver.com/helloworld/4969726?fbclid=IwAR0wq0PQnXnLHdIqpZrM8p0cxaIGQ9tP7GB7PlfzFh3NqE0UjtSq32PTGoQ)

[NONRIA '웹폰트로 사용하기 위한 서브셋 지정'](https://nonria.com/post/96/)
