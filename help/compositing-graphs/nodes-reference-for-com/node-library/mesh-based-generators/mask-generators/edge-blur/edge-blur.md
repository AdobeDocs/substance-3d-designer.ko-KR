---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/mask-generators/edge-blur.html"
breadcrumb-title: ''
description: 가장자리 흐림 효과 노드를 사용하면 가장자리 마스크를 흐리게 하여 부드러운 전환과 부드러운 가장자리 기반 풍화 효과를 만들 수 있습니다.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Mask Generators > Edge Blur
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 가장자리 흐림 효과
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '145'
ht-degree: 2%

---


# 가장자리 흐림 효과

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/edge-blur.png){width="128px"}

## 가장자리 흐림 효과

**내부:** *메시 기반 생성기**/마스크 생성기*

**단순**

</td>
<td style="border: 0;" valign="top">

## 설명

베이킹된 맵 및 사용자 설정을 기반으로 흑백 마스크를 생성합니다. [Painter](https://support.allegorithmic.com/documentation/display/SPDOC/Substance+Painter)의 [스마트 마스크](https://support.allegorithmic.com/documentation/display/SPDOC/Smart+Materials+and+Masks)와 비슷합니다.

이 마스크는 구워진 곡률 맵을 기반으로 가장자리를 강조합니다. 이것은 보다 간단한 마스크 생성기 중 하나입니다.

## 매개변수

### 입력

* **곡률**: *회색 음영 입력*\
  효과의 기반이 되는 데 사용되는 베이킹된 맵.
* **마스크(선택 사항)**: *회색 음영 입력*\
  노드의 효과를 마스킹하는 데 사용되는 마스크 슬롯입니다.

### 매개변수

* **수준**: *0.0 - 1.0*\
  가장자리 강조표시의 양을 설정합니다.
* **대비**: *0.0 - 1.0*\
  결과의 대비를 조정합니다.
* **흐림 반경**: *0.0 - 8.0*&#x200B;강조 표시된 가장자리의 흐림 정도를 설정합니다.

## 예제 이미지

![](../../../../../../assets/edge-blur-ex.gif)

</td>
</tr>
</table>
