---
helpx_url: "https://helpx.adobe.com/kr/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/mask-generators/leather-wear.html"
breadcrumb-title: ''
description: 가죽 마모 노드를 사용하여 메쉬 곡률과 접촉점을 기반으로 가죽 표면에 마모 마스크를 생성합니다.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Mask Generators > Leather Wear
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 가죽 마모
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '252'
ht-degree: 1%

---


# 가죽 마모

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/leather-wear.png){width="128px"}

## 가죽 마모

**내부:** *메시 기반 생성기**/마스크 생성기*

**중간**

</td>
<td style="border: 0;" valign="top">

## 설명

베이킹된 맵 및 사용자 설정을 기반으로 흑백 마스크를 생성합니다. [Painter](https://support.allegorithmic.com/documentation/display/SPDOC/Substance+Painter)의 [스마트 마스크](https://support.allegorithmic.com/documentation/display/SPDOC/Smart+Materials+and+Masks)와 비슷합니다.

이 마스크는 가죽 패턴의 마모를 나타내며, 곡률을 기반으로 가장자리가 더 마모됩니다. 기능상 [섬유 유리 Edge Wear](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/mesh-based-generators/mask-generators/fiber-glass-edge-wear/fiber-glass-edge-wear.md)과(와) 비슷하며 대부분 동일한 매개 변수를 사용합니다.

## 매개변수

### 입력

* **곡률**: *회색 음영 입력*\
  가장자리 배치에 사용되는 베이킹된 맵. 필수!
* **주변 오클루전**: *회색 음영 입력*\
  베이킹된 맵은 특정 영역을 폐쇄하는 데 사용되었습니다. 권장되지만 필수는 아닙니다.
* **그런지 입력**: *회색 음영 입력*\
  &quot;사용자 지정 그런지 사용&quot; 매개 변수를 통해 전환할 수 있는 선택적 그런지 맵 입력 슬롯입니다.
* **마스크(선택 사항)**: *회색 음영 입력*\
  노드의 효과를 마스킹하는 데 사용되는 마스크 슬롯입니다.

### 매개변수

* **마모 수준**: *0.0 - 1.0*&#x200B;전체적으로 마모 수준을 설정하여 점차적으로 드러나도록 합니다.
* **마모 대비**: *0.0 - 1.0*&#x200B;효과의 대비를 설정합니다.
* **그런지 양**: *0.0 - 1.0*&#x200B;가장자리 간에 혼합할 그런지(기본 가죽 패턴)의 양을 설정합니다.
* **주변 오클루전 마스크**: *0.0 - 1.0* AO가 마모 효과를 가리는 정도를 설정합니다.
* **곡률 두께**: *0.0 - 1.0*&#x200B;곡선의 가장자리가 최종 결과에 영향을 주는 정도를 설정합니다. 0으로 설정해도 곡률 맵이 필요합니다.
* **사용자 지정 그런지 사용**: *False/True*&#x200B;기본 제공 가죽 패턴을 재정의할 수 있습니다. 대신 사용자 정의 입력 슬롯을 사용합니다.

## 예제 이미지

![](../../../../../../assets/leather-wear-ex.gif)

</td>
</tr>
</table>
