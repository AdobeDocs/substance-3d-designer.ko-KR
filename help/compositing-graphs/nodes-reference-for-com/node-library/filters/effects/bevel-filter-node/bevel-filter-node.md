---
helpx_url: "https://helpx.adobe.com/kr/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/bevel-filter-node.html"
breadcrumb-title: ''
description: 경사 필터 노드를 사용하면 깊이 및 치수를 추가하기 위해 모양과 패턴에 경사진 가장자리를 만들 수 있습니다.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Bevel (Filter Node)
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 경사(필터 노드)
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '202'
ht-degree: 2%

---


# 경사(필터 노드)

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/bevel.png){width="128px"}

## 경사

**내부:** *필터/효과*

**중간**

</td>
<td style="border: 0;" valign="top">

## 설명

입력 회색 음영 높이 맵에 가장자리 베벨링 효과를 적용합니다. 해당 Heightmap에 따라 경사진 Heightmap과 Normalmap을 모두 반환합니다.

이 노드는 이상적인 바이너리(높은 수축 흑백), 기본 Heightmap에 정확한 곡선 프로파일을 적용하는 데 유용합니다.

## 매개변수

### 입력

* **입력**: *회색 음영 입력*\
  변환할 Heightmap.
* **사용자 지정 곡선**: *회색 음영 입력*\
  정확한 곡선/경사를 결정하는 그레이디언트입니다. [수준](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/levels/levels.md) 또는 [곡선](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/curve/curve.md)과 같은 모든 종류의 조정을 수행할 수 있는 [선형 그레이디언트] 노드입니다. &quot;사용자 정의 곡선 사용&quot;이 True인 경우에만 활성화됩니다.

### 매개변수

* **거리**: *-1.0 - 1.0*&#x200B;경사 효과의 도달 거리
* **모퉁이 유형**: *둥근 Angular*&#x200B;베벨링 프로필을 둥글게 해야 하는지, 곧게 해야 하는지 여부.
* **매끄럽게 하기**: *0.0 - 5.0*&#x200B;경사 후 수행할 추가 매끄럽게 하기(흐림) 정도.
* **균일하지 않은 흐림 효과 사용**: *False/True*&#x200B;매끄럽게 만드는 작업이 균일하지 않게 수행되어야 하는지 여부.
* **사용자 지정 곡선 사용**: *False/True*&#x200B;사용자 지정 Height 곡선 사용을 전환합니다. 자세한 내용은 위를 참조하십시오.
* **표준 강도**: *0.0 - 50.0*&#x200B;생성된 표준 맵의 강도.
* **표준 형식**: *DirectX, OpenGL*\
  다른 표준 맵 포맷 간에 전환합니다(녹색 채널을 반전합니다).

## 예제 이미지

| <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid_items_grid-cell1_position-par_dx_table_row-r0-column-c0_image" src="../../../../../../assets/bevel-example.png" width="300px"/></div> |
| --- |
|  |

</td>
</tr>
</table>
