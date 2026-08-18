---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/blending-material/material-adjustment-blend.html"
breadcrumb-title: ''
description: 재질 조정 블렌드 노드를 사용하여 재질 간에 재질 조정을 블렌딩하여 합성 효과를 미세 조정합니다.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > Blending (Material) > Material Adjustment Blend
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 재질 조정 블렌드
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '385'
ht-degree: 1%

---


# 재질 조정 블렌드

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/material-adjustment-blend.png){width="128px"}

## 재질 조정 블렌드

**내부:** *재질 필터/혼합*

**중간**

</td>
<td style="border: 0;" valign="top">

## 설명

이 노드는 마스크를 기반으로 전체 재질의 모든 채널을 조정할 수 있습니다. 전체 재질 워크플로우를 더 쉽고 빠르게 만들기 위한 것입니다.

이 효과는 동일한 마스크를 기반으로 재질의 몇 가지 채널을 조정하려는 경우(예: 확산을 더 밝게 하고 거칠기를 더 어둡게 하려는 경우)에 유용합니다.

## 매개변수

### 입력

* **색상 ID 마스크**: *색상 입력*\
  노드의 효과를 마스킹하는 데 사용되는 마스크 슬롯입니다.
* **회색 음영 마스크**: *회색 음영 입력*\
  노드의 효과를 마스킹하는 데 사용되는 마스크 슬롯입니다.

### 매개변수

* **채널**\
  이 그룹에서 재질 채널을 켜거나 끕니다. 예를 들어 [금속]/[거칠음] 대신 [Specular/광택] 맵을 사용하는 경우\
  이렇게 하면 채널의 관련 그룹도 나타나거나 나타나지 않게 됩니다.
* **확산**\
  마스크에 의해 정의된 영역에서 확산 채널에 대한 조정 작업을 수행합니다.
* **기본 색상**\
  마스크에 의해 정의된 영역의 [기준 색상] 채널에서 조정 작업을 수행합니다.
* **표준**
  * **강도**: *0.0 - 1.0*&#x200B;표준 강도를 낮춥니다.
* **Specular**\
  마스크에 의해 정의된 영역에서 Specular 채널에 대한 조정 작업을 수행합니다.
* **발광**\
  마스크에 의해 정의된 영역에서 Emissive 채널에 대한 조정 작업을 수행합니다.
* **광택**\
  마스크에 의해 정의된 영역의 [광도] 채널에서 조정 작업을 수행합니다.
* **거칠음**\
  마스크에 의해 정의된 영역에서 [거칠음] 채널에 대한 조정 작업을 수행합니다.
* **금속**\
  마스크에 의해 정의된 영역의 금속 채널에 대해 조정 작업을 수행합니다.
* **Specular level**\
  마스크에 의해 정의된 영역에서 Specular level 채널에 대한 조정 작업을 수행합니다.
* **주변 오클루전**\
  마스크에 의해 정의된 영역의 앰비언트 오클루전 채널에 대해 조정 작업을 수행합니다.
* **Height**\
  마스크에 의해 정의된 영역에서 Height 채널에 대한 조정 작업을 수행합니다.
* **불투명도**\
  마스크로 정의된 영역의 [불투명도] 채널에서 조정 작업을 수행합니다.
* **색상 ID 마스크**: *False/True*&#x200B;회색 음영 마스크 대신 색상 ID 마스크를 사용하도록 설정합니다.
* **허용량**: *0.01 - 1.0*&#x200B;색상 ID 마스크를 사용하면 색상 ID 선택 색상의 확산이 결정됩니다.
* **색상**: *(색상 값)*색상 ID 맵 및 마스크에서 선택할 색상을 설정합니다.
* **패딩**: *0.0 - 1.0*&#x200B;색상 ID 마스크의 혼합 대비/전환을 결정합니다.

## 예제 이미지

|  |
| --- |
| 이 페이지에 첨부된 이미지가 없습니다. |

</td>
</tr>
</table>
