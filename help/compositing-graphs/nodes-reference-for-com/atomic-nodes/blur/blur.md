---
helpx_url: "https://helpx.adobe.com/kr/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/atomic-nodes/blur.html"
breadcrumb-title: ''
description: '[흐림 효과] 노드를 사용하면 세부 사항을 매끄럽게 하고 소프트 포커스 효과를 만들기 위해 텍스처에 흐림 효과를 적용할 수 있습니다.'
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Atomic nodes > Blur
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 흐림 효과
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '168'
ht-degree: 5%

---


# 흐림 효과

<table>
<tr style="border: 0;">
<td width="41.60%" style="border: 0;" valign="top">

![흐림 효과 노드 아이콘](../../../../assets/blur-9.png){width="200px"}

**내부:** 원자 노드

**단순**

</td>
<td width="58.30%" style="border: 0;" valign="top">

## 설명

흐림 효과 노드는 &quot;상자 흐림 효과&quot; 작업을 수행합니다. 설정된 거리 위의 픽셀 값의 평균을 내서 흐릿하고 선명하지 않은 모양을 만듭니다. 이 기능은 [Substance 3D Designer](https://www.adobe.com/kr/products/substance3d-designer.html)에서 사용할 수 있는 가장 간단하고 빠르고 기본적인 흐림 효과를 제공합니다.

흐림 효과는 일부 가장자리를 약간 부드럽게 하는 등의 빠르고 간단한 작업에 적합하지만 보다 까다로운 시나리오에서 [흐림 효과 HQ](../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/blurs/blur-hq/blur-hq.md)를 사용하는 것이 더 좋습니다. 즉, 품질을 위해 성능을 저하시킬 수 있습니다.

</td>
</tr>
</table>

## 매개변수

* **강도**: 0-무제한\
  흐림 효과의 강도나 거리를 설정합니다. 이 값은 상한이 적용되지 않지만 높은 값에서 전체 이미지는 평균 색상으로 바뀝니다.

아래 예제는 높은 값(이 경우 50)을 사용할 때 이 노드의 흐림 효과를 왼쪽의 흐림 효과와 오른쪽의 [흐림 효과 HQ](../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/blurs/blur-hq/blur-hq.md)에 대해 보여 줍니다. 1-2 정도의 값에서는 차이가 두드러지지 않습니다.

| 흐림(원자성) | 흐림 효과 HQ |
| --- | --- |
| <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dx_table_row-r1-column-c0_dynamic_grid_items_grid-cell_position-par_image" src="../../../../assets/blur-example.png"/></div> | <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dx_table_row-r1-column-c1_dynamic_grid_items_grid-cell_position-par_image" src="../../../../assets/blur-hq.png"/></div> |
