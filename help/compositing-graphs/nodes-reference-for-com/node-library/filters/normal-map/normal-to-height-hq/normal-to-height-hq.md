---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/normal-map/normal-to-height-hq.html"
breadcrumb-title: ''
description: 표준-Height HQ 노드를 사용하여 표준 맵을 표면 세부 정보 추출을 위한 고품질 Height 맵으로 변환합니다.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Normal Map > Normal To Height HQ
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Height HQ에 수직
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '192'
ht-degree: 1%

---


# Height HQ에 수직

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/normal-to-height-hq.png){width="128px"}

## Height HQ에 수직

**내부:** *필터/표준 맵*

**중간**

</td>
<td style="border: 0;" valign="top">

## 설명

탄젠트 공간 정규맵을 다시 Heightmap으로 변환하려는 역방향 변환 노드입니다. 이 Height은 고급 노드입니다. [노드에 대한 일반](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/normal-map/normal-to-height/normal-to-height.md)은(는) 옵션이 적으며 다른 계산을 사용합니다.

Normalmap 소스만 있지만 Heightmap과 결합하는 작업을 수행하려는 경우에 유용합니다. Height이 [일반]으로 변환되는 프로세스의 특성상 정보가 손실되므로 이 경우 100% 정확한 결과를 제공할 수 없다는 점을 명심하십시오. 올바르게 생성된 Heightmap은 절대 바꿀 수 없습니다!

## 매개변수

* **표준 형식**: *DirectX, OpenGL*\
  서로 다른 표준 맵 포맷 사이를 전환합니다(녹색 채널을 반전합니다).
* **부조 균형**: *0.0 - 1.0*&#x200B;낮은 주파수 및 높은 주파수 편향을 혼합합니다.
* **Height 강도**: *0.0 - 1.0*&#x200B;하이트맵의 강도 또는 승수는 전역 불투명도와 약간 비슷하게 작동합니다.
* **Height 표준화**: *False/True* Heightmap 범위를 자동으로 확장하여 [자동 수준](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/auto-levels/auto-levels.md)과 같이 완전한 대비를 사용합니다.
* **품질**: *보통, 높음*&#x200B;속도 또는 품질 사이를 전환합니다.

## 예제 이미지

| <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid_items_grid-cell1_position-par_dx_table_row-r0-column-c0_image" src="../../../../../../assets/normal2height-hq-ex.png" width="300px"/></div> |
| --- |
|  |

</td>
</tr>
</table>
