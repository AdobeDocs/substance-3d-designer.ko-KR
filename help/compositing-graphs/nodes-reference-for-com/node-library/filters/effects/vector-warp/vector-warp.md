---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/vector-warp.html"
breadcrumb-title: ''
description: 벡터 뒤틀기 노드를 사용하면 유동적이고 유기적인 왜곡 효과를 만들기 위해 벡터 필드를 사용하여 텍스처를 뒤틀 수 있습니다.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Vector Warp
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 벡터 뒤틀기
user-guide-description: ''
user-guide-title: ''
source-git-commit: c002fea6f396f09ccb3218bd290db812d8367dc4
workflow-type: tm+mt
source-wordcount: '237'
ht-degree: 1%

---


# 벡터 뒤틀기

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/vector-warp.png){width="128px"}

![](../../../../../../assets/vector-warp-grayscale.png){width="128px"}

## 벡터 뒤틀기(회색 음영)

**내부:** *필터/효과*

**복합**

</td>
<td style="border: 0;" valign="top">

## 설명

벡터 뒤틀기는 [뒤틀기](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/warp/warp.md) 및 [방향 뒤틀기](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/directional-warp/directional-warp.md)와 유사한 고급 왜곡 효과로, 주요 차이점은 회색 음영 맵이 아닌 (색상) 벡터 비트맵으로 구동된다는 것입니다. 이것은 그것이 원자 마디의 사촌들보다 더 강력하고 다재다능하다는 것을 의미한다.

벡터맵은 정규맵과 유사하지만 정규화할 필요는 없으며 R 및 Green (X 및 Y) 채널만 사용됩니다. 파란색 및 Alpha 채널은 원하는 경우 검은색으로 남겨둘 수 있습니다. 좋은 벡터 맵을 구성하는 것은 이 노드를 사용하는 데 있어 가장 큰 문제가 될 수 있습니다. [회색 음영 맵을 표준으로 변환](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/normal/normal.md)하거나 채널을 [RGBA 병합](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/channels/rgba-merge/rgba-merge.md)과 결합하여 맵을 구성할 수 있습니다. 또는 [&quot;흐름 맵&quot;](https://experienceleague.adobe.com/en/docs/substance-3d-painter/using/painting/advanced-channel-painting/flow-map-painting)과 같은 것도 사용할 수 있습니다.

이 왜곡은 표준 뒤틀기 노드가 노드를 잘라내지 않고 방향이 다양한 매우 특정 노드를 수행하려는 경우에 유용할 수 있습니다.

## 매개변수

### 입력

* **입력**: *색상 입력*\
  왜곡에 매핑할 수 있습니다.
* **벡터 맵**: *색상 입력*\
  왜곡 드라이버 맵. 빨강 및 파랑 색상 채널이 사용됩니다.

### 매개변수

* **강도**: 벡터 맵에 대한 *0.0 - 1.0*&#x200B;강도 승수.
* **벡터 형식**: *DirectX, OpenGL*&#x200B;위/아래 해석 간에 녹색 채널을 바꿉니다.

## 예제 이미지

| <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid_items_grid-cell1_position-par_dx_table_row-r0-column-c0_image" src="../../../../../../assets/vector-warp-ex.png" width="300px"/></div> |
| --- |
|  |

</td>
</tr>
</table>
