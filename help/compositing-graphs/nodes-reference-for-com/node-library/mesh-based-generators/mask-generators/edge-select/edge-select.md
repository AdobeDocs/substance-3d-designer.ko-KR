---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/mask-generators/edge-select.html"
breadcrumb-title: ''
description: 가장자리 선택 노드를 사용하면 가장자리 기반 풍화 및 마모 효과를 만들기 위해 메시 가장자리를 선택하는 마스크를 생성할 수 있습니다.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Mask Generators > Edge Select
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 가장자리 선택
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '275'
ht-degree: 1%

---


# 가장자리 선택

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/edge-select.png){width="128px"}

## 가장자리 선택

**내부:** *메시 기반 생성기**/마스크 생성기*

**중간**

</td>
<td style="border: 0;" valign="top">

## 설명

베이킹된 맵 및 사용자 설정을 기반으로 흑백 마스크를 생성합니다. [Painter](https://support.allegorithmic.com/documentation/display/SPDOC/Substance+Painter)의 [스마트 마스크](https://support.allegorithmic.com/documentation/display/SPDOC/Smart+Materials+and+Masks)와 비슷합니다.

이 마스크는 곡률을 기준으로 가장자리를 선택하는 가장 좋은 방법입니다. 어떤 레벨이나 대비에서도 볼록하거나 오목할 수 있으므로 [레벨 노드](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/levels/levels.md)를 통해 이러한 작업을 수동으로 수행하지 않도록 하는 탁월한 단축키를 제공합니다.

## 매개변수

### 입력

* **곡률**: *회색 음영 입력*\
  가장자리를 강조하는 데 사용되는 베이킹된 맵. 필수!
* **마스크(선택 사항)**: *회색 음영 입력*\
  노드의 효과를 마스킹하는 데 사용되는 마스크 슬롯입니다.

### 매개변수

* **수준**: *0.0 - 1.0*\
  볼록 및 오목 모두에 대해 총 가장자리 강조표시 양을 설정합니다.
* **대비**: *0.0 - 1.0*\
  [볼록]과 [오목] 모두에 대해 강조 표시의 대비를 조정합니다.
* **볼록**
  * **볼록 가장자리 폭**: *0.0 - 1.0*&#x200B;볼록 가장자리에 대한 강조 표시의 폭을 설정합니다. [부드러움]을 약간 늘리면 가장자리가 더 얇아질 수 있습니다.
  * **볼록 부드러움**: *0.0 - 1.0*&#x200B;볼록 가장자리에 대한 전환의 부드러움을 설정합니다.
  * **볼록 강도**: *0.0 - 1.0*&#x200B;볼록 가장자리에 대한 최대 강조 강도를 설정합니다. 강조 표시를 하지 않으려면 0으로 설정합니다.
* **오목**
  * **오목 가장자리 폭**: *0.0 - 1.0*&#x200B;오목 가장자리에 대한 강조 표시 폭을 설정합니다. [부드러움]을 약간 늘리면 가장자리가 더 얇아질 수 있습니다.
  * **오목 부드러움**: *0.0 - 1.0*&#x200B;오목 가장자리에 대한 전환의 부드러움을 설정합니다.
  * **오목 강도**: *0.0 - 1.0*&#x200B;오목한 가장자리에 대한 가장자리 강조 표시의 최대 강도를 설정합니다. 강조 표시를 하지 않으려면 0으로 설정합니다.

## 예제 이미지

![](../../../../../../assets/edge-select-ex.gif)

</td>
</tr>
</table>
