---
title: "[Style] 작업 스타일가이드"
date: 2018-12-19 17:00:00 -0400
categories: CSS
tags: Sass Styleguide
---

작업 스타일가이드
=======


특징 및 규칙
-----

1. Sass 사용
1. 모듈화
1. BEM 방법론 기반 
 (단어와 단어사이는 하이픈, 엘리먼트는 더블언더바, import될 파일은 첫 시작을 언더바로 구분)
1. id 선택자 사용 지양


구조도
------

```
base/
  _reset.scss          (초기화)
  _fonts.scss          (폰트) 
components/            (버튼, 모달 등 위젯, 컴포넌트)
  _buttons.scss        (버튼)
  _modal.scss          (모달)
  …                    (기타)
layout/                (사이트의 주요 레이아웃)
  _header.scss         (헤더)
  _footer.scss         (푸터)
  _common.scss         (레이아웃 공통요소)
  …                    (기타)
pages/                 (각페이지)
  _index.scss          (메인)
  …                    (기타)
utils/                 (프로젝트에서 사용되는 모든 Sass 도구와 헬퍼)
  _var.scss            (변수)
  _mixins.scss         (믹스인)
  …                    (기타)
vendor/                (외부 라이브러리와 프레임워크)
  _semantic.css
  …                    (기타)
index.scss(index.css)  (메인 파일) 
```

```
index.scss 의 import 순서

//scss 변수
@import "utils/_var";

//scss mixin
@import "utils/_mixin";

//vendor
@import "vendor/semantic-ui.css";
@import "vendor/jquery-ui-1.12.1.css";

//공통으로 사용되는 폰트와 리셋
@import "../global/base/_font";
@import "../global/base/_reset";

//scss components
@import "components/_button";
@import "components/_checkbox";
@import "components/_tab";
@import "components/_dropdown";
@import "components/_modal";
@import "components/_date-search";
@import "components/_paging";

//공통 부분
//header를 제외한 공통부분
@import "layout/_common";
@import "layout/_header";
@import "layout/_navigation";
@import "layout/_footer";

//각 페이지
//메인1
@import "pages/_index";
//서브페이지1
@import "pages/_sub-name";
```

위 구조도를 완성하기까지 많은 고민이 있었습니다.
코드의 효율과 브라우저 로딩속도를 위해 Sass를 도입했는데, 
파일 확장자를 CSS로 import했을 경우에는 단순히 파일들을 부른다는 점이었습니다.
이는 파일을 2개씩 로딩하는 단점이 있기에 속도면에서 떨어진다고 합니다. 하지만, 모든파일을
SCSS 변환시키기에는 특히 외부 라이브러리와 프레임워크가 부담됐습니다. 현재 구조도 상으로는
한 파일(index.css)만 HTML에 link하는데, 그러려면 외부 라이브러리도 Sass로 처리하는 과정을 거치기 떄문에, 컴파일시 상당한 시간이 소요되기 때문입니다.

그래서 작업할 때에는 css로 import를 하고, 작업이 끝나고 나서는 해당 파일을 scss 형태로
바꾸었습니다. (사실 이부분도 유지보수측면에서 번거롭긴 했습니다^^;)

이 스타일가이드는 더 나은 방법을 고민하고 해서 점진적으로 수정될 예정입니다.


참고 URL
------
[Sass Guide](https://sass-guidelin.es/ko/#sass-)