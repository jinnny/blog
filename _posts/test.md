---
title: "[CSS] Intellij를 이용한 Sass auto compile"
date: 2019-05-12 16:00:00 -0400
categories: Intellij CSS Sass
tags: Sass 전처리기
---

Intellij를 이용해 Sass 를 자동 컴파일 하기
======

다양한 에디터를 사용해봤지만 제게 가장 맞는 에디터는 Intellij 였습니다.  
HTML 파일만 작업하는게 아니라 jsp, php,vueJS 등의 환경에서도 작업했기 때문이었습니다.

제가 주로 사용하는 Intellij에는 Sass를 통해 실시간 watch를 하고 이를 통해 css 파일을 만들어주는 편리한 플러그인이 있었으며,
오늘은 이것을 사용해 Sass 자동 컴파일에 대해 포스팅하고자 합니다.

소개드릴 플러그인은 **File Watchers** 입니다.  
이 플러그인은 Sass뿐 아니라 Less, Stylus 등 전처리기를 추가해 watch가 가능합니다.

이것을 이용해 Ruby Sass를 세팅해봅시다.
(사실 Ruby Sass는 2019년 3월 26일 날짜로 지원이 중단되었음..)


------
1\. Ruby 설치하기   
(MAC의 경우 이미 설치되어 있음)  
https://rubyinstaller.org/downloads/  
**Ruby+Devkit 2.5.5-1 (x64)** 설치

2\. Sass 설치하기  
```
gem install sass

*gem (루비의 패키지 관리 프로그램)
```

3\. file watchers 설치하기  
   1. Intellij의 'intellij - Preference - Plugin' 켜고 file watchers 검색  
     ![image](/blog/assets/images/intellij_sass_2.png)
   2. restart후 'intellij - Preference - Tools - File Watchers' 접속 후 하단 + 버튼 클릭후 File type 선택(이 경우 Compass Sass 선택)    
     ![image](/blog/assets/images/intellij_sass_3.png)
   3. Sass가 잘 설치되었다면 Program 경로가 자동으로 지정되어있음. 지정되어 있지 않은경우 설치 장소를 찾아 sass 를 지정해야함.
   Arguments는 Compile 될 당시 설정값을 세팅하는 곳.  
     ![image](/blog/assets/images/intellij_sass_4.png)
   4. 컴파일을 하게되면 souremap이 생기는데 불편해서 생기지 않도록 처리, 캐시가 없도록 처리, style 은 minify 된 형식으로 출력, 주석의 경우 UTF-8 속성 추가  
     ![image](/blog/assets/images/intellij_sass_5.png)
```
--sourcemap=none
--no-cache
--style
compressed
-E
UTF-8
```

해당 속성들을 세팅한뒤 OK 버튼을 누르시면 적용이 완료됩니다.
그러면 해당 file type를 watch 하게 됨으로 변경이 생길때마다 컴파일을 진행합니다.
처리과정은 아래 처리바에서 확인하실 수 있으며, 문법이 잘못된 경우 하단과 같이 상세히 알려줍니다.  
![image](/blog/assets/images/intellij_sass_6.png)

어느 라인의 무엇이 어떻게 잘못사용되었는지 알려주므로 편합니다.
참고로 위와 같은 상황이 일어나면 css 파일도 깨져서? 출력하기 때문에 실수하는 일이 거의 없게 도와줍니다.


참고 URL
------
[Install Sass](https://sass-lang.com/install)  
[Ruby Installer](https://rubyinstaller.org/downloads/)