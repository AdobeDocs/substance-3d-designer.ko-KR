---
helpx_url: "https://helpx.adobe.com/kr/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/utilities-mesh-based-generators/material-selector.html"
breadcrumb-title: ''
description: 재질 선택기 노드를 사용하여 다중 재질 텍스처 효과를 만들기 위해 메시 데이터를 기준으로 재질을 선택합니다.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Utilities (Mesh Based Generators) > Material Selector
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 재질 선택기
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '183'
ht-degree: 1%

---


# 재질 선택기

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/material-selector.png){width="128px"}

## 재질 선택기

**내부:** *메시 기반 생성기**/유틸리티*

**중간**

</td>
<td style="border: 0;" valign="top">

## 설명

전체 색상 ID 맵을 2진 흑백 마스크로 변환합니다. 서로 다른 색상을 혼합하고 하나의 마스크로 결합할 수 있습니다.

이 기능은 [다중 재질 혼합](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/blending-material/multi-material-blend/multi-material-blend.md)을 사용하지 않고 마스크를 수동으로 사용하거나 다른 위치에서 동일한 마스크를 수동으로 사용하려는 경우에 유용합니다.

## 매개변수

* **재질**: 1 - 16\
  결합을 사용할 수 있는 재질 수를 설정합니다.
* **재질 #1-16** 사용: False/True\
  색상을 혼합하고 결합하여 최종 출력 마스크를 만듭니다. 원하는 수의 색상을 결합할 수 있도록 활성화할 수 있습니다.
* **재질 #1-16**: (색상 값)\
  흑백으로 변환될 재질 색상의 색상 피커입니다.
* **색상 피커 매개 변수**\
  혼합 및 색상을 흑백으로 변환합니다.
  * **허용량**: 0.01 - 1.0\
    인접 색상과 혼합할 양입니다.
  * **패딩**: 0.0 - 1.0\
    대비와 같은 전환의 선명도입니다.

## 예제 이미지

| <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid_items_grid-cell1_position-par_dx_table_row-r0-column-c0_image" src="../../../../../../assets/matselector-ex.png" width="300px"/></div> |
| --- |
|  |

</td>
</tr>
</table>
