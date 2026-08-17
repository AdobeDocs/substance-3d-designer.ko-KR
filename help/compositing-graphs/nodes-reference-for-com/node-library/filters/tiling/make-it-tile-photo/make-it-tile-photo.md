---
helpx_url: "https://helpx.adobe.com/kr/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/tiling/make-it-tile-photo.html"
breadcrumb-title: ''
description: Make It Tile Photo 노드를 사용하여 사진을 매끄러운 타일링 텍스처로 변환하여 재질을 만들 수 있습니다.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Tiling > Make It Tile Photo
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 사진을 바둑판식으로 만들기
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '158'
ht-degree: 1%

---


# 사진을 바둑판식으로 만들기

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/make-it-tile-photo.png)

![](../../../../../../assets/make-it-tile-photo-grayscale.png)

## 사진을 바둑판식으로 만들기(회색 음영)

**내부:** *필터/타일링*

**중간**

</td>
<td style="border: 0;" valign="top">

## 설명

이 노드는 비연속적인 가장자리로 인해 바둑판식으로 배열되지 않을 수 있는 이미지에 대한 가장자리 수정 기능을 제공합니다. 입력 이미지의 가장자리를 제외한 다른 요소에는 영향을 주지 않습니다. 비율 또는 타일을 다른 방법으로 조정하려면 [바둑판식 패치로 만들기](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/tiling/make-it-tile-patch/make-it-tile-patch.md)를 확인하세요.

## 매개변수

* **마스크 뒤틀기 H**: *-100.0 - 100.0*&#x200B;정의되지 않은 전환을 방지하기 위해 가로 축에 뒤틀기를 도입합니다.
* **마스크 뒤틀기 V**: *-100.0 - 100.0*&#x200B;정의되지 않은 전환을 방지하기 위해 세로 축에 뒤틀기를 도입합니다.
* **마스크 크기 H**: *0.0 - 1.0*&#x200B;전환 가장자리가 가로로 도달하는 정도를 설정합니다.
* **마스크 크기 V**: *0.0 - 1.0*&#x200B;전환 가장자리가 세로로 도달하는 정도를 설정합니다.
* **마스크 정밀도 H**: *0.0 - 1.0*&#x200B;전환이 가로로 얼마나 매끄러운지 설정합니다.
* **마스크 정밀도 V**: *0.0 - 1.0*&#x200B;전환이 세로로 얼마나 매끄러운지 설정합니다.

## 예제 이미지

| <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid_items_grid-cell1_position-par_dx_table_row-r0-column-c0_image" src="../../../../../../assets/mit-photo-ex.png" width="300px"/></div> |
| --- |
|  |

</td>
</tr>
</table>
