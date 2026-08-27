---
helpx_url: "https://helpx.adobe.com/kr/substance-3d-designer/scripting/plugin-search-paths.html"
breadcrumb-title: ''
description: Substance 3D Designer에서 플러그인 검색 경로를 구성하여 Python 플러그인이 위치한 위치를 지정합니다.
helpx_creative_field: ""
helpx_description: Designer > Scripting > Plugin search paths
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 플러그인 검색 경로
user-guide-description: ''
user-guide-title: ''
source-git-commit: 5b9c9d12e2ccd76f75ec2a74815f9c68c43c06a2
workflow-type: tm+mt
source-wordcount: '133'
ht-degree: 0%

---


# 플러그인 검색 경로

Designer은 특정 디렉터리에서 플러그인을 찾습니다(예: 검색 경로). 이 페이지에서는 이러한 경로를 구성하는 방법에 대해 설명합니다.

사용자는 소프트웨어 환경 설정에서 수동으로 *사용자 지정 디렉터리를 추가*&#x200B;하거나 환경 변수를 사용하여 지정할 수 있습니다.

## 수동으로 플러그인 검색 경로 추가

1. <b>편집 > 기본 설정...</b>(으)로 이동
1. <b>프로젝트</b> 범주 선택
1. 편집할 <b>프로젝트 파일</b> 선택
1. <b>Python</b> 탭에서 *<b>+</b>*버튼을 클릭하여 플러그인이 포함된 디렉터리를 추가합니다
1. <b>확인</b>을 클릭하여 유효성 검사

![Python 플러그인 검색 경로 프로젝트 설정](../../assets/image-70.png "Python 플러그인 검색 경로 프로젝트 설정")

## 환경 변수 사용

응용 프로그램은 <b>SBS\_DESIGNER\_PYTHON\_PATH </b>환경 변수를 사용하여 지정한 모든 경로에서 플러그인을 찾습니다.
