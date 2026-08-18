---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/mask-generators/edge-notch.html"
breadcrumb-title: ''
description: 가장자리 노치 노드를 사용하여 메시 가장자리에 노치 패턴을 생성하여 사실적인 가장자리 손상과 들여쓰기 효과를 만듭니다.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Mask Generators > Edge Notch
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 가장자리 노치
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '140'
ht-degree: 2%

---


# 가장자리 노치

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/edge-notch.png){width="128px"}

## 가장자리 노치

**내부:** *메시 기반 생성기**/마스크 생성기*

**단순**

</td>
<td style="border: 0;" valign="top">

## 설명

베이킹된 맵 및 사용자 설정을 기반으로 흑백 마스크를 생성합니다. [Painter](https://support.allegorithmic.com/documentation/display/SPDOC/Substance+Painter)의 [스마트 마스크](https://support.allegorithmic.com/documentation/display/SPDOC/Smart+Materials+and+Masks)와 비슷합니다.

이 마스크는 높은 주파수 노이즈로 깨진 솟아오른 가장자리를 위한 간단한 마스크를 나타냅니다. 자세한 옵션은 [Edge Dirt](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/mesh-based-generators/mask-generators/edge-dirt/edge-dirt.md) 또는 [Edge 손상](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/mesh-based-generators/mask-generators/edge-damages/edge-damages.md)을 참조하십시오.

## 입력

* **곡률**: *회색 음영 입력*\
  가장자리를 강조하는 데 사용되는 베이킹된 맵. 필수!
* **마스크(선택 사항)**: *회색 음영 입력*\
  노드의 효과를 마스킹하는 데 사용되는 마스크 슬롯입니다.

## 매개변수

* **수준**: *0.0 - 1.0*\
  가장자리 노치 효과의 레벨을 설정합니다.
* **대비**: *0.0 - 1.0*\
  결과의 대비를 조정합니다.

## 예제 이미지

![](../../../../../../assets/edge-notch-ex.gif)

</td>
</tr>
</table>
