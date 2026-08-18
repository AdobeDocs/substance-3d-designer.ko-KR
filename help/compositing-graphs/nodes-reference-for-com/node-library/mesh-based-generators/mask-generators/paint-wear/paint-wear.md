---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/mask-generators/paint-wear.html"
breadcrumb-title: ''
description: 페인트 마모 노드를 사용하면 메시 형상을 기반으로 사실적인 페인트 조각 효과를 만들 수 있는 페인트 마모 마스크를 생성할 수 있습니다.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Mask Generators > Paint Wear
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 페인트 마모
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '203'
ht-degree: 1%

---


# 페인트 마모

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/paint-wear.png){width="128px"}

## 페인트 마모

**내부:** *메시 기반 생성기**/마스크 생성기*

**중간**

</td>
<td style="border: 0;" valign="top">

## 설명

베이킹된 맵 및 사용자 설정을 기반으로 흑백 마스크를 생성합니다. [Painter](https://support.allegorithmic.com/documentation/display/SPDOC/Substance+Painter)의 [스마트 마스크](https://support.allegorithmic.com/documentation/display/SPDOC/Smart+Materials+and+Masks)와 비슷합니다.

이 마스크는 페인트가 벗겨져 가장자리가 닳아 없어지는 것을 나타냅니다.

## 매개변수

### 입력

* **주변 오클루전**: *회색 음영 입력*\
  내부 효과 및 마스크에 사용되는 베이킹된 맵.
* **곡률**: *회색 음영 입력*\
  내부 효과 및 마스크에 사용되는 베이킹된 맵.
* **변형 마스크**: *회색 음영 입력*\
  노드의 효과를 마스킹하는 데 사용되는 마스크 슬롯입니다.
* **마스크(선택 사항)**: *회색 음영 입력*\
  노드의 효과를 마스킹하는 데 사용되는 마스크 슬롯입니다.

### 매개변수

* **수준**: *0.0 - 1.0*\
  페인트 마모의 전체 양을 설정하여 점진적으로 표시합니다.
* **대비**: *0.0 - 1.0*\
  결과의 대비를 조정합니다.
* **오클루전**: *0.0 - 1.0*&#x200B;구워진 AO가 어두운 영역에서 마모되는 것을 방지하는 데 미치는 효과의 양을 설정합니다.
* **반경**: *0.0 - 2.0*&#x200B;볼록 가장자리에서 치핑 효과가 확산되는 거리를 설정합니다.
* **변형**: *0.0 - 1.0*&#x200B;효과에 혼합할 변형 양(그런지)을 설정합니다.
* **변형 마스크 재정의**: *False/True*&#x200B;사용자 지정 변형(그런지) 맵 입력 슬롯을 사용합니다.

## 예제 이미지

![](../../../../../../assets/paint-wear-ex.gif)

</td>
</tr>
</table>
