---
helpx_url: "https://helpx.adobe.com/kr/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/edge-detect.html"
breadcrumb-title: ''
description: '[가장자리 감지] 노드를 사용하면 윤곽선 및 가장자리 기반 마스크 효과를 만들기 위한 텍스처의 가장자리를 감지할 수 있습니다.'
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Edge Detect
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 가장자리 감지
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '123'
ht-degree: 1%

---


# 가장자리 감지

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/edge-detect.png){width="128px"}

## 가장자리 감지

**내부:** *필터/효과*

**단순**

</td>
<td style="border: 0;" valign="top">

## 설명

흑백 이미지의 대비를 감지한 다음 대비를 강조하는 흑백 마스크를 만듭니다.

가장자리를 위한 일종의 마스크가 필요한 많은 경우에 유용합니다. 이 옵션은 고대비 입력에서 가장 효과적이라는 점에 유의하십시오. 필요한 경우 이 노드에 내용을 전달하기 전에 대비를 조정하십시오.

## 매개변수

* **가장자리 폭**: *1.0 - 16.0*&#x200B;가장자리 주위의 감지된 영역의 폭.
* **가장자리 원형률**: *0.0 - 16.0*&#x200B;생성된 마스크를 함께 둥글게, 흐리게, 매끄럽게 합니다.
* **반전**: *False/True*\
  결과를 반전합니다.
* **허용치**: *0.0 - 1.0*&#x200B;가장자리가 나타나는 위치의 허용치 임계값 계수

## 예제 이미지

| <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid_items_grid-cell1_position-par_dx_table_row-r0-column-c0_image" src="../../../../../../assets/edge-detect-ex.png" width="300px"/></div> |
| --- |
|  |

</td>
</tr>
</table>
