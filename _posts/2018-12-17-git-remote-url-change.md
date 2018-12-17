---
title: "[Git] Git remove 변경하기(원격 저장소 URL 변경하기)"
date: 2018-12-17 18:15:00 -0400
categories: Git
---

Git remove 변경하기(원격 저장소 URL 변경하기)
=============

용도
----
작성한 코드를 A remote 에 올리고, B remote 에도 올리고 싶을때 사용했습니다


코드
----
코드는 간단합니다!

``
git remote -v 
(원격저장소 URL 체크)
``

``
git remote set-url origin URL
(원격저장소 URL 변경)
``

``
git remote -v 
(설정한 원격저장소 URL 체크)
``

``
git push
(설정된 원격저장소로 Push)
``

