---
helpx_url: "https://helpx.adobe.com/kr/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/mask-generators/edge-dirt.html"
breadcrumb-title: ''
description: '[가장자리] Dirt 노드를 사용하면 메시 가장자리에 Dirt 누적 마스크를 생성하여 사실적인 가장자리 풍화 효과를 만들 수 있습니다.'
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Mask Generators > Edge Dirt
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 가장자리 Dirt
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '164'
ht-degree: 2%

---


# 가장자리 Dirt

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/edge-dirt.png){width="128px"}

## 가장자리 Dirt

**내부:** *메시 기반 생성기**/마스크 생성기*

**단순**

</td>
<td style="border: 0;" valign="top">

## 설명

베이킹된 맵 및 사용자 설정을 기반으로 흑백 마스크를 생성합니다. [Painter](https://support.allegorithmic.com/documentation/display/SPDOC/Substance+Painter)의 [스마트 마스크](https://support.allegorithmic.com/documentation/display/SPDOC/Smart+Materials+and+Masks)와 비슷합니다.

이 마스크는 곡률 맵만을 기준으로 가장자리 주변에 누적되는 Dirt 효과를 나타냅니다.

## 매개변수

### 입력

* **곡률**: *회색 음영 입력*\
  효과 배치에 사용되는 베이킹된 맵. 필수!
* **변형 마스크**: *회색 음영 입력*\
  노드의 효과를 마스킹하는 데 사용되는 마스크 슬롯으로, 재정의 매개 변수가 활성화된 경우에만 사용됩니다.
* **마스크(선택 사항)**: *회색 음영 입력*\
  노드의 효과를 마스킹하는 데 사용되는 마스크 슬롯입니다.

### 매개변수

* **수준**: *0.0 - 1.0*\
  Dirt 양을 설정합니다.
* **대비**: *0.0 - 1.0*\
  결과의 대비를 조정합니다.
* **변형**: *0.0 - 1.0*&#x200B;대규모 마스크/분리 발생 정도를 혼합합니다.
* **변형 마스크 재정의**: *False/True*

## 예제 이미지

![](../../../../../../assets/edge-dirt-ex.gif)

</td>
</tr>
</table>
