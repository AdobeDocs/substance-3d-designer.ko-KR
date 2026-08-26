---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/pipeline-and-project-configuration/environment-variables.html"
breadcrumb-title: ''
description: Substance 3D Designer에서 환경 변수를 사용하여 경로 및 시스템 설정을 구성하는 방법을 알아봅니다.
helpx_creative_field: ""
helpx_description: Designer > Pipeline and Project Configuration > Environment variables
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 환경 변수
user-guide-description: ''
user-guide-title: ''
source-git-commit: 5b9c9d12e2ccd76f75ec2a74815f9c68c43c06a2
workflow-type: tm+mt
source-wordcount: '145'
ht-degree: 3%

---


# 환경 변수

이 페이지에는 애플리케이션의 기본 동작을 재정의하는 데 사용할 수 있는 환경 변수가 나열됩니다.

| 변수 | 설명 |
| --- | --- |
| **SBS\_DESIGNER\_PYTHON\_PATH** | Designer에서 [Python 플러그인](../../scripting/plugin-basics/plugin-basics.md)을 로드할 경로입니다. |
| **SUBSTANCE\_DESIGNER\_라이선스** | Designer에서 사용해야 하는 라이선스 파일(*license.key*)의 위치   Designer [활성화 마법사](../../getting-started/activation-and-licenses/activation-and-licenses.md)에 설정된 경로를 재정의합니다.  **참고:** 이전 버전에서는 대체 변수 이름을 사용해야 할 수 있습니다.<ul data-preserve-html="true"><li data-preserve-html="true"><strong>SUBSTANCE_DESIGNER_6_LICENSE</strong></li><li data-preserve-html="true"><strong>SUBSTANCE_DESIGNER_5_LICENSE</strong></li></ul> |
| <b>OCIO</b> | OpenColorIO [색상 관리](../../color-management/color-management.md)를 사용할 때 사용해야 하는 OCIO 구성 파일의 경로입니다.   [프로젝트 설정](../../interface/preferences-window/project-settings/project-settings.md)의 Designer 색상 관리 설정에 설정된 경로를 재정의합니다. |
| **ALLEGO\_LICENSE\_IDLE\_DELAY** | 다중 사용자 구성의 경우 라이선스 시트를 릴리스하기 전 시간(초) 기본값은 7200초(2시간)입니다. |
