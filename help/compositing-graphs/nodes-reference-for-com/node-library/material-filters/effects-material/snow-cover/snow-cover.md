---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/effects-material/snow-cover.html"
breadcrumb-title: ''
description: '[Snow 덮개] 노드를 사용하여 표면 각도 및 위치를 기반으로 재질에 눈 축적 효과를 추가합니다.'
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > Effects (Material) > Snow Cover
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Snow 표지
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '171'
ht-degree: 2%

---


# Snow 표지

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/snow-cover.png){width="128px"}

## Snow 표지

**내부:** *재질 필터/효과*

**중간**

</td>
<td style="border: 0;" valign="top">

## 설명

올인원 효과로 전체 소재에 쌓인 눈을 추가할 수 있습니다. Photoscan과 같은 좋은 고품질 Heightmap에 크게 의존합니다. 결과는 PBR 교정이 됩니다.

## 매개변수

### 입력

* **마스크(선택 사항)**: *회색 음영 입력*\
  노드의 효과를 마스킹하는 데 사용되는 마스크 슬롯입니다.

### 매개변수

* **채널**\
  예를 들어 [금속]/[거칠음] 대신 [Specular/광택] 맵을 사용하는 경우 이 그룹에서 재질 채널을 켜거나 끌 수 있습니다.
* **새 Snow**: *0.0 - 1.0*&#x200B;눈 양을 높인 영역으로 설정합니다. 결과는 용융된 Snow 매개변수와 연관됩니다.
* **녹은 Snow**: *0.0 - 1.0*&#x200B;낮은 모서리의 녹은 눈의 양을 설정합니다.
* **빌드업**: *0.0 - 1.0*&#x200B;대부분 Height 출력에 영향을 미치고 Height 쌓기 효과를 결정합니다.
* **Smoothness**: *0.0 - 1.0*&#x200B;눈 쌓기로 Height 세부 사항의 매끄러움을 설정합니다.
* **플레이크 강도**: *0.0 - 1.0*&#x200B;주로 플레이크 세부 정보의 강도(표준 맵)에 영향을 줍니다.

## 예제 이미지

|  |
| --- |
| 이 페이지에 첨부된 이미지가 없습니다. |

</td>
</tr>
</table>
