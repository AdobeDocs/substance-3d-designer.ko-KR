---
helpx_url: "https://helpx.adobe.com/kr/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/weathering/rock-weathering.html"
breadcrumb-title: ''
description: 암석 풍화 노드를 사용하여 사실적인 침식 효과를 위해 메쉬 형상을 기반으로 암석 표면에 풍화 패턴을 생성합니다.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Weathering > Rock Weathering
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 암석 풍화
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '271'
ht-degree: 1%

---


# 암석 풍화

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/rock-weathering.png){width="128px"}

## 암석 풍화

**내부:** *메쉬 기반 생성기**/풍화*

**복합**

</td>
<td style="border: 0;" valign="top">

## 설명

## 매개변수

### 입력

* **주변 오클루전**: *회색 음영 입력*\
  내부 효과 및 마스크에 사용되는 베이킹된 맵.
* **곡률**: *회색 음영 입력*\
  내부 효과 및 마스크에 사용되는 베이킹된 맵.
* **일반 WS**: *색상 입력*\
  내부 효과 및 마스크에 사용되는 Baked World Space Normalmap
* **마스크** : *회색 음영 입력*\
  노드의 효과를 마스킹하는 데 사용되는 마스크 슬롯입니다. &quot;마스크&quot; 매개 변수로 전환할 수 있습니다.

### 매개변수

* **채널**
  * 예를 들어 [금속]/[거칠음] 대신 [Specular/광택] 맵을 사용하는 경우 이 그룹에서 재질 채널을 켜거나 끌 수 있습니다.
* **고급**
  * **표준 형식**: *DirectX, OpenGL*\
    서로 다른 표준 맵 포맷 사이를 전환합니다(녹색 채널을 반전합니다).
  * **마스크**: *False/True*\
    마스크 맵 사용을 설정하거나 해제합니다.
* **효과**
  * **Dust**: *0.0 - 1.0*
  * **더러움**: *0.0 - 1.0*
  * **가장자리 착용**: *0.0 - 1.0*
  * **사용된 바위**: *0.0 - 1.0*
  * **균열 크기**: *1.0 - 60.0*
  * **균열 강도**: *0.0 - 1.0*
  * **나이**: *0.0 - 1.0*
  * **연령 임계값**: *0.0 - 1.0*
  * **선명한 가장자리 Scratches 크기**: *1.0 - 32.0*
  * **선명한 가장자리 Scratches 뒤틀기 강도**: *0.0 - 1.0*
  * **사용된 바위 채도 감소**: *0.0 - 1.0*
  * **사용된 바위 밝기**: *0.0 - 1.0*
* **혼합**
  * **확산 강도**: *0.0 - 1.0*\
    확산 영역의 혼합 강도입니다.
  * **기본 색상 강도**: *0.0 - 1.0*\
    기본 색상의 혼합 강도입니다.
  * **표준 강도**: *0.0 - 64.0*\
    표준의 혼합 강도입니다.
  * **Specular 강도**: *0.0 - 1.0*\
    Specular의 혼합 강도입니다.
  * **광택 강도**: *0.0 - 1.0*\
    광택의 혼합 강도입니다.
  * **거칠음 강도**: *0.0 - 1.0*\
    거칠기의 혼합 강도입니다.
  * **주변 오클루전 강도**: *0.0 - 1.0*\
    주변 오클루전의 혼합 강도입니다.
  * **Height 강도**: *0.0 - 1.0*\
    Height의 혼합 강도입니다.

## 예제 이미지

![](../../../../../../assets/rock-ex.gif)

</td>
</tr>
</table>
