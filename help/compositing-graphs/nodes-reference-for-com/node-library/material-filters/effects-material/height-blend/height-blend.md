---
helpx_url: "https://helpx.adobe.com/kr/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/effects-material/height-blend.html"
breadcrumb-title: ''
description: '[Height 혼합] 노드를 사용하면 Height 맵을 기반으로 텍스처를 블렌딩하여 사실적인 재질 전환을 만들 수 있습니다.'
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > Effects (Material) > Height Blend
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Height 블렌드
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '171'
ht-degree: 2%

---


# Height 블렌드

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/height-blend.png){width="128px"}

## Height 블렌드

**내부:** *재질 필터/효과*

**단순**

</td>
<td style="border: 0;" valign="top">

## 설명

Height 정보를 기반으로 두 개의 Heightmap을 결합합니다. 혼합 하이트맵을 생성하지만 다른 곳에서 사용할 수 있는 흑백 마스크도 생성합니다.

이 기능은 결합할 두 개의 고품질 Heightmap이 있지만 [재질 Height 블렌드](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/effects-material/material-height-blend/material-height-blend.md)에 필요한 전체 재질이 아닐 때 유용합니다.

## 매개변수

### 입력

* **위쪽 Height**: *회색 음영 입력*
* **Height 아래쪽**: *회색 음영 입력*
* **마스크(선택 사항)**: *회색 음영 입력*\
  노드의 효과를 마스킹하는 데 사용되는 마스크 슬롯입니다.

### 매개변수

* **Height 오프셋**: *0.0 - 1.0*&#x200B;혼합 레벨이 Height 축을 따라 이동되도록 높이 맵을 오프셋합니다. 혼합에 대한 기본 컨트롤입니다.
* **대비**: *0.0 - 1.0*\
  혼합의 대비를 조정하고 전환을 더 선명하게 합니다.
* **모드**: *균형 잡힌 Height, 아래쪽 Height 우선 순위*&#x200B;두 다른 혼합 모드 간에 전환합니다.
* **불투명도**: *0.0 - 1.0*\
  전경 Height의 불투명도를 혼합하면 안쪽이나 바깥쪽으로 페이드됩니다.

## 예제 이미지

|  |
| --- |
| 이 페이지에 첨부된 이미지가 없습니다. |

</td>
</tr>
</table>
