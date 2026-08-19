---
helpx_url: "https://helpx.adobe.com/kr/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/utilities-mesh-based-generators/material-mesh-data-blender.html"
breadcrumb-title: ''
description: 재질 메시 데이터 블렌더 노드를 사용하여 여러 재질 영역 간에 부드러운 전환을 만들기 위해 재질 메시 데이터를 블렌딩합니다.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Utilities (Mesh Based Generators) > Material Mesh Data Blender
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 재질 메쉬 데이터 블렌더
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '578'
ht-degree: 0%

---


# 재질 메쉬 데이터 블렌더

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/material-mesh-data-blender.png){width="128px"}

## 재질 메쉬 데이터 블렌더

**내부:** *메시 기반 생성기**/유틸리티*

**복합**

</td>
<td style="border: 0;" valign="top">

## 설명

이 노드는 구운 데이터를 기반으로 세부 사항을 훨씬 더 쉽게 추가할 수 있도록 하기 위한 것입니다. 입력 베이킹된 맵을 기반으로 입력 전체 재질을 수정할 수 있는 슬라이더가 많이 제공됩니다. 사용할 수 있는 옵션이 많으므로 다양하게 실험해 보십시오.

곡률 또는 기타 맵을 기반으로 가장자리 강조 효과를 추가하거나, 일부 AO에서 확산/기본 색상으로 혼합하거나, 곡률 및/또는 AO를 기반으로 Specular 오클루전을 추가하는 등의 작업을 수행하는 데 유용합니다.

## 매개변수

### 입력

* **전체 재질 입력(&quot;재질&quot; 그룹):** 재질 맵의 전체 세트.\
  이 노드에 의해 수정된 다음 출력으로 다시 반환됩니다.
* **주변 오클루전**: *회색 음영 입력*\
  내부 효과 및 마스크에 사용되는 베이킹된 맵.
* **곡률**: *회색 음영 입력*\
  내부 효과 및 마스크에 사용되는 베이킹된 맵.
* **Height**: *회색 음영 입력*
* **표준**: *색상 입력*
* **꼭지점 색상**: *색상 입력*
* **월드 스페이스 표준**: *색상 입력*

### 매개변수

* **채널**
  * 예를 들어 [금속]/[거칠음] 대신 [Specular/광택] 맵을 사용하는 경우 이 그룹에서 재질 채널을 켜거나 끌 수 있습니다. 아래 매개 변수의 가용성에 영향을 줍니다.
* **베이킹된 맵**
  * 계산에 나열된 베이킹된 맵을 사용할지 여부를 지정합니다. 아래 매개 변수의 가용성에 영향을 줍니다.
* **확산 AO**: *0.0 - 1.0*&#x200B;확산에 혼합할 주변 오클루전 양.
* **선명한 가장자리 확산**: 0.0 - 1.0\
  확산에 혼합할 곡률 맵의 양입니다.
* **꼭지점 색상에서 확산 색상**: 0.0 - 1.0\
  확산에 혼합할 꼭지점 색상 베이크의 양입니다.
* **사전 조명 확산**: 0.0 - 1.0\
  월드 스페이스 표준을 기반으로 한 (가짜) 사전 조명의 양입니다.
* **만화 조명 균형 확산**: 0.0 - 1.0\
  [확산]에 대한 사실적인 조명과 만화적인 조명 간의 변화를 살펴봅니다.
* **만화 확산 사전 조명 레이어**: 0 - 10\
  만화 같은 조명 계산의 모양을 제어합니다.
* **카툰 윤곽선 확산**: 0.0 - 1.0\
  만화 같은 조명 계산의 모양을 제어합니다.
* **기본 색상 AO**: 0.0 - 1.0\
  기준 색상에 혼합할 앰비언트 오클루전 양입니다.
* **기본 색 선명한 가장자리**: 0.0 - 1.0\
  기준 색상에 혼합할 곡률 맵의 양입니다.
* **꼭지점 색상의 기준 색상**: 0.0 - 1.0\
  기준 색상에 혼합할 꼭지점 색상 베이크의 양입니다.
* **표준 재질 강도**: 0.0 - 1.0\
  구워진(탄젠트) 표준 맵의 혼합 강도입니다.
* **반사 AO**: 0.0 - 1.0\
  Specular에서 AO의 혼합 강도입니다.
* **Specular 밝은 선명한 가장자리**: 0.0 - 1.0\
  Specular 곡률 혼합 강도입니다.
* **Specular 카툰 윤곽선**: 0.0 - 1.0\
  곡률 기반의 카툰 Specular 가장자리 윤곽선 효과 혼합 강도입니다.
* **광택 어두운 선명한 가장자리**: 0.0 - 1.0\
  광택이 있는 곡률 혼합 강도입니다.
* **거칠음 밝고 선명한 가장자리**: 0.0 - 1.0\
  거칠기 곡선의 혼합 강도입니다.
* **거칠음 카툰 윤곽선**: 0.0 - 1.0\
  곡률 기반의 카툰 거칠기 가장자리 윤곽선 효과 혼합 강도입니다.
* **금속 밝은 날카로운 가장자리**: 0.0 - 1.0\
  금속에 있는 곡률의 혼합 강도입니다.
* **금속성 카툰 윤곽선**: 0.0 - 1.0\
  곡률 기반의 카툰 금속 가장자리 윤곽선 효과의 혼합 강도입니다.
* **AO 재질 강도**: 0.0 - 1.0\
  베이킹된 맵 AO의 강도와 재질 생성 AO의 혼합(두 AO 맵을 어느 정도까지 결합할지).
* **Height 재질 강도**: 0.0 - 1.0\
  베이킹된 맵 Height과 재질 생성 Height의 혼합 강도, 두 Heightmap을 어느 정도까지 결합할지 지정합니다.
* **Height 재질 혼합 유형**: 보강, 보간\
  두 높이 맵을 결합하기 위한 혼합 모드입니다.

## 예제 이미지

![](../../../../../../assets/blenddata-ex.gif)

</td>
</tr>
</table>
