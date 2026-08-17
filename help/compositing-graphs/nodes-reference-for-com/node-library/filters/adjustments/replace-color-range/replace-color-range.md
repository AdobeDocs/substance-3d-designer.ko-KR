---
helpx_url: "https://helpx.adobe.com/kr/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/adjustments/replace-color-range.html"
breadcrumb-title: ''
description: 색상 범위 바꾸기 노드를 사용하여 지정된 범위 내의 색상을 색상 교정을 위한 새 색상으로 바꿉니다.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Adjustments > Replace Color Range
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 색상 범위 바꾸기
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '128'
ht-degree: 1%

---


# 색상 범위 바꾸기

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/replace-color-range.png){width="128px"}

## 색상 범위 바꾸기

**내부:** *필터/조정*

**단순**

</td>
<td style="border: 0;" valign="top">

## 설명

소스 색상을 대상 색상으로 대체하고 추가 컨트롤을 사용합니다. 예를 들어 재질 ID 맵의 일부를 다시 채색하는 데 사용할 수 있습니다(bake).

고급 버전은 [색상 일치](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/color-match/color-match.md)를 참조하세요.

## 매개변수

* **소스 색상**: *(색상 값)*바꿀 색상.
* **대상 색상**: *(색상 값)*바꿀 색상.
* **원본 범위**: *0.0 -* 1.0\
  선택된 출처의 범위 또는 허용한도입니다. 인접한 다른 색상에 색조가 변경되도록 추가할 수 있습니다.
* **임계값**: *0.0 - 1.0*&#x200B;범위의 밝기 감소/대비. 소스 색상만 바꾸려면 [낮음]으로 설정하고, 소스로의 혼합 색상도 바꾸려면 [높음]으로 설정합니다.

## 예제 이미지

| <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid_items_grid-cell1_position-par_dx_table_row-r0-column-c0_image" src="../../../../../../assets/replace-color-range-example.png" width="300px"/></div> |
| --- |
|  |

</td>
</tr>
</table>
