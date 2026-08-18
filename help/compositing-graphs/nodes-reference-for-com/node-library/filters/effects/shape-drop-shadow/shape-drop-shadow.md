---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/shape-drop-shadow.html"
breadcrumb-title: ''
description: '[모양 그림자] 노드를 사용하면 모양에 그림자 효과를 추가하여 텍스처에 깊이와 차원을 만들 수 있습니다.'
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Shape Drop Shadow
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 모양 그림자
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '209'
ht-degree: 0%

---


# 모양 그림자

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/shape-dropshadow-grayscale.png){width="128px"}

![](../../../../../../assets/shape-dropshadow.png){width="128px"}

## 모양 그림자(회색 음영)

**내부:** *필터/효과*

**중간**

</td>
<td style="border: 0;" valign="top">

## 설명

다른 2D 이미지 처리 소프트웨어에서 잘 알려진 &quot;그림자 만들기&quot; 효과를 입력 흑백 마스크(회색 음영 버전) 또는 투명도가 있는 이미지(색상 버전)에 수행합니다.

[어두운 영역](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/shadows-filter-node/shadows-filter-node.md) 효과와는 달리 전체 투명도가 적용된 이미지를 반환하므로 다른 소프트웨어에서 기대하는 것과 유사한 효과를 더 완벽하게 얻을 수 있습니다.

## 매개변수

* **각도**: (가짜) 빛의 *0.0 - 1.0*&#x200B;입사각.
* **거리**: *-0.5 - 0.5*&#x200B;그림자가 아래로 떨어지면 모양에서 멀어집니다.
* **크기**: *0.0 - 1.0*&#x200B;그림자의 흐림/흐림 효과를 제어합니다.
* **스프레드**: *0.0 - 1.0*&#x200B;흐림 효과의 차단/임계값 때문에 그림자가 더 멀리 퍼집니다.
* **불투명도**: *0.0 - 1.0*\
  그림자 효과에 대한 혼합 불투명도.
* **(그림자) 색상**: *(색상 값)*그림자에 적용될 색상 색조입니다.
* **마스크 색상**: *(색상 값) *(회색 음영 버전만)**투명도 매핑 출력에 사용할 단색.
* **입력이 미리 곱해졌습니다**: *False/True *(색상 버전만 해당)**입력이 미리 곱해졌다고 가정해야 하는지 여부.
* **미리 곱하기 출력**: *False/True*&#x200B;미리 곱해야 하는지 여부를 지정합니다.

## 예제 이미지

| <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid_items_grid-cell1_position-par_dx_table_row-r0-column-c0_image" src="../../../../../../assets/dropshadowex.png" width="300px"/></div> |
| --- |
|  |

</td>
</tr>
</table>
