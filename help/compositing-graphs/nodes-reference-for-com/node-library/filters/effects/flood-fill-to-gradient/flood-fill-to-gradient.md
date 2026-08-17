---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/flood-fill-to-gradient.html"
breadcrumb-title: ''
description: '[그레이디언트 Flood Fill] 노드를 사용하여 부드러운 색상 전환을 만들기 위해 그레이디언트 값으로 영역을 채웁니다.'
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Flood Fill to Gradient
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 그레이디언트로 Flood Fill
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '207'
ht-degree: 1%

---


# 그레이디언트로 Flood Fill

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/floodfill-to-gradient.png){width="128px"}

## 그레이디언트로 Flood Fill

**내부:** *필터/효과*

**단순**

</td>
<td style="border: 0;" valign="top">

## 설명

[Flood Fill](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/flood-fill/flood-fill.md) 베이스를 무작위로 향하는 그레이디언트로 변환합니다. 타일이 임의로 기울어진 높이 맵을 만드는 데 매우 유용합니다.

## 매개변수

### 입력

* **Flood Fill**: *색상 입력*&#x200B;기본 Flood Fill 데이터.
* **각도 입력**: *회색 음영 입력*\
  외부 맵을 사용하여 셀별 각도를 결정하는 옵션 맵
* **경사 입력**: *회색 음영 입력*&#x200B;셀별 그레이디언트 경사 강도를 결정하는 선택적 맵

### *매개 변수*

* **각도**: *0.0 - 1.0*&#x200B;모든 타일에 대해 균일한 전역 각도/방향을 설정합니다.
* **각도 변형**: *0.0 - 1.0*&#x200B;각 타일의 각도를 개별적으로 임의화합니다. 이것은 가장 유용하고 강력한 매개 변수입니다!
* **테두리 상자 크기에 곱하기**: *0.0 - 1.0*&#x200B;전체 선형 효과의 크기를 타일의 개별 테두리 상자 크기로 조절합니다. 즉, 더 작은 타일이 더 큰 타일보다 더 어두워집니다.
* **각도 이미지 입력 배율**: *0.0 - 1.0*&#x200B;생성된 그레이디언트 방향에 대한 선택적 각도 입력 맵의 영향 설정
* **경사 이미지 입력 승수**: *0.0 - 1.0*\
  생성된 그레이디언트 경사 강도에 대한 선택적 경사 입력 맵의 영향을 설정합니다.
* **경사 강도로 곱하기**: *0.0 - 1.0*
* **플랫 경사 색상**: *(회색 음영 값)*플랫 경사에 대해 단색 값을 설정할 수 있습니다.

## 예제 이미지

| <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid_items_grid-cell1_position-par_dx_table_row-r0-column-c0_image" src="../../../../../../assets/floodgradient-ex2.png" width="256px"/></div> | <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid_items_grid-cell1_position-par_dx_table_row-r0-column-c1_image" src="../../../../../../assets/floodgradient-ex1.png" width="256px"/></div> |
| --- | --- |
|  |  |

</td>
</tr>
</table>
