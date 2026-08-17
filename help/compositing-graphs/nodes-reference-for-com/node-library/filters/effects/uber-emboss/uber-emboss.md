---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/uber-emboss.html"
breadcrumb-title: ''
description: Uber Emboss 노드를 사용하여 사용자 정의 가능한 깊이, 각도 및 조명 컨트롤로 고급 엠보스 효과를 만듭니다.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Uber Emboss
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 우버 엠보스
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '165'
ht-degree: 2%

---


# 우버 엠보스

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/uber-emboss.png){width="128px"}

## 우버 엠보스

**내부:** *필터/효과*

**중간**

</td>
<td style="border: 0;" valign="top">

## 설명

기능이 풍부한 [엠보스](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/emboss/emboss.md)의 고급 버전입니다. Heightmap을 기반으로 정교한 2D 가짜 조명 효과를 수행합니다.

많은 제어가 필요한 경우 특정 텍스처링 스타일에 적합한 추가 조명을 만들 때 유용합니다.

## 매개변수

### 입력

* **색상**: *색상 입력*\
  수정할 기본 이미지
* **Height**: *회색 음영 입력*\
  Heightmap이 효과의 드라이버로 사용됩니다.

### 매개변수

* **주변 색상**: *(색상 값)*어두운 영역에서 사용되는 색상입니다.
* **확산 색상**: *(색상 값)*조명 영역에서 사용되는 색상입니다.
* **Specular 색상**: *(색상 값)*Specular 반사에 사용되는 색상
* **조명 강도**: *0.0 - 1.0*\
  (위조된) 조명의 강도입니다.
* **조명 각도**: *0.0 - 1.0*\
  (가짜) 빛의 입사각
* **Specular 강도**: *0.0 - 1.0* Specular 반사의 강도.
* **Specular 광도**: *0.0 - 1.0* Specular 밝은 영역의 크기.
* **확산 거칠기**: *0.0 - 1.0*&#x200B;확산 조명을 계산하는 데 사용되는 거칠기.
* **그림자 불투명도**: *0.0 - 1.0*&#x200B;그림자가 있는 영역의 혼합 불투명도.

## 예제 이미지

| <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid_items_grid-cell1_position-par_dx_table_row-r0-column-c0_image" src="../../../../../../assets/uberemboss-ex.png" width="300px"/></div> |
| --- |
|  |

</td>
</tr>
</table>
