---
helpx_url: "https://helpx.adobe.com/kr/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/glow.html"
breadcrumb-title: ''
description: Glow node를 사용하여 텍스처에 광선 효과를 추가하면 발광형 및 발광형 재질 모양을 만들 수 있습니다.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Glow
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 광선
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '178'
ht-degree: 1%

---


# 광선

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/glow-greyscale.png){width="128px"}

![](../../../../../../assets/glow-3.png){width="128px"}

## 광선

**내부:** *필터/효과*

**단순**

</td>
<td style="border: 0;" valign="top">

## 설명

다른 인기 있는 이미지 편집 소프트웨어에서 볼 수 있는 &quot;외부 광선&quot; 유형의 효과를 수행합니다. 기본적으로 입력 주위에 페이딩 그레이디언트 윤곽선을 추가합니다.

예상과 달리 Alpha 채널이 있는 이미지에는 적용되지 않습니다. 색상 버전에서도 이진, 검은색 및 흰색 마스크만 입력으로 표시되며 색상이 있는 광선만 사용할 수 있습니다. 투명도가 있는 이미지에 사용할 버전을 찾고 있는 경우 [모양 광선](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/shape-glow/shape-glow.md)을 참조하세요.

중요: 입력에 적합한 버전을 사용해야 합니다. 색상 입력에는 &quot;Glow&quot;를 사용하고 회색 음영 입력에는 &quot;Glow Grayscale&quot;을 사용합니다.

## 매개변수

* **광선 양**: 광선 효과에 대한 *0.0 - 1.0*&#x200B;전역 불투명도.
* **양 지우기**: *0.0 - 1.0*&#x200B;광선 효과를 잘라내는 시점을 위한 트레숄드. 반투명 영역에 유용합니다.
* **광선 크기**: *0.0 - 20.0*&#x200B;광선 효과의 도달 범위를 제어합니다.
* **광선 색상**: *(색상 값)(색상 버전만 해당)*광선 효과의 색상을 설정합니다.

## 예제 이미지

| <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid_items_grid-cell1_position-par_dx_table_row-r0-column-c0_image" src="../../../../../../assets/glow-ex.png" width="300px"/></div> |
| --- |
|  |

</td>
</tr>
</table>
