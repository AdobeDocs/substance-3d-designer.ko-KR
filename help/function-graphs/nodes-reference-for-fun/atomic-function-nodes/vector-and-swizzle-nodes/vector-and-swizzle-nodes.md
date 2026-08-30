---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/function-graphs/nodes-reference-for-function-graphs/atomic-function-nodes/vector-and-swizzle-nodes.html"
breadcrumb-title: ''
description: Substance 3D Designer 함수 그래프에서 벡터 및 스위즐 노드를 사용하여 벡터 데이터 및 구성 요소를 조작할 수 있습니다.
helpx_creative_field: ""
helpx_description: Designer > Function graphs > Nodes reference for function graphs > Vector
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 벡터
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '498'
ht-degree: 5%

---


# 벡터 및 스위즐 노드

벡터 노드와 스위즐 노드를 사용하면 각각 별도의 구성 요소에서 벡터 노드를 구성하고 분해할 수 있습니다.[RGBA 병합](../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/channels/rgba-merge/rgba-merge.md) 및 [RGBA 분할](../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/channels/rgba-split/rgba-split.md)과(와) 비슷하지만 함수 그래프의 경우에는 비슷합니다. [Casting](../../../../function-graphs/nodes-reference-for-fun/atomic-function-nodes/cast-nodes/cast-nodes.md)은(는) 많은 경우에 옵션이 아니므로 벡터 데이터 형식 간에 변환하기 위한 주된 방법이기도 합니다.

## 벡터 노드

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

벡터 노드를 사용하면 구성 요소가 적은 벡터 또는 요소를 구성 요소가 많은 벡터로 결합할 수 있습니다. 벡터 노드에는 몇 가지 특정 규칙이나 제한 사항이 있습니다.

* 결과 Vector에 2개 이상의 구성 요소가 있는 경우에도 벡터 노드에는 **2개의 입력만**&#x200B;이 있습니다.
* 벡터 입력은 **한 유형으로 제한되지 않음**: 더 작은 구성 요소를 입력으로 사용할 수 있습니다.
* 결과 출력의 순서는 **입력의 순서**&#x200B;에 따라 결정됩니다.

즉, 다음 방법을 사용하는 것이 가장 좋습니다.

* 두 가지 방법으로 벡터 4를 구성합니다. 즉, 두 개의 2성분 벡터를 연결하거나, 1성분과 3성분 벡터를 연결합니다.
* 단일 정수 또는 Float에서 3 또는 4 구성 요소 벡터를 생성하려면 먼저 벡터 2 조합을 하나 이상 수행한 다음 이들을 3 구성 요소 벡터로 결합해야 합니다.

연결 순서에 대해 잘 생각해 보십시오. 입력의 연결 순서는 다음과 같습니다.

![](vector-and-swizzle-nodes.resources/vector-int1.png){width="200px"}

Example on Left는 먼저 Integer(1)를 연결한 다음 Integer 3을 연결합니다. 결과는 아래와 같습니다

| 출력 | X | Y | Z | W |
| --- | --- | --- | --- | --- |
| 입력 1 | 0 |  |  |  |
| 입력 2 |  | 1 | 2 | 4 |

![](vector-and-swizzle-nodes.resources/vector-int2.png){width="200px"}

Example on Left swaps는 첫 번째 예인 Integer 3부터 Integer(1) 순으로 입력합니다.

| 출력 | X | Y | Z | W |
| --- | --- | --- | --- | --- |
| 입력 1 | 1 | 2 | 4 |  |
| 입력 2 |  |  |  | 0 |

</td>
<td style="border: 0;" valign="top">

| <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid_items_grid-cell1_position-par_dx_table_row-r0-column-c0_image" src="vector-and-swizzle-nodes.resources/fn-vector-vectorint4.png"/></div> | <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid_items_grid-cell1_position-par_dx_table_row-r0-column-c1_image" src="vector-and-swizzle-nodes.resources/fn-vector-vectorint2.png"/></div> | <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid_items_grid-cell1_position-par_dx_table_row-r0-column-c2_image" src="vector-and-swizzle-nodes.resources/fn-vector-vectorint3.png"/></div> |
| --- | --- | --- |
| **벡터 정수2** | **벡터 정수3** | **벡터 정수4** |
| <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid_items_grid-cell1_position-par_dx_table_row-r2-column-c0_image" src="vector-and-swizzle-nodes.resources/fn-vector-vectofloat3.png"/></div> | <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid_items_grid-cell1_position-par_dx_table_row-r2-column-c1_image" src="vector-and-swizzle-nodes.resources/fn-vector-vectofloat2.png"/></div> | <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid_items_grid-cell1_position-par_dx_table_row-r2-column-c2_image" src="vector-and-swizzle-nodes.resources/fn-vector-vectofloat4.png"/></div> |
| **벡터 부동 소수점2** | **벡터 부동 소수점3** | **벡터 Float4** |

</td>
</tr>
</table>

## 스위즐 노드

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

스와이즐 노드는 다성분 벡터에서 성분을 분해하거나 분리하여 X, Y, Z, W 성분을 개별적으로 활용하고 스와이즈할 수 있도록 합니다. 다음 규칙 및 제한 사항이 적용됩니다.

* 스위즐 노드에는 **한 개의 출력**&#x200B;만 있습니다.
* 스위즐 노드 **입력**&#x200B;이 올바른 형식(Int 또는 Float)입니다.

### 구성 요소 분할

스위즐의 가장 일반적인 경우는 Integer4를 4개의 개별 정수로 내리는 것과 같은 구성 요소를 분할하는 데 사용하는 것입니다. 제한 사항은 이를 위해 4개의 개별 스위즐 정수 노드가 필요하다는 것을 의미합니다.

두 개의 Integer2, 또는 Integer와 Integer3과 같은 Integer4에 대해서도 모든 결과에는 자체 노드가 필요하다는 점을 다시 염두에 두고 다른 종류의 분할이 가능합니다.

### 구성 요소 교체/교체

이름에서 알 수 있듯이 스위즐은 값의 순서를 변경하거나 값을 덮어쓰는 데 사용할 수 있습니다. X,Y,Z,W에서 W,Y,X,Z로 순서를 변경할 수 있으며 예를 들어 X,Y,Z,W에서 X,X,X,W로 값을 변경할 수 있습니다.

</td>
<td style="border: 0;" valign="top">

| <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid1_items_grid-cell1_position-par_dx_table_row-r0-column-c0_image" src="vector-and-swizzle-nodes.resources/fn-vector-swizzleint1.png"/></div> | <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid1_items_grid-cell1_position-par_dx_table_row-r0-column-c1_image" src="vector-and-swizzle-nodes.resources/fn-vector-swizzleint2.png"/></div> | <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid1_items_grid-cell1_position-par_dx_table_row-r0-column-c2_image" src="vector-and-swizzle-nodes.resources/fn-vector-swizzleint3.png"/></div> | <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid1_items_grid-cell1_position-par_dx_table_row-r0-column-c3_image" src="vector-and-swizzle-nodes.resources/fn-vector-swizzleint4.png"/></div> |
| --- | --- | --- | --- |
| **스위즐 정수** | **스위즐** **정수2** | **스위즐** **정수3** | **스위즐** **정수4** |
| <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid1_items_grid-cell1_position-par_dx_table_row-r2-column-c0_image" src="vector-and-swizzle-nodes.resources/fn-vector-swizzlefloat1.png"/></div> | <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid1_items_grid-cell1_position-par_dx_table_row-r2-column-c1_image" src="vector-and-swizzle-nodes.resources/fn-vector-swizzlefloat2.png"/></div> | <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid1_items_grid-cell1_position-par_dx_table_row-r2-column-c2_image" src="vector-and-swizzle-nodes.resources/fn-vector-swizzlefloat3.png"/></div> | <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid1_items_grid-cell1_position-par_dx_table_row-r2-column-c3_image" src="vector-and-swizzle-nodes.resources/fn-vector-swizzlefloat4.png"/></div> |
| **회전** **부동** | **스위즐** **부동 소수점2** | **회전** **부동 소수점3** | **스위즐** **부동 소수점 4** |

</td>
</tr>
</table>
