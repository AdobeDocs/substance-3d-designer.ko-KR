---
helpx_url: "https://helpx.adobe.com/kr/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/curvature-sobel.html"
breadcrumb-title: ''
description: 곡률 소벨(Curvature Sobel) 노드를 사용하면 모서리 기반 마스크를 생성하는 소벨 연산자(Sobel operators)를 사용하여 곡률 모서리를 감지할 수 있습니다.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Curvature Sobel
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 곡률 소벨
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '107'
ht-degree: 1%

---


# 곡률 소벨

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/curvature-sobel.png){width="128px"}

## 곡률 소벨

**내부:** *필터/효과*

**단순**

</td>
<td style="border: 0;" valign="top">

## 설명

입력 [Normalmap](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/normal/normal.md)에 대해 간단하고 거친 단일 패스 곡률 변환을 수행합니다. 그 결과로 생성된 맵에는 볼록 영역의 흰색 색조와 오목 영역의 검은색 색조가 있습니다. 곡률은 항상 더 두꺼운 선과 선명한 전환을 생성합니다.

이 노드는 특정 가장자리를 빠르게 강조 표시하거나 어둡게 하는 데 유용합니다. 이 효과는 [곡률](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/curvature-filter-node/curvature-filter-node.md)과는 약간 다릅니다. 더 나은 품질의 결과를 제공하지만 선명하고 거친 느낌을 줍니다.

## 매개변수

* **강도**: *0.0 - 1.0*&#x200B;효과의 강도는 대비를 조정합니다.
* **표준 형식**: *DirectX, OpenGL*

## 예제 이미지

| <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid_items_grid-cell1_position-par_dx_table_row-r0-column-c0_image" src="../../../../../../assets/curv-sobel-ex.png" width="300px"/></div> |
| --- |
|  |

</td>
</tr>
</table>
