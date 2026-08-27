---
helpx_url: "https://helpx.adobe.com/kr/substance-3d-designer/technical-issues/baking-issues.html"
breadcrumb-title: ''
description: Substance 3D Designer의 텍스처 구이와 관련된 기술적 문제에 대한 문제 해결 단계를 찾아보십시오.
helpx_creative_field: ""
helpx_description: Designer > Technical issues > Baking issues
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 베이킹 문제
user-guide-description: ''
user-guide-title: ''
source-git-commit: 5b9c9d12e2ccd76f75ec2a74815f9c68c43c06a2
workflow-type: tm+mt
source-wordcount: '216'
ht-degree: 0%

---


# 베이킹 문제

이 페이지에는 Substance 3D Designer의 [텍스처 굽기](../../bakers/bakers.md)와 관련된 기술적 문제가 나열되어 있으며 각각에 대한 문제 해결 단계를 제공합니다.

## 이 페이지의 내용

&#39;이름별 일치&#39;가 작동하지 않음

## &#39;이름별 일치&#39;가 작동하지 않음

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

<b>![(오류)](../../assets/error.svg) 문제</b>

&#39;Match&#39; 옵션을 &#39;By mesh name&#39;으로 설정하면 일치하는 내용이 적용되지 않거나 모든 장면 개체에서 일관되게 적용되지 않습니다.

<b>![(틱)](../../assets/check.svg) 권장 단계</b>

Designer 버전 14.1 이하에서 하위 폴리 및 상위 폴리 개체는 해당 *상위* 개체의 이름을 사용하여 일치했습니다. 대부분의 경우 상위 개체가 변형됩니다.

Designer 15.0부터 *기하 도형* 개체의 이름이 직접 사용됩니다.

</td>
<td style="border: 0;" valign="top">

![장면 트리에 있는 기하 도형 개체와 그 부모](../../assets/sceneTree_objectsName.png "장면 트리에 있는 기하 도체와 그 부모"){zoomable="yes"}

</td>
</tr>
</table>

두 가지 경로를 사용하여 원하는 결과를 얻을 수 있습니다.

* 형상 개체의 이름을 조정하여 일치하는 이름을 적용합니다.
* [프로젝트] 설정에서 [&#39;이름 필터링 모드&#39; 옵션](../../interface/preferences-window/project-settings/project-settings.md)을(를) 조정하여 동작 또는 이전 Designer 버전으로 되돌립니다.
  1. 편집 > 환경 설정 > 프로젝트로 이동합니다.
  1. 목록에서 마지막 프로젝트 파일 선택
  1. 프로젝트 파일 목록 아래에서 &#39;베이커&#39; 탭을 선택합니다
  1. &#39;이름 필터링 모드&#39;를 &#39;부모 이름(레거시)&#39;으로 설정
