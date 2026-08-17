---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/blending-material/multi-material-blend.html"
breadcrumb-title: ''
description: 다중 재질 혼합 노드를 사용하여 여러 재질을 혼합하여 복잡한 재질 조합을 만들 수 있습니다.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > Blending (Material) > Multi-Material Blend
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 다중 재질 혼합
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '293'
ht-degree: 1%

---


# 다중 재질 혼합

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/multi-material-blend.png){width="128px"}

## 다중 재질 혼합

**내부:** *재질 필터/혼합*

**중간**

</td>
<td style="border: 0;" valign="top">

## 설명

이 노드는 메쉬에서 베이킹할 수 있는 재질 ID/색상 ID 맵을 기반으로 여러 재질을 결합합니다. [채널] 그룹에서 활성화할 수 있는 채널의 종류에 관계없이 최대 16개의 다양한 전체 재질이 필요합니다.

노드는 전체 소품을 텍스처화할 때 매우 유용합니다. 모든 소품을 동적으로 결합하면서도 재료의 전체 매개변수화를 허용합니다. 적절한 ID 베이크가 있는 단순한~복잡한 소품의 텍스처링이나 팀 표준에 완전히 부합하는 완벽한 파이프라인 &quot;템플릿&quot; Substance을 만드는 데 적합합니다.

이 옵션을 사용할 때는 [재질 1], [슬롯 1]이 항상 기본 재질이며 다른 재질이 나타나지 않는 모든 위치에 표시된다는 점에 유의하십시오. 따라서 색상을 설정할 수 없습니다. 이 금고를 재생하려면 예를 들어 러프 블랙으로 설정된 [기본 재질](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/pbr-utilities/base-material/base-material.md)를 연결하면 됩니다.

## 매개변수

### 입력

* **1-16 전체 재질 슬롯**&#x200B;슬롯 양은 **재질** 드롭다운에 의해 결정됩니다.
* **색상 ID**: *색상 입력*\
  색상 ID 맵을 구웠습니다.

### 매개변수

* **재질**: *2, 3, 4, 5, 6, 7, 8, 9, 10, 11, 12, 13, 14, 15, 16*&#x200B;혼합할 서로 다른 재질의 최대 양을 설정합니다.
* **채널**\
  예를 들어 [금속]/[거칠음] 대신 [Specular/광택] 맵을 사용하는 경우 이 그룹에서 재질 채널을 켜거나 끌 수 있습니다.
* **재질 2-16**&#x200B;활성화된 모든 재질에 대해 하나의 그룹이 나타납니다.
  * **색상**: *(색상 값)*이 재질 슬롯과 일치하는 ID 맵에서 선택할 색상입니다.
  * **흐림**: *0.01 - 1.0*&#x200B;인접한 색상으로 도련.
  * **패딩**: *0.0 - 1.0*&#x200B;전환 경도: 마스크 대비.

## 예제 이미지

|  |
| --- |
| 이 페이지에 첨부된 이미지가 없습니다. |

</td>
</tr>
</table>
