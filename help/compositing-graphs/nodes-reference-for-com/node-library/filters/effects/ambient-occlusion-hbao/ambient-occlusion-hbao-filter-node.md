---
helpx_url: "https://helpx.adobe.com/kr/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/ambient-occlusion-hbao-filter-node.html"
breadcrumb-title: ''
description: 주변 오클루전 HBAO 필터 노드를 사용하면 사실적인 음영을 위해 수평선 기반 알고리즘을 사용하여 주변 오클루전 맵을 생성할 수 있습니다.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Ambient Occlusion (HBAO) (Filter Node)
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 앰비언트 오클루전(HBAO)(필터 노드)
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '196'
ht-degree: 1%

---


# 앰비언트 오클루전(HBAO)(필터 노드)

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/hbao.png){width="128px"}

## 앰비언트 오클루전 (HBAO)

**내부:** *필터/효과*

**중간**

</td>
<td style="border: 0;" valign="top">

## 설명

Heightmap을 입력으로 받아 Ambient 오클루전 맵을 생성합니다. 이 응용 프로그램은 원래 화면-공간 실시간 AO 생성을 위한 알고리즘인 수평선 기반 앰비언트 오클루전(Horizon-Based Ambient Display)를 사용합니다. 절차 Heightmaps에서 절차 AO 맵을 만드는 데 매우 유용합니다.

AO의 다른 고급 버전은 [주변 오클루전(RTAO)](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/ambient-occlusion-rtao/ambient-occlusion-rtao.md)를 참조하십시오.

## 매개변수

* **월드 단위 사용**: *False/True*&#x200B;월드 단위 또는 화면 공간 단위 사용을 전환합니다. 보다 정확하게 제어할 수 있는 추가 매개 변수를 활성화합니다.
* **Height 깊이**: *0.0 - 1.0*&#x200B;세계 단위가 False로 설정된 경우에만 사용됨. 전역 크기 조절을 제어합니다.
* **표면 크기**: **0.0 - 1000.0** World Units가 True로 설정된 경우에만 사용됩니다. 전역 크기 조절을 제어합니다.
* **Height 크기(cm)**: *0.0 - 1000.0* World Units가 True로 설정된 경우에만 사용됩니다. 전역 크기 조절을 제어합니다.
* **반경**: *0.0 - 1.0* AO의 확산을 제어합니다.
* **품질**: *4개 샘플, 8개 샘플, 16개 샘플*\
  계산에 사용되는 샘플 양을 결정하여 품질 레벨을 설정합니다.
* **GPU 최적화**: *False/True*&#x200B;내부 GPU 최적화를 사용하고 처리 속도를 높입니다.

## 예제 이미지

| <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid_items_grid-cell1_position-par_dx_table_row-r0-column-c0_image" src="../../../../../../assets/image2021-6-18-11-11-11-1.png" width="300px"/></div> | <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid_items_grid-cell1_position-par_dx_table_row-r0-column-c1_image" src="../../../../../../assets/image2021-6-18-11-11-22.png" width="300px"/></div> |
| --- | --- |
|  |  |

</td>
</tr>
</table>
