---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/flood-fill-to-bbox-size.html"
breadcrumb-title: ''
description: 점진적 크기 조정 효과를 위해 테두리 상자 크기 값으로 영역을 채우려면 [상자 크기 Flood Fill] 노드를 사용합니다.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Flood Fill to BBox Size
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 상자 크기에 Flood Fill
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '101'
ht-degree: 1%

---


# 상자 크기에 Flood Fill

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/floodfill-to-bbox-size.png){width="128px"}

## 상자 크기에 Flood Fill

**내부:** *필터/효과*

**단순**

</td>
<td style="border: 0;" valign="top">

## 설명

각 타일의 개별 크기에 연결된 값을 사용하여 [Flood Fill](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/flood-fill/flood-fill.md) 기준에서 회색 음영 맵을 생성합니다.

값은 전체 캔버스 크기에 상대적이므로(전체 흰색 타일은 전체 캔버스를 늘린다는 의미임) 대비가 낮은 경우가 많습니다.

## 매개변수

* **출력**: *최대(X, Y), X, Y*&#x200B;너비, 길이 또는 둘 다 값의 기준이 되는 메트릭을 설정합니다.

## 예제 이미지

| <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid_items_grid-cell1_position-par_dx_table_row-r0-column-c0_image" src="../../../../../../assets/floodbbox-ex1.png" width="256px"/></div> |
| --- |
|  |

</td>
</tr>
</table>
