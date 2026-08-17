---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/mask-generators/edge-wear.html"
breadcrumb-title: ''
description: Edge Wear 노드를 사용하여 메시 가장자리에 마모 마스크를 생성하여 사실적인 가장자리 손상 및 풍화 효과를 생성합니다.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Mask Generators > Edge Wear
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Edge Wear
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '202'
ht-degree: 1%

---


# Edge Wear

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/edge-wear.png){width="128px"}

## Edge Wear

**내부:** *메시 기반 생성기**/마스크 생성기*

**중간**

</td>
<td style="border: 0;" valign="top">

## 설명

베이킹된 맵 및 사용자 설정을 기반으로 흑백 마스크를 생성합니다. [Painter](https://support.allegorithmic.com/documentation/display/SPDOC/Substance+Painter)의 [스마트 마스크](https://support.allegorithmic.com/documentation/display/SPDOC/Smart+Materials+and+Masks)와 비슷합니다.

이 노드는 개체 가장자리의 마모를 나타냅니다. 그것은 꽤 많은 매개 변수를 가지고 있지만, 사용하기 쉽지는 않습니다 : 우리는 당신이 놀고있는 것을 느낄 것을 권장합니다. 이 노드는 매우 강력하지만 사용자 정의 재정의 마스크는 사용할 수 없습니다.

## 매개변수

### 입력

* **곡률**: *회색 음영 입력*\
  내부 효과 및 마스크에 사용되는 베이킹된 맵
* **마스크(선택 사항)**: *회색 음영 입력*\
  노드의 효과를 마스킹하는 데 사용되는 마스크 슬롯입니다.

### 매개변수

* **수준**: *0.0 - 1.0*\
  효과의 총 스프레드를 설정합니다.
* **대비**: *0.0 - 1.0*\
  결과의 대비를 조정합니다.
* **임계값**: *0.0 - 1.0*&#x200B;수준과 비슷하게 효과의 총 분배를 설정합니다.
* **가장자리 폭**: *0.0 - 1.0*&#x200B;강조 효과의 전체 두께를 설정합니다. 줄여 더 반짝이게 합니다.
* **장애**: *0.0 - 1.0*\
  Smoothness을 분할하기 위해 혼합할 노이즈의 양을 설정합니다.

## 예제 이미지

![](../../../../../../assets/edge-wear-ex.gif)

</td>
</tr>
</table>
