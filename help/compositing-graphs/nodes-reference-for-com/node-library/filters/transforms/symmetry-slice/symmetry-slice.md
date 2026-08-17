---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/transforms/symmetry-slice.html"
breadcrumb-title: ''
description: 대칭 슬라이스(Symmetry Slice) 노드를 사용하면 대칭 축을 따라 텍스처를 분할하여 대칭복사된 패턴과 효과를 생성할 수 있습니다.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Transforms > Symmetry Slice
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 대칭 슬라이스
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '143'
ht-degree: 1%

---


# 대칭 슬라이스

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/mirror-2.png){width="128px"}

## 대칭 슬라이스

**내부:** *필터/변형*

**복합**

</td>
<td style="border: 0;" valign="top">

## 설명

복잡한 대칭/미러링 작업 노드입니다. 전체 제어를 통해 다양한 기하학적 연산을 수행할 수 있지만 몇 가지 실험적인 작업이 필요합니다.

[미러링](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/transforms/mirror-filter-node/mirror-filter-node.md) 및 [대칭](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/transforms/symmetry/symmetry.md)과 비교하여 이 노드에는 더 많은 옵션이 있습니다.

## 매개변수

* **대칭 모드**: *0 - 6*&#x200B;대칭 형상/거울선을 선택합니다. 옵션은 [가로], [세로], [왼쪽 대각선], [오른쪽 대각선], [세로 반전], [모퉁이] 및 [대각선 모퉁이]입니다.
* **전송 모드**: *0 - 6\
  혼합 모드. 옵션:*
* **혼합**: *0.0 - 1.0*&#x200B;원본 이미지를 결과에 다시 혼합합니다.
* **측면 뒤집기**: *False/True*&#x200B;원본을 뒤집습니다. 즉, 작업의 원본 측면이 반전됩니다. 예를 들어, 왼쪽에서 오른쪽 대칭은 오른쪽에서 왼쪽이 된다.
* **측면 뒤집기2**: *False/True*&#x200B;대칭 모드가 5 또는 6인 경우에만 사용됩니다. 모퉁이 원점을 뒤집습니다.

## 예제 이미지

| <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid_items_grid-cell1_position-par_dx_table_row-r0-column-c0_image" src="../../../../../../assets/symslice.png" width="300px"/></div> |
| --- |
|  |

</td>
</tr>
</table>
