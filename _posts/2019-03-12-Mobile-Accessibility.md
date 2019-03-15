---
title: "[HTML5] Mobile Accessibility: How WCAG 2.0 and Other W3C/WAI Guidelines Apply to Mobile 번역하기"
date: 2019-03-12 21:30:00 -0400
categories: HTML5
tags: Mobile HTML5 Accessibility 접근성 모바일접근성
---

Mobile Accessibility: How WCAG 2.0 and Other W3C/WAI Guidelines Apply to Mobile
=======
모바일 접근성: WCAG 2.0 및 기타 W3C / WAI 지침을 모바일에 적용하는 방법

작업에 앞서..
---

접근성, 표준에 대한 Guide 가 여러곳에 쓰여있지만 
제일 좋은 방법은 W3C 문서를 보는 것이라고 생각합니다.

원문이 영어고 그 길이도 무시못할 정도로 길기 때문에 쉽지는않지만
W3C Guide 에 대한 한글 번역도 존재하기때문에 그것을 참고하는 방법도 있습니다.

모바일 접근성에도 여러 한국어 번역문서가 있긴 했지만... 
주관기관이 다 다르고 애매한 부분이 존재해 직접 번역해서 읽어보는건 어떨까하며 작업을 시작하게 되었습니다.

많은 내용이 있지만, 필요한 부분만 번역하도록 하겠습니다. 번역하다보니 거의 대부분이긴 합니다.


---

1.Introduction
---
This section is non-normative.  
이 부분은 비규범적입니다.

This document provides informative guidance (but does not set requirements) with regard to interpreting 
and applying Web Content Accessibility Guidelines (WCAG) 2.0 [WCAG20] to web and non-web mobile content and applications.  
본 문서는 웹 및 비 웹 모바일 콘텐츠 및 응용 프로그램에 대한 Web Content Accessibility Guideline(WCAG) 2.0 [WCAG20]의 해석 및 적용에 관한 유익한 지침(그러나 요구사항은 설정하지 않음)을 제공합니다.  
While the World Wide Web Consortium (W3C)'s W3C Web Accessibility Initiative (WAI) is primarily concerned with web technologies, guidance for web-based technologies is also often relevant to non-web technologies.   
W3C(World Wide Web Consortium)의 W3C Web Accessibility Initiative(WAI)는 주로 웹 기술에 관련된 반면, 웹 기반 기술에 대한 지침은 비 웹 기술과 관련이 있는 경우가 많습니다.  
The W3C-WAI has published the Note Guidance on Applying WCAG 2.0 to Non-Web Information and Communications Technologies (WCAG2ICT) to provide authoritative guidance on how to apply WCAG to non-web technologies such as mobile native applications. The current document is a mobile-specific extension of this effort.  
W3C-WAI는 비 웹정보통신기술(WCAG2ICT)에 WCAG 2.0 적용에 관한 참고지침을 발행해 모바일 네이티브 애플리케이션 등 비웹 기술에 WCAG를 적용하는 방법에 관한 권위 있는 지침을 제공하고 있습니다. 현재 문서는 이러한 노력의 모바일 전용 확장입니다.   
W3C Mobile Web Initiative Recommendations and Notes pertaining to mobile technologies also include the Mobile Web Best Practices and the Mobile Web Application Best Practices.   
W3C 모바일 웹 이니셔티브 권장사항 및 모바일 기술에 관한 참고사항에는 모바일 웹 모범 사례와 모바일 웹 애플리케이션 모범 사례도 포함됩니다.  
These offer general guidance to developers on how to create content and applications that work well on mobile devices.  
이들은 개발자들에게 모바일 기기에서 잘 작동하는 콘텐츠와 애플리케이션을 만드는 방법에 대한 일반적인 지침을 제공합니다.  
The current document is focused on the accessibility of mobile web and applications to people with disabilities and is not intended to supplant any other W3C work.  
현재의 문서는 장애가있는 사람들에게 모바일 웹과 애플리케이션의 접근성에 중점을 두고 있으며 다른 W3C 작업을 대체하려는 의도는 없습니다.  


**1.1 WCAG 2.0 and Mobile Content/Applications**  
WCAG 2.0와 모바일 컨텐츠/애플리케이션  

"Mobile" is a generic term for a broad range of wireless devices and applications that are easy to carry and use in a wide variety of settings, including outdoors.   
모바일은 옥외를 포함한 다양한 환경에서 휴대하고 사용하기 쉬운 다양한 무선 장치와 애플리케이션의 총칭한 것 입니다.   
Mobile devices range from small handheld devices (e.g. feature phones, smartphones) to somewhat larger tablet devices.   
모바일 기기는 소형 기기 장치(예: 피처폰, 스마트폰들)에서 다소 큰 태블릿 장치에 이르기까지 다양합니다.  
The term also applies to "wearables" such as "smart"-glasses, "smart"-watches and fitness bands, 
and is relevant to other small computing devices such as those embedded into car dashboards, airplane seatbacks, and household appliances.  
그 범주는 또한  '스마트' 안경, '스마트'와치 및 피트니스 밴드 와 같은 '착용감이 좋은'것에도 적용되고, 자동차 대시보드, 비행기 좌석 등받이, 가전제품에 내장된 것과 같은 다른 소형 컴퓨터 장치에도 적용됩니다.   

While mobile is viewed by some as separate from "desktop/laptop", and thus perhaps requiring new and different accessibility guidance, in reality there is no absolute divide between the categories. For example:  
모바일은 '데스크탑/랩탑'과 별개로 간주되어 새롭고 다른 접근성 지침이 필요할 수 있지만, 실제로는 범주 간에 절대적인 차이는 없습니다. 예를 들면 다음과 같습니다.  

- many desktop/laptop devices now include touchscreen gesture control,  
많은 데스크탑/랩탑 장치들은 터치스크린 제스처 컨트롤을 포함합니다.  

- many mobile devices can be connected to an external keyboard and mouse,  
많은 모바일 장치들은 외부 키보드와 마우스와 연결 될 수 있습니다.  

- web pages utilizing responsive design can transition into a "mobile" screen size even on a desktop/laptop, and  
반응형 디자인을 활용한 웹 페이지들은 심지어 데스크탑/랩탑 에서도 '모바일' 화면 크기로 전환될 수 있습니다. 그리고  

- mobile operating systems have been used for laptop devices.  
모바일 운영체제는 랩탑 장치에 사용해왔습니다.   

Furthermore, the vast majority of user interface patterns from desktop/laptop systems (e.g. text, hyperlinks, tables, buttons, pop-up menus, etc.) are equally applicable to mobile.   
더불어, 데스크탑/랩탑 시스템(예: 텍스트, 하이퍼링크, 테이블, 버튼, 팝업 메뉴 등)의 사용자 인터페이스 패턴의 대부분이 모바일에도 동일하게 적용됩니다.   
Therefore, it's not surprising that a large number of existing WCAG 2.0 techniques can be applied to mobile content and applications (see Appendix A).   
따라서 기존의 WCAG 2.0 기법이 모바일 콘텐츠와 애플리케이션에 대거 적용될 수 있다는 것은 놀라운 일이 아닙니다(부록 A 참조).   
Overall, WCAG 2.0 is highly relevant to both web and non-web mobile content and applications.  
전체적으로 WCAG 2.0은 웹 및 비 웹 모바일 콘텐츠와 응용 프로그램 모두에 매우 관련성이 높습니다.  

That said, mobile devices do present a mix of accessibility issues that are different from the typical desktop/laptop.   
이말은, 모바일 기기는 일반적인 데스크탑/랩탑과는 다른 접근성 문제를 혼합하여 제시합니다.  
The "Discussion of Mobile-Related Issues" section, below, explains how these issues can be addressed in the context of WCAG 2.0 as it exists or with additional best practices.   
아래의 "모바일 관련 이슈의 논의" 부분에서는 이러한 이슈가 존재하는 경우 또는 추가적인 모범 사례와 함께 WCAG 2.0 에서 어떻게 다루어질 수 있는지 설명합니다.  
All the advice in this document can be applied to mobile web sites, mobile web applications, and hybrid web-native applications.   
이 문서안의 모든 조언은 모바일 웹 사이트, 모바일 웹 애플리케이션 및 하이브리드 웹 네이티브 애플리케이션에 적용될 수 있습니다.  
Most of the advice also applies to native applications (also known as "mobile apps").  
대부분의 조언은 또한 네이티브 애플리케이션에 적용될 수 있습니다. 일명 "모바일앱" 입니다.  

Note: WCAG 2.0 does not provide testable success criteria for some of the mobile-related issues.   
메모: WCAG 2.0는 일부 모바일 관련 문제에 대해 검증 가능한 성공 기준을 제공하지 않습니다.  
The work of the Mobile Accessibility Task Force has been to develop techniques and best practices in these areas.   
모바일 접근성 Task Force의 작업은 이러한 영역에서 기술과 모범 사례를 개발하는 것이었습니다.  
When the techniques or best practices don't map to specific WCAG success criteria, they aren't given a sufficient, advisory or failure designation.   
기술 또는 모범 사례가 특정 WCAG 성공 기준에 부합하지 않는 경우 충분한 조언 또는 실패 지정이 제공되지 않습니다.  
This doesn't mean that they are optional for creating accessible web content on a mobile platform, but rather that they cannot currently be assigned a designation.   
이는 모바일 플랫폼에서 접근 가능한 웹 컨텐츠를 생성하기위한 선택 사항이 아니라 현재 지정을 지정할 수 없다는 의미입니다.  
The Task Force anticipates that some of these techniques will be included as sufficient or advisory in a potential future iteration of WCAG.  
Task Force는 WCAG의 향후 잠재적 반복에 이러한 기술 중 일부가 충분하거나 자문으로 포함될 것으로 예상합니다.  

The current document references existing WCAG 2.0 Techniques that apply to mobile platform (see Appendix A) and provides new best practices, which may in the future become WCAG 2.0 Techniques that directly address emerging mobile accessibility challenges such as small screens, touch and gesture interface, and changing screen orientation.  
현재 문서는 모바일 플랫폼에 적용되는 기존 WCAG 2.0 기술을 참조하고 (부록 A 참조) 작은 화면, 터치 및 제스처 인터페이스, 화면 방향 변경과 같은 모바일 접근성 문제를 직접 해결할 수있는 향후 WCAG 2.0이 될 수도 있는 새로운 모범사례를 제공 할 예정입니다.  


**1.2 Other W3C-WAI Guidelines Related to Mobile**  
모바일과 관련된 다른 W3C-WAI 지침  

* 1.2.1 UAAG 2.0 and Accessible Mobile Browsers  
UAAG 2.0와 모바일 브라우저 접근성  
The User Agent Accessibility Guidelines (UAAG) 2.0 [UAAG2] is meant for the developers of user agents (e.g. web browsers and media players), whether for desktop/laptop or mobile operating systems.   
사용자 에이전트 접근성 지침 2.0은 데스크탑/랩탑 또는 모바일 운영 체제와 관계없이 사용자 에이전트(예: 웹 브라우저 및 미디어 플레이어)의 개발자를 위한 것입니다.  
A user agent that follows UAAG 2.0 will improve accessibility through its own user interface, through options it provides for rendering and interacting with ​content, and through its ability to communicate with other technologies, including assistive technologies.  
UAAG 2.0을 따르는 사용자 에이전트는 자체 사용자 인터페이스, 콘텐츠 렌더링 및 상호 작용을 위한 옵션, 보조 기술을 포함한 다른 기술과의 통신 기능을 통해 접근성을 향상시킵니다.  
To assist developers of mobile browsers, the UAAG 2.0 Reference support document contains numerous mobile examples.   
모바일 브라우저의 개발자들을 지원하기 위해, UAAG 2.0 참조 문서에는 다양한 모바일 예들이 포함되어 있습니다.  
These examples are also available in a separate list of mobile-related examples, maintained by the User Agent Accessibility Guidelines Working Group (UAWG).  
이 예는 UAWG(User Agent Accessibility Guideline Working Group)에서 유지 관리하는 별도의 모바일 관련 예제 목록에서도 사용할 수 있습니다.  

* 1.2.2 ATAG 2.0 and Accessible Mobile Authoring Tools  
ATAG 2.0과 접근 가능한 모바일 제작도구   
The Authoring Tool Accessibility Guidelines (ATAG) 2.0 [ATAG2] provides guidelines for the developers of authoring tools, whether for desktop/laptop or mobile operating systems.  
저작도구 접근성 지침(ATAG) 2.0 은 데스크탑/랩탑이나 모바일 운영 체제든 아니든 저작도구의 개발자를 위한 제공합니다.  
An authoring tool that follows ATAG 2.0 will be both more accessible to authors with disabilities (Part A) and designed to enable, support, and promote the production of more accessible web content by all authors (Part B).  
ATAG 2.0을 따르는 저작 도구는 장애를 가진 저자(A부)가 더 쉽게 접근할 수 있으며, 모든 저자(B부)가 보다 쉽게 접근할 수 있는 웹 콘텐츠의 제작을 지원 및 촉진하도록 설계되었습니다.  

To assist developers of mobile authoring tools, the Implementing ATAG 2.0 support document contains numerous mobile authoring tool examples  
모바일 저작도구의 개발자를을 지원하기 위해, ATAG 2.0 지원 문서 구현에는 다양한 모바일 작성 도구 예가 포함되어 있습니다.  


2.Mobile accessibility considerations primarily related to Principle 1: Perceivable
---
2.모바일 접근성 고려사항은 주로 원칙 1: 인지할 수 있음 과 관련이 있습니다.  

**2.1 Small Screen Size**  
2.1 작은 화면 크기  
Small screen size is one of the most common characteristics of mobile devices.   
작은 화면 크기는 모바일 기기의 가장 공통적인 특징 중의 하나입니다.  
While the exceptional resolution of these screens theoretically enables large amounts of information to be rendered, the small size of the screen places practical limits on how much information people can actually view at one time, especially when magnification is used by people with low vision.  
이러한 화면의 예외적인 해상도는 이론적으로 대량의 정보를 렌더링할 수 있는 반면, 작은 크기의 화면은 사람들이 실제로 한 번에 볼 수 있는 정보의 양에 실질적인 제한을 두는데, 특히 시야가 낮은 사람들이 배율을 사용할 때 그러합니다.  
Some best practices for helping users to make the most of small screens include  
사용자가 작은 화면을 최대한 활용할 수 있도록 지원하는 몇 가지 모범사례는 다음과 같습니다.  

- Minimizing the amount of information that is put on each page compared to desktop/laptop versions by providing a dedicated mobile version or a responsive design:  
전용 모바일 버전 또는 반응형 디자인을 제공하여 데스크탑/ 랩탑 버전과 비교하여 각 페이지에 입력되는 정보의 양을 최소화하십시오.  
  - a dedicated mobile version contains content tailored for mobile use. For example, the content may contain fewer content modules, fewer images, or focus on important mobile usage scenarios.    
전용 모바일 버전은 모바일 용으로 맞춤 설정된 콘텐츠를 포함합니다. 예를 들어, 콘텐츠에는 아마 더 적은 수의 콘텐츠 모듈이 포함되거나, 이미지 또는 중요한 모바일 사용 시나리오에 집중될 수 있습니다.  
  - a responsive design contains content that stays the same, but CSS stylesheets are used to render it differently depending on the viewport width. For example, on narrow screens the navigation menus may be hidden until the user taps a menu button.  
반응성 설계에는 동일하게 유지되는 내용이 포함되지만 CSS 스타일시트는 뷰포트 넓이에 따라 다르게 렌더링하는 데 사용됩니다. 예를 들어 좁은 화면에서 사용자가 메뉴 버튼을 누를 때까지 탐색 메뉴가 숨겨질 수 있습니다.  

- Providing a reasonable default size for content and touch controls (see "B.2 Touch Target Size and Spacing") to minimize the need to zoom in and out for users with low vision.  
시력이 낮은 사용자를 위해 확대, 축소할 필요성을 최소화 하기 위해 콘텐츠 및 터치 컨트롤에 적합한 기본 크기를 제공하십시오.  

- Adapting the length of link text to the viewport width.  
링크 텍스트의 길이는 뷰포트 넓이에 맞추십시오.
  
- Positioning form fields below, rather than beside, their labels (in portrait layout)  
양식 필드를 레이블 옆에 위치시키지 마십시오.(세로 레이아웃에서)  

**2.2 Zoom/Magnification**  
2.2 확대축소/확대  

A variety of methods allow the user to control content size on mobile devices with small screens.
다양한 방법은 작은 화면을 가진 모바일 기기에서의 콘텐츠 사이즈를 컨트롤하는 사용자를 허용합니다. (사용자가 다양한 방법을 통해 작은 화면의 모바일기기에서 콘텐츠 크기 제어 가능합니다)
At the browser level these methods are generally available to assist a wide audience of users. 
브라우저 수준에서 이러한 방법은 일반적으로 다양한 사용자를 지원하기 위해 이용 가능 합니다.  
At the platform level these methods are available as accessibility features to serve people with visual impairments or cognitive disabilities.  
플랫폼 수준에서 이러한 방법은 시각 장애 또는 인지 장애를 가진 사람들에게 제공되는 접근성 기능으로 이용 가능 합니다.  

The methods include the following:  
그 방법들은 아래 지시사항을 포함합니다.  

- OS-level features  
 OS 수준 기능
  - Set default text size (typically controlled from the Display Settings) Note: System text size is often not supported by mobile browsers.  
  기본 글자 크기 설정 (일반적으로 화면 설정에서 제어) 참고: 시스템 글자 크기는 모바일 브라우저에서 종종 지원이 되지 않습니다.
  
  - Magnify entire screen (typically controlled from the Accessibility Settings). Note: Using this setting requires the user to pan vertically and horizontally.  
  전체 화면 확대 (일반적으로 접근성 설정에서 제어) 참고: 이 설정을 사용하려면 사용자가 세로 및 가로로 이동해야합니다.
  
  - Magnifying lens view under user's finger (typically controlled from the Accessibility Settings)  
  사용자 손가락 아래 확대 렌즈 보기(일반적으로 접근성 설정에서 제어)

- Browser-level features   
  브라우저 수준 기능  
  - Set default text size of text rendered in the browser's viewport  
    브라우저의 뷰포트에 렌더링 된 기본 글자 크기 설정  
    - Reading mode that renders main content at a user-specified text size  
      사용자 지정 텍스트 크기로 기본 내용을 렌더링하는 읽기모드
      
  - Magnify browser's viewport (typically "pinch-zoom"). Note: Using this setting requires the user to pan vertically and horizontally.  
    브라우저의 뷰포트 확대 참고: 이 설정을 사용하려면 사용자가 세로 및 가로로 이동해야합니다.
    - Note: Some browsers have features that might modify this type of magnification (e.g. re-flowing the content at the new magnification level, overriding author attempts to prevent pinch-zoom).  
      참고: 몇몇 브라우저에는 이러한 확대 유형을 수정할 수 있는 기능이 있습니다. (예: 핀 확대,축소를 방지하려는 작성자 시도를 무시하고 새로운 배율로 콘텐츠를 다시 흐르게 하는 것)  

The WCAG 2.0 success criterion that is most related to zoom/magnification is  
줌/확대와 가장 관련이 있는 wcag 2.0 성공 기준은 다음과 같습니다.  

```
1.4.4 Resize text (Level AA)
```

SC 1.4.4 requires text to be resizable without assistive technology up to 200 percent. To meet this requirement content must not prevent text magnification by the user.  
1.4.4는 보조 기술없이 최대 200%의 글자 크기를 재조정 할 수 있을 것을 요구합니다. 이 요구 사항을 충족 시키기 위해 콘텐츠가 사용자의 글자 확대를 막아서는 안됩니다.  

The following methods might be used:  
다음방법을 사용할 수 있습니다.  

- Ensure that the browser pinch zoom is not blocked by the page's viewport meta element so that it can be used to zoom the page to 200%. Restrictive values for user-scalable and maximum-scale attributes of this meta element should be avoided.  
  브라우저의 pinch 확대/축소가 페이지의 뷰포트 메타 요소에 의해 차단되지 않도록 해 페이지를 200%로 확대하는데 사용될 수 있도록 하십시오. 이 메타요소의 사용자 확장 가능 및 최대 스케일 속성에 대한 제한적인 값은 피해야 합니다.   
  Note: Relying on full viewport zooming (e.g. not blocking the browser's pinch zoom feature) requires the user to pan horizontally as well as vertically.   
  참고: 전체 뷰포트 확대.축소(예: 브라우저의 집기 확대/ 축소 기능을 차단하지 않음)를 사용하려면 사용자가 세로뿐만 아니라 가로로 이동해야합니다.     
  While this technique meets the success criteria it is less usable than supporting text resizing features that reflow content to the user's chosen viewport size.    
  이 기술은 성공 기준을 충족하지만 사용자가 선택한 뷰포트 크기로 내용을 리플로우하는 글자 크기 조정 기능을 지원하는 것보다 사용하기에 적합하지 않습니다.     
  It is best practice to use techniques that support text resizing without requiring horizontal panning.    
  가장 좋은 것은 가로 패닝을 요구하지 않고 글자 크기 조정을 지원하는 기술을 사용하는 것입니다.    
  
- Support for system fonts that follow platform level user preferences for text size.  
  글자 크기에 대한 플랫폼 수준의 사용자 기본 설정을 따르는 시스템 글꼴을 지원합니다.  
  
- Provide on-page controls to change the text size.    
  글자 크기를 바꾸는 컨트롤을 페이지 내부에 제공합니다.  

Accessibility features geared toward specific populations of people with disabilities fall under the definition of assistive technology adopted by WCAG and thus cannot be relied upon to meet the success criteria.  
wcag가 채택한 보조 기술의 정의에 장애인의 특정 모집단에 맞춰진 접근성 기능은  성공 기준을 충족시키는데 의존 할 수없습니다. (특정 모집단에 맞춰진 접근성은 성공 기준이 아니다)  
For example, a platform-level zoom feature that magnifies all platform content and has features to specifically support people with low vision is likely considered an assistive technology.  
예를 들어, 모든 플랫폼 콘텐츠를 확대하고 시력이 낮은 사람들을 지원할 수 있는 기능을 갖춘 플랫폼 수준의 확대/축소 기능은 보조 기술로 간주될 수 있습니다.  

**2.3 Contrast**  
2.3 대비  

Mobile devices are more likely than desktop/laptop devices to be used in varied environments including outdoors, where glare from the sun or other strong lighting sources is more likely.  
모바일 기기들은 데스크탑/랩탑 기기보다 야외등 다양한 환경에서 사용할 가능성이 높습니다.   

This scenario heightens the importance of use of good contrast for all users and may compound the challenges that users with low vision have accessing content with poor contrast on mobile devices.  
이 시나리오는 모든 사용자들을 위한 좋은 대비의 사용의 중요성을 높이고 시력이 낮은 사용자가 모바일 기기에서 대비가 낮은 콘텐츠에 접근할때 어려움이 복합 될 수 있습니다.  

The WCAG 2.0 success criteria related to the issue of contrast are:  
대비에 관련이 있는 wcag 2.0 성공 기준은 다음과 같습니다.  

```
1.4.3 Contrast (Minimum) (Level AA) which requires a contrast of at least 4.5:1 (or 3:1 for large-scale text) and
1.4.6 Contrast (Enhanced) (Level AAA) which requires a contrast of at least 7:1 (or 4.5:1 for large-scale text).
1.4.3. 대비(최소) 대비는 적어도 4.5: 1 (이나 큰 크기의 글자의 경우 3:1)이 요구되고, 1.4.6 대비(강화) 적어도 7:1 (이나 큰 크기의 글자의 경우 4.5:1)
```

SC 1.4.3. allows for different contrast ratios for large text.   
1.4.3은  큰 글자의 다른 대비를 허용합니다.   

Allowing different contrast ratios for larger text is useful because larger text with wider character strokes is easier to read at a lower contrast.  
허용되는 다른 큰 글자의 비는 유용합니다. 왜냐하면 더 넓은 문자 획을 가진 큰 글자는 낮은 대비에서도 읽기가 쉽기 때문입니다.   

This allows designers more leeway for contrast of larger text, which is helpful for content such as titles.  
이는 디자이너에게 큰 텍스트의 대비에 대해 더 많은 재량을 허용해 제목과 같은 콘텐츠에 도움이 됩니다.  
The ratio of 18-point text or 14-point bold text described in the SC 1.4.3 was judged to be large enough to enable a lower contrast ratio for web pages displayed on a 15-inch monitor at 1024x768 resolution with a 24-inch viewing distance.  
1.4.3에 설명된 18포인트나 굵은 14포인트 글자 비율은  24인치 시야 거리를 가진 1024x768 해상도에서 15인치 모니터에 표시되는 웹 페이지에 대해 낮은 대비 비율을 제공할 수 있을 정도로 충분히 큰 것으로 판단되었습니다.   
Mobile device content is viewed on smaller screens and in different conditions so this allowance for lessened contrast on large text must be considered carefully for mobile apps.  
모바일 기기 콘텐츠는 더 작은 화면과 다른 조건에서 볼 수 있으므로 큰 글자의 대비를 줄이는 데 사용할 수 있는 허용량을 모바일 앱의 경우 신중하게 고려해야 합니다.  

For instance, the default point size for mobile platforms might be larger than the default point size used on non-mobile devices.   
예를 들어, 모바일 플랫폼의 기본 포인트 사이즈는 모바일이 아닌 기기에서 사용된 기본 포인트 사이즈보다 작을 것입니다.   
When determining which contrast ratio to follow, developers should strive to make sure to apply the lessened contrast ratio only when text is roughly equivalent to 1.2 times bold or 1.5 times (120% bold or 150%) that of the default platform size.   
따라야 할 명암비를 결정할 때, 개발자는 글자가 기본 플랫폼 크기의 1.2배 또는 1.5배(120% 굵게 또는 150%)와 거의 동일한 경우에만 축소된 대비 비율을 적용해야합니다.   
Note, however, that the use of text that is 1.5 times the default on mobile platforms does not imply that the text will be readable by a person with low vision.   
그러나 모바일 플랫폼에서 1.5배의 텍스트 사용이 시력이 낮은 사람이 글자를 읽을 수 있음을 의미하지는 않습니다.  
People with low vision will likely need and use additional platform level accessibility features and assistive technology such as increased text size and zoom features to access mobile content.  
시력이 낮은 사람들은 모바일 콘텐츠에 접근하기 위해 추가 플랫폼 수준 접근성 기능과 글자 크기 증가 및 확대축소 기능과 같은 보조 기술을 필요로 하고 사용하게 될 것입니다.  


3. Mobile accessibility considerations primarily related to Principle 2: Operable
----
3.원칙2:운용가능한 와 주로 관계된 모바일 접근성 고려사항    

**3.1 Keyboard Control for Touchscreen Devices**  
3.1 터치스크린 기기를 위한 키보드 컨트롤  

Mobile device design has evolved away from built-in physical keyboards (e.g. fixed, slide-out) towards devices that maximize touchscreen area and display an on-screen keyboard only when the user has selected a user interface control that accepts text input (e.g. a textbox).  
모바일 기기 디자인은 내장된 물리적(예: 고정식, 슬라이드아웃) 키보드에서 사용자가 텍스트 입력을 허용하는 인터페이스 제어(예: 텍스트 박스)를 선택했을 때만 화면에 키보드를 표시하는 장치로 발전해왔습니다.  

However, keyboard accessibility remains as important as ever and most major mobile operating systems do include keyboard interfaces, allowing mobile devices to be operated by external physical keyboards (e.g. keyboards connected via Bluetooth, USB On-The-Go) or alternative on-screen keyboards (e.g. scanning on-screen keyboards).  
하지만, 키보드 접근성은 무엇보다 중요하며,  대부분의 주요 모바일 운영체제에는 키보드 인터페이스가 포함되어 있어 모바일 장치를 외부 물리적 키보드(예: 블루투스로 연결된 키보드, USB) 대체 화면 키보드(예: 화면의 키보드)로 작동할 수 있습니다.  

Supporting these keyboard interfaces benefits several groups with disabilities:  
이러한 키보드 인터페이스를 지원하는 것은 장애를 가진 다양한 그룹들에게 이점을 줍니다.  
- People with visual disabilities who can benefit from some characteristics of physical keyboards over touchscreen keyboards (e.g. clearly separated keys, key nibs and more predictable key layouts).  
  터치스크린키보드를 통해 물리적 키보드의 일부 특성으로부터 혜택을 얻을 수 있는 시각장애인. 
   
- People with dexterity or mobility disabilities, who can benefit from keyboards optimized to minimize inadvertent presses (e.g. differently shaped, spaced and guarded keys) or from specialized input methods that emulate keyboard input.  
  부주의한 누름(예: 서로 다른 모양, 간격 및 보호되는 키)을 최소화하도록 최적화된 키보드나 키보드 입력을 모방하는 특수 입력 방법의 혜택을 얻을 수 있는 손재주 또는 이동성 장애를 가진 사람들.  
  
- People who can be confused by the dynamic nature of onscreen keyboards and who can benefit from the consistency of a physical keyboard.  
  화면 키보드의 동적 특징에 혼란이 될 수 있고 물리적 키보드의 일관성으로 부터 혜택을 얻을 수 있는 사람들.  

Several WCAG 2.0 success criteria are relevant to effective keyboard control:  
효과적인 키보드 컨트롤에 관련된 여러 WCAG 2.0의 성공기준 입니다  

```
2.1.1 Keyboard (Level A)
2.1.2 No Keyboard Trap (Level A)
2.4.3 Focus Order (Level A)
2.4.7 Focus Visible (Level AA)
```

**3.2 Touch Target Size and Spacing**  
3.2 터치 대상 크기와 공간  

The high resolution of mobile devices means that many interactive elements can be shown together on a small screen. But these elements must be big enough and have enough distance from each other so that users can safely target them by touch.  
모바일 기기의 고해상도화는  작은 기기에서 상호작용하는 많은 요소들이 함께 보여줄 수 있다는 것을 의미합니다. 그러나 이 요소들은 사용자가 터치에 의해 안전하게 타겟팅을 할 만큼 충분히 커야하고 각각 충분한 거리가 있어야합니다.  

Best practices for touch target size include the following:  
터치 대상의 사이즈에 대한 가장 좋은 것은 다음을 포함합니다.  

- Ensuring that touch targets are at least 9 mm high by 9 mm wide.  
  터치 대상의 높이가 최소 9mm, 너비가 9mm가 되도록 하세요  
  
- Ensuring that touch targets close to the minimum size are surrounded by a small amount of inactive space.  
  최소 크기에 가까운 터치 대상이 최소 활성화되지않은 공간으로 둘러 싸이게 하세요.  

Note: This size is not dependent on the screen size, device or resolution. Screen magnification should not need to be used to obtain this size, because magnifying the screen often introduces the need to pan horizontally as well as vertically, which can decrease usability.  
참고: 이 사이즈는 스크린크기, 디바이스나 해상도에 의존하지 않습니다. 이 크기를 위해 화면 확대를 사용할 필요가 없습니다. 왜냐하면 화면을 확대하면 가로뿐아니라 세로로도 팬이 필요하기 때문에 유용성이 줄어들 수 있습니다.  

**3.3 Touchscreen Gestures**  
3.3 터치화면 동작  

Many mobile devices are designed to be primarily operated via gestures made on a touchscreen. These gestures can be simple, such as a tap with one finger, or very complex, involving multiple fingers, multiple taps and drawn shapes.  
많은 모바일 기기들은 터치스크린에서 만들어진 동작을 통해 주로 작동하도록 디자인되었습니다. 이 동작들은 한손으로 탭하는 것과 같이 쉬울 수 있고, 여러 손가락을 수반하고, 여러 개의 탭 및 그려진 모양을 포함하는 아주 복잡할 수 있습니다.  

Some (but not all) mobile operating systems provide work-around features that let the user simulate complex gestures with simpler ones using an onscreen menu.  
몇몇 (그러나 다는 아닌) 모바일 운영 체제는 사용자가 화면 메뉴를 사용해서 간단한 동작으로 복잡한 동작을 시뮬레이션 할 수 있는 작업 기능을 제공합니다.  

Some best practices when deciding on touchscreen gestures include the following:  
터치화면 동작을 결정하는데 가장 좋은 방법은 다음에 말하는 것을 포함합니다.	  

- Gestures in apps should be as easy as possible to carry out.     
  앱안에 동작들은 가능한 수행하기 쉬워야 합니다.    
  This is especially important for screen reader interaction modes that replace direct touch manipulation by a two-step process of focusing and activating elements.  
  이것은 이는 요소를 집중시키고 활성화하는 2단계 프로세스로 직접 터치 조작을 대체하는 스크린 리더기 상호 작용 모드에 특히 중요합니다.  
  It is also a challenge for users with motor or dexterity impairments or people who rely on head pointers or a stylus where multi-touch gestures may be difficult or impossible to perform.   
  또한 운동이나 손재주 장애를 가진 사용자또는 멀티 터치 동작이 어렵거나 불가능할 수있는 헤드 포인터 또는 스타일러스를 사용하는 사용자를 위한 도전 입니다.  
  Often, interface designers have different options for how to implement an action.   
  보통 인터페이스 디자이너들은 동작을 시행하는 방법에 대한 어려움을 가집니다.  
  Widgets requiring complex gestures can be difficult or impossible to use for screen reader users. Usually, design alternatives exist to allow changes to settings via simple tap or swipe gestures.  
  복잡한 동작이 필요한 위젯들은 스크린 리더 사용자가 사용하기 어렵거나 불가능할 수 있습니다. 대게, 간단한 탭이나 스와이프 동작을 통해 설정을 변경할 수 있는 설계 대안이 있습니다.  
  
- Activating elements via the mouseup or touchend event.   
  마우스업이나 터치엔드 이벤트를 통한 요소 활성화.  
  Using the mouseup or touchend event to trigger actions helps prevent unintentional actions during touch and mouse interaction.   
  마우스업이나 터치엔드 이벤트를 트리거 액션으로 사용하는 것은 터치와 마우스의 상호작용 동안 의도치 않은 행동을 방지 할 수 있습니다.  
  Mouse users clicking on actionable elements (links, buttons, submit inputs) should have the opportunity to move the cursor outside the element to prevent the event from being triggered.   
  실행 가능힌 요소들을(링크,버튼,제출 버튼) 클릭하는 마우스 사용자는 커서가 이벤트가 트리거 되지 않을 요소 바깥으로 움직일 기회를 잡아야 합니다.(바깥으로 움직여야 합니다.)  
  This allows users to change their minds without being forced to commit to an action.   
  이를 통해 사용자는 행동을 강요하지 않고도 마음을 바꿀 수 있습니다. (바꾸는 것을 허용합니다.)   
  In the same way, elements accessed via touch interaction should generally trigger an event (e.g. navigation, submits) only when the touchend event is fired (i.e. when all of the following are true: the user has lifted the finger off the screen, the last position of the finger is inside the actionable element, and the last position of the finger equals the position at touchstart).    
  같은 맥락으로, 터치 상호작용을 통해 접근된 요소들은 일반적으로 이벤트에 트리거 되야 합니다.(예: 네비게이션, 제출) 오직 터치된 이벤트가 발생했을 때 입니다. (즉, 다음 모든 사항에 해당하는 경우: 사용자가 화면에서 손가락을 들어 올린 후, 마지막 손가락의 위치가 실행가능한 요소 내부에 있고, 손가락의 마지막 위치는 터치 시작의 위치와 같을 때)  

Another issue with touchscreen gestures is that they might lack onscreen indicators that remind people how and when to use them.   
터치 스크린 동작에 관한 또다른 이슈는 사람들에게 언제 어떻게 사용할 것인지를 상기시키는 화면 지시사항이 부족한 것입니다.    
For example, a swipe in from the left side of the screen gesture to open a menu is not discoverable without an indicator or advisement of the gesture. See Touchscreen gesture instructions.  
예를 들어, 화면 동작의 왼쪽에서부터 와이프해서 메뉴를 열면 동작의 표기나 조언 없이는 발견 할 수 없습니다. 터치화면 동작 지시사항을 보세요.  


**3.4 Device Manipulation Gestures**
3.4 기기 다중 동작들

In addition to touchscreen gestures, many mobile operating systems provide developers with control options that are triggered by physically manipulating the device (e.g. shaking or tilting).   
터치화면 동작들 외에도 많은 모바일 운영 체제는 개발자에게 기기를 물리적으로 조작함으로써 유발되는 제어 옵션(예: 흔들림 이나 기울임) 을 제공합니다.  
While device manipulation gestures can help developers create innovative user interfaces, they can also be a challenge for people who have difficulty holding or are unable to hold a mobile device.  
기기 조작 동작은 개발자가 혁신적인 사용자 인터페이스를 만드는데 도움이 될 수 있지만, 또한 모바일 기기를 가지기 어렵거나 가질 수 없는 사람들에게 어려움을 줄 수 있습니다.  

Some (but not all) mobile operating systems provide work-around features that let the user simulate device shakes, tilts, etc. from an onscreen menu.  
몇몇(전부는 아닌) 모바일 운영 체제는 사용자가 화면 메뉴에서 기기 흔들고, 기울이기 등등 시뮬레이션 할 작업 기능을 제공합니다.   
Therefore, even when device manipulation gestures are provided, developers should still provide touch and keyboard operable alternative control options.  
즉, 심지어 기기 조작 동작이 제공 되더라도 개발자들은 여전히 터치와 키보드 운용가능한 대체 조작 옵션들을  제공해야 합니다.  

```
2.1.1 Keyboard (Level A)
```

Another issue with control via device manipulation gestures is that they might lack onscreen indicators that remind people how and when to use them. See Touchscreen gesture instructions.  
기기 조작 동작을 통한 제어에 관한 또다른 이슈는 사람들에게 언제 어떻게 사용할 것인지를 상기시키는 화면 지시사항이 부족한 것입니다.  

**3.5 Placing buttons where they are easy to access**  
3.5 접근하기 쉬운 곳에 버튼들을 위치하기  

Mobile sites and applications should position interactive elements where they can be easily reached when the device is held in different positions.  
모바일 사이트와 애플리케이션은 기기가 서로 다른 위치에 있을 때 쉽게 도달할 수 있는 상호작용하는 요소들이 위치해야합니다.  

When designing mobile web content and applications many developers attempt to optimize use with one hand.   
모바일 웹 콘텐츠와 애플리케이션을 설계할 때 많은 개발자가 한 손으로 사용을 최적화 하려 합니다.  
This can benefit people with disabilities who may only have one hand available, however, developers should also consider that an easy-to-use button placement for some users might cause difficulties for others (e.g. left- vs. right-handed use, assumptions about thumb range of motion). Therefore, flexible use should always be the goal.  
이것은 한손으로만 사용 가능한 장애를 가진 사람들에게 이점을 줄 수 있습니다. 그러나 개발자는 또한 일부 사용자들을 위한 사용하기 쉬운 버튼의 위치가 다른 사용자에게 어려움을 줄 수 있다는 것을 고려해야합니다. (예: 왼손 대 오른손 사용, 엄지 동작 범위에 대한 가정). 그러므로 유연한 사용은 항상 목표가 되어야합니다.  

Some (but not all) mobile operating systems provide work-around features that let the user temporarily shift the display downwards or sideways to facilitate one-handed operation.  
일부 (전체가 아닌) 모바일 운영 체제는 한손으로 작업 할 수 있도록 사용자가 임시로 디스플레이를 아래쪽이나 옆쪽으로 옮길 수 있는 작업 기능을 제공합니다.  


4. Mobile accessibility considerations related primarily to Principle 3: Understandable
----
4.원칙3:이해하기쉬운 과 주로 관계된 모바일 접근성 고려사항  

**4.1 Changing Screen Orientation (Portrait/Landscape)**  
4.1 화면 방향 변경 (세로/가로)  

Some mobile applications automatically set the screen to a particular display orientation (landscape or portrait) and expect that users will respond by rotating the mobile device to match. However, some users have their mobile devices mounted in a fixed orientation (e.g. on the arm of a power wheelchair).  
일부 모바일 애플리케이션은 자동으로 화면을 특정 화면 방향(가로나 세로로)을 설정하고, 사용자가 모바일 기기를 회전하여 응답 할 것으로 예측합니다. 하지만, 일부 사용자는 고정된 방향(예: 전동 휠체어의 팔)에 모바일 기기를 고정합니다.   
Therefore, mobile application developers should try to support both orientations. If it is not possible to support both orientations, developers should ensure that it is easy for all users to change the orientation to return to a point at which their device orientation is supported.  
그러므로, 모바일 애플리케이션 개발자들은 양방향 다 지원하도록 노력해야 합니다. 만약 양방향 지원이 불가하다면, 개발자들은 모든 사용자가 장치 방향이 지원되는 지점으로 돌아가기 위해 방향을 변경하는 것이 쉽도록 해야합니다.  

Changes in orientation must be programmatically exposed to ensure detection by assistive technology such as screen readers. For example, if a screen reader user is unaware that the orientation has changed the user might perform incorrect navigation commands.  
방향의 변경은 스크린 리더기와 같은 보조 기술로 감지되도록 프로그램적으로 노출되어야 합니다. 예를 들어, 스크린 리더기 사용자가 방향이 변경되었다는 것을 인지하지 못한 경우, 사용자가 잘못된 탐색 명령을 수행 할 수 있습니다.  

**4.2 Consistent Layout**  
4.2 일관된 레이아웃  

Components that are repeated across multiple pages should be presented in a consistent layout.   
여러 페이지에 걸쳐 반복되는 컴포넌트들은 일관된 레이아웃으로 나타나야 합니다.  
In responsive web design, where components are arranged based on device size and screen orientation, web pages within a particular view (set size and orientation) should be consistent in placement of repeated components and navigational components. Consistency between the different screen sizes and screen orientations is not a requirement under WCAG 2.0.  
반응형 웹 디자인에서, 기기 사이즈나 화면 방향을 기반으로 조정되는 컴포넌트들이 배치되는 경우, 특정보기 (크기 밑 방향 설정) 내의 웹 페이지는 반복되는 구성 요소와 탐색 구성 요소의 배치가 일관되어야합니다. 다른 화면 크기와 화면 방향 사이에 일관성은 WCAG 2.0에 요구사항이 아닙니다.  
 
For example:  
예를 들어:  
- A Web site has a logo, a title, a search form and a navigation bar at the top of each page; these appear in the same relative order on each page where they are repeated.   
  웹 사이트는 로고, 제목, 검색양식, 네비게이션바를 각 페이지 상단에 가지고 있습니다; 이들은 반복되는 각 페이지에 동일한 순서로 나타납니다. 
  On one page the search form is missing but the other items are still in the same order.   
  한 페이지에서 검색양식은 누락되었지만, 다른 요소들은 여전히 동일한 순서로 있습니다.  
  When the Web site is viewed on a small screen in portrait mode, the navigation bar is collapsed into a single icon but entries in the drop-down list that appears when activating the icon are still in the same relative order.  
  세로모드인 작은 화면에서 웹 사이트가 보여질 때, 네비게이션 바는 하나의 아이콘으로 축소 되지만, 아이콘이 활성화 될 때는 나타나는 드롭 다운 목록의 항목은 여전히 동일한 순서입니다.  
- A Web site, when viewed on the different screen sizes and in different orientations, has some components that are hidden or appear in a different order. The components that show, however, remain consistent for any screen size and orientation.  
  다른 방향과 다른 화면 사이즈에서 볼 때, 웹사이트는 일부 컴포넌트가 숨겨져 있거나 다른 순서로 표시됩니다. 그러나 보여지는 컴포넌트는 화면 크기와 방향에 대해 일관성을 유지합니다.   

The WCAG 2.0 success criteria that are most related to the issue of consistency are:  
일관성 이슈와 관련된 WCAG 2.0의 성공 기준입니다.  

```
3.2.3 Consistent Navigation (Level AA)
3.2.4 Consistent Identification (Level AA)
```

**4.3 Positioning important page elements before the page scroll**  
4.3 페이지 스크롤 전에 중요한 페이지 요소들 배치  

The small screen size on many mobile devices limits the amount of content that can be displayed without scrolling.  
많은 모바일 기기의 작은 화면 사이즈는 스크롤없이 표시할 수 있는 콘텐츠의 양이 제한적입니다.  
Positioning important page information so it is visible without requiring scrolling can assist users with low vision and users with cognitive impairments.  
중요한 페이지 정보를 스크롤 하지않고도 볼 수 있도록 배치하면 시력이 낮은 사용자와 인지 장애를 가진 사용자에게 도움이 될 수 있습니다.   
If a user with low vision has the screen magnified only a small portion of the page might be viewable at a given time.   
시력이 낮은 사용자가 화면을 확대하면 특정 시간에 페이지의 일부만 볼 수 있습니다.   
Placing important elements before the page scroll allows those who use screen magnifiers to locate important information without having to scroll the view to move the magnified area.   
페이지 스크롤 전에 중요한 페이지 요소들 배치하면 확대된 영역을 이동하기 위해 화면을 스크롤 없이 화면 돋보기를 사용해 중요한 정보를 찾을 수 있습니다.    
Placing important elements before the page scroll also makes it possible to locate content without performing an interaction.   
페이지 스크롤 전에 중요한 페이지 요소들 배치하면 상호작용없이 콘텐트의 위치 또한 찾을 수 있습니다.  
This assists users that have cognitive impairments such as short-term memory disabilities.   
이것은 사용자가 단기기억 장애와 같은 인지장애를 가진 사용자를 돕습니다.   
Placing important elements before the page scroll also helps ensure that elements are placed in a consistent location. Consistent and predictable location of elements assists people with cognitive impairments and low vision.  
페이지 스크롤 전에 중요한 페이지 요소들 배치하면 또한 일관성있는 위치에 요소를 배치됩니다. 요소의 일관성있고 예측가능한 위치는 인지장애와 시력이 낮은 사용자를 돕습니다.  

**4.4 Grouping operable elements that perform the same action**  
4.4 동일한 작업을 수행하는 작동가능한 요소의 그룹화  

When multiple elements perform the same action or go to the same destination (e.g. link icon with link text), these should be contained within the same actionable element.   
다중 요소가 동일한 작업이나 동일한 목적(예: 링크 텍스트와 링크 아이콘)으로 이동을 수행할 때, 이들은 동일한 작동가능한 요소가 포함되어야합니다.  
This increases the touch target size for all users and benefits people with dexterity impairments. It also reduces the number of redundant focus targets, which benefits people using screen readers and keyboard/switch control.  
이것은 모든사용자의 터치 대상 크기를 증가시키고 손재주 장애를 가진 사람들에게 이점을 제공합니다. 또한 키보드/스위치 컨트롤러와 스크린 리더를 사용하는 사용자에게 이점이 되는 중복 초점 대상의 수를 줄입니다.   
The WCAG 2.0 success criterion that is most related to grouping of actionable elements is:  
작동가능한 요소의 그룹화와 관련된 WCAG 2.0의 성공 기준 입니다.  

```
2.4.4 Link Purpose (In Context) (Level A)
2.4.9 Link Purpose (Link Only) (Level AA)
```

For more information on grouping operable elements, see H2: Combining adjacent image and text links for the same resource technique.  
작동가능한 요소의 그룹화에 대한 더 많은 정보는, 같은 자원에 대한 인접 이미지와 텍스트의 링크 결합을 참조하세요.  


**4.5 Provide clear indication that elements are actionable**  
4.5 작동 가능한 요소의 명확한 인지사항 제공  

Elements that trigger changes should be sufficiently distinct to be clearly distinguishable from non-actionable elements (content, status information, etc). Providing a clear indication that elements are actionable is relevant for web and native mobile applications that have actionable elements like buttons or links, especially in interaction modes where actionable elements are commonly detected visually (touch and mouse use).   
변화를 유발하는 요소들은 작동가능하지 않은 요소(콘텐츠, 상태 정보, 등) 와 명백히 구별될 수 있도록 충분히 명확 해야 합니다.  요소가 실행 가능하다는 명확한 지시사항의 제공하는 것은 버튼나 링크와 같은 실행 가능한 요소를 가진 웹 및 기본 모바일 애플리케이션 특히, 실행 가능 요소가 시각적으로 감지되는 상호작용 모드(터치와 마우스 사용)와 관련이 있습니다.  
Interactive elements must also be detectable by users who rely on a programmatically determined accessible name (e.g. screen reader users).  
상호작용 요소들은 또한 프로그램적으로 결정된 접근 가능한 이름에 의존하는 사용자(예: 스크린 리더 사용자들)에 의해 탐지가능해야 합니다.(사용자가 알아채야합니다)  
Visual users who interact with content using touch or visual cursors (e.g. mice, touchpads, joysticks) should be able to clearly distinguish actionable elements such as links or buttons. Existing interface design conventions are aimed at indicating that these visual elements are actionable. The principle of redundant coding ensures that elements are indicated as actionable by more than one distinguishing visual feature.   
터치나 시각적인 커서들을(예: 마이크, 터치패드, 조이스틱) 사용해 콘텐츠와 상호작용하는 시각적인 사용자들이 링크나 버튼과 같은 실행가능한 요소들을 명확하게 구분할 수 있어야 합니다. 현재 인터페이스 디자인 규칙은 시각적인 요소가 실행 가능함을 나타내는 것을 목적으로 합니다. 요소중복 코딩의 원칙은 둘 이상의 구별되는 시각적인 기능을 실행 가능한 것으로 표시되도록 합니다.   
Following these conventions benefits all users, but especially users with vision impairments.  
이 규칙을 따르는 것은 모든 사용자에게 이점을 주는데 특히 시각장애인에게 그렇습니다.  
Visual features that can set an actionable element apart include shape, color, style, positioning, text label for an action, and conventional iconography.  
실행가능한 요소를 구분하여 설정할 수 있는 시각적 기능들은 모양,색,스타일,위치,실행에 대한 글자 라벨과 기존 아이콘 구조가 포함됩니다.   

Examples of distinguishing features:  
구별되는 특징의 예  

1. Conventional shape: Button shape (rounded corners, drop shadows), checkbox, select rectangle with arrow pointing downwards  
   기존의 모양: 버튼 모양 (둥근 모서리, 그림자), 체크박스, 화살표가 아래를 가리키는 직사각형 셀렉트  
2. Iconography: conventional visual icons (question mark, home icon, burger icon for menu, floppy disk for save, back arrow, etc)   
   아이콘구조: 기존의 시각적 아이콘 (물음표, 홈, 메뉴를 위한 햄버거 아이콘, 저장을 위한 플로피디스크, 뒤로 화살표, 등)  
3. Color offset: shape with different background color to distinguish the element from the page background, different text color    
   색 오프셋: 모양을 다른 배경색으로 지정하여 페이지 배경과 요소를 구분, 다른 글자 색   
4. Conventional style: Underlined text for links, color for links    
   기존의 스타일: 링크를 위한 글자 밑줄, 링크를 위한 색   
5. Conventional positioning: Commonly used position such as a top left position for back button (iOS), position of menu items within left-aligned lists in drop-down menus for navigation    
   기존의 위치: 좌측상단에 위치한 뒤로가기 버튼(iOS) 과 같은 공통적으로 사용된 위치, 드롭다운에 왼쪽정렬 리스트내 메뉴 위치    

The WCAG 2.0 success criteria do not directly address issue of clear visual indication that elements are actionable but are related to the following success criteria:  
WCAG 2.0 성공 기준은 실행할 수 있는 요소지만 다음 성공기준과 관련되어 있다는 명확한 시각적인 인지사항에 대한 이슈를 직접적으로 다루지는 않습니다.  

```
3.2.3 Consistent Navigation (Level AA)
3.2.4 Consistent Identification (Level AA)
```

**4.6 Provide instructions for custom touchscreen and device manipulation gestures**  
4.6 사용자 터치화면과 기기 조작 행위에 대한 지침 제공  

The ability to provide control via custom touchscreen and device manipulation gestures can help developers create efficient new interfaces.   
사용자 터치화면과 기기조작 동작을 통한 제어기능을 제공하면 개발자가 효율적인 새 인터페이스를 만들 수 있습니다.  
However, for many people, custom gestures can be a challenge to discover, perform and remember.  
그러나, 많은 사람들에게 사용자 동작은 발견 하고 수행하고 기억하는데 어려움이 될 수 있습니다.   
Therefore, instructions (e.g. overlays, tooltips, tutorials, etc.) should be provided to explain what gestures can be used to control a given interface and whether there are alternatives.   
그러므로, 인터페이스를 제어하는데 사용할 수 있는 동작과 대안이 있는지를 설명하기 위한 지시사항(예: 오버레이, 툴팁, 튜토리얼 등)이 제공되어야 합니다.   
To be effective, the instructions should, themselves, be easily discoverable and accessible.   
이 지침은 효과적으로 적용하려면 그 자체가 발견하기 쉬워야하고 접근하기 쉬워야합니다.  
The instructions should also be available anytime the user needs them, not just on first use, though on first use they may be made more apparent through highlighting or some other mechanism.  
첫 사용시 하이라이트나 다른 메커니즘을 통해 보다 명확하게 표시될 수 있지만, 지침은 첫번째 사용뿐 아니라 사용자가 그들이 필요할 때마다 언제나 이용가능해야합니다.  

These WCAG 2.0 success criteria are relevant to providing instructions for gestures:  
WCAG 2.0 성공기준은 동작 지침을 제공하는 것과 관련이 있습니다.  

```
3.3.2 Labels or Instructions (Level A)
3.3.5 Help (Level AAA)
```

5. Mobile accessibility considerations related primarily to Principle 4: Robust
---
5.원칙4: 견고성 와 주로 관계된 모바일 접근성

**5.1 Set the virtual keyboard to the type of data entry required**  
5.1 시각 키보드를 필요한 데이터 입력 유형으로 설정  

On some mobile devices, the standard keyboard can be customized in the device settings and additional custom keyboards can be installed.   
일부 모바일 기기에서, 키보드를 기기 설정에서 사용자 지정할 수 있고 추가적인 사용자 키보드를 설치할 수 있습니다.  
Some mobile devices also provide different virtual keyboards depending on the type of data entry.  
일부 모바일 기기는 또한 데이터 입력의 유형에 따라 다른 시각적인 키보드를 제공합니다.  
This can be set by the user or can be set to a specific keyboard.   
유저에 의해 설정하거나 특별한 키보드로 설정할 수 있습니다.  
For example, using the different HTML5 form field controls (see Method Editor API) on a website will show different keyboards automatically when users are entering in information into that field.   
예를 들어, 사용자가 해당 필드에 정보를 입력할 때 웹사이트에 다른 HTML5 양식 필드 컨트롤을 사용하면 다른 키보드가 자동으로 표시됩니다.  
Setting the type of keyboard helps prevent errors and ensures formats are correct but can be confusing for people who are using a screen reader when there are subtle changes in the keyboard.  
키보드의 유형을 설정하는 것은 오류를 방지하고 형식이 올바른지 확인하지만 키보드에 미묘한 변화가 있을 때 스크린 리더기를 사용하는 사람은 혼란스러울 수 있습니다.  

**5.2 Provide easy methods for data entry**  
5.2 데이터 입력을 위한 쉬운 수단을 제공  

Users can enter information on mobile devices in multiple ways such as on-screen keyboard, Bluetooth keyboard, touch, and speech.   
사용자들은 모바일 기기에 화면 키보드, 블루투스 키보드, 터치, 말하기와 같은 다양한 방법으로 정보를 입력할 수 있습니다.  
Text entry can be time-consuming and difficult in certain circumstances.   
글자 입력은 특정 상황에서는 시간이 많이 걸리고 어려울 수 있습니다.  
Reduce the amount of text entry needed by providing select menus, radio buttons, check boxes or by automatically entering known information (e.g. date, time, location).  
셀렉트 메뉴, 라디오 버튼,확인 란을 제공하거나 알려진 정보(예: 날짜,시간,위치)를 자동으로 입력해 글자 입력의 양을 줄입니다.  

**5.3 Support the characteristic properties of the platform**  
5.3 플랫폼의 특성 지원  

Mobile devices provide many features to help users with disabilities interact with content.   
모바일 기기는 장애가 있는 사용자가 콘텐츠와 상호작용하는데 도움이 되는 많은 기능을 제공합니다.  
These include platform characteristics such as zoom, larger fonts, and captions.   
이들은 확대, 큰 글자, 캡션과 같은 플랫폼 특성을 포함합니다.  
The features and functions available differ depending on the device and operating system version.   
사용가능한 특징과 기능은 운영체제버전과 기기에 따라 다릅니다.  
For example, most platforms have the ability to set large fonts, but not all applications honor it for all text. Also, some applications might increase font size but not wrap text, causing horizontal scrolling.  
예를 들어, 대부분의 플랫폼은 큰 글자로 세팅이 가능하지만 모든 애플리케이션이 모든 글자에 대해 지정할 수는 없습니다. 또한, 일부 애플리케이션은 글자 크기를 증가시키지만 글자를 줄바꿈 하지 않고 가로 스크롤을 유발할 수 있습니다.  

---


전문 문서다 보니 어려운 용어가 많아 상당수 구글번역기와 파파고의 도움을 받았습니다.
잘못번역된 부분은 언제든 알려주시면 감사하겠습니다.


참고 URL
------
[Mobile Accessibility: How WCAG 2.0 and Other W3C/WAI Guidelines Apply to Mobile](https://www.w3.org/TR/mobile-accessibility-mapping/)

