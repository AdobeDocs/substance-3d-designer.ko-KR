---
helpx_url: "https://helpx.adobe.com/kr/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/mask-generators/selective-dirt.html"
breadcrumb-title: ''
description: '[선택 Dirt] 노드를 사용하여 사실적인 풍화를 위해 메시 형상을 기반으로 선택 Dirt 누적 마스크를 생성합니다.'
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Mask Generators > Selective Dirt
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 선택 Dirt
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '171'
ht-degree: 5%

---


# 선택 Dirt

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/selective-dirt.png){width="128px"}

## 선택 Dirt

**내부:** *메시 기반 생성기**/마스크 생성기*

**단순**

</td>
<td style="border: 0;" valign="top">

## 설명

베이킹된 맵 및 사용자 설정을 기반으로 흑백 마스크를 생성합니다. [Painter](https://support.allegorithmic.com/documentation/display/SPDOC/Substance+Painter)의 [스마트 마스크](https://support.allegorithmic.com/documentation/display/SPDOC/Smart+Materials+and+Masks)와 비슷합니다.

이 [Substance 3D Designer](https://www.adobe.com/kr/products/substance3d-designer.html) 마스크는 볼록 가장자리에 대한 간단한 Dirt 효과를 나타냅니다.

## 매개변수

### 입력

* **곡률**: *회색 음영 입력*\
  내부 효과 및 마스크에 사용되는 베이킹된 맵.
* **변형 마스크**: *회색 음영 입력*\
  선택적 변형 맵은 매개 변수를 통해 활성화할 수 있습니다.
* **마스크(선택 사항)**: *회색 음영 입력*\
  노드의 효과를 마스킹하는 데 사용되는 마스크 슬롯입니다.

### 매개변수

* **수준**: *0.0 - 1.0*\
  효과의 전체 수준을 점진적으로 표시합니다.
* **대비**: *0.0 - 1.0*\
  결과의 대비를 조정합니다.
* **변형**: *0.0 - 1.0*&#x200B;효과에 혼합할 변형/그런지 양을 설정합니다.
* **변형 마스크 재정의**: *False/True*&#x200B;사용자 지정 입력 슬롯으로 변형을 재정의할 수 있습니다.

## 예제 이미지

![](../../../../../../assets/selective-dirt-ex.gif)

</td>
</tr>
</table>
