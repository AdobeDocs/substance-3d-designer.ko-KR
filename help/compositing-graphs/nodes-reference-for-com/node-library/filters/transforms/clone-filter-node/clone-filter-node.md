---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/transforms/clone-filter-node.html"
breadcrumb-title: ''
description: 복제 필터 노드를 사용하면 매끄러운 패턴 및 타일링 효과를 내기 위해 텍스처 영역을 복제하고 오프셋할 수 있습니다.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Transforms > Clone (Filter Node)
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 복제(필터 노드)
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '181'
ht-degree: 2%

---


# 복제(필터 노드)

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/clone-4.png)

## 복제

**내부:** *필터/변형*

**중간**

</td>
<td style="border: 0;" valign="top">

## 설명

입력 이미지를 지정한 위치로 한 번 복제합니다. 조잡한 &quot;복제 도장&quot; 도구로 작동할 수 있습니다.

원하는 결과를 얻기 위해 약간의 주의가 필요합니다.

* 블렌드는 직선 복사본이므로 입력 이미지에는 데칼과 같은 알파 채널이 있는 것이 좋습니다.
* 마스크는 기본적으로 검은색으로 설정되므로 결과를 보려면 균일한 흰색 회색 음영 값을 적어도 플러깅해야 합니다.
* [오프셋]은 이미지 바깥쪽을 쉽게 클리핑하므로 작은 값을 사용합니다.

## 매개변수

### 입력

* **소스**: *색상 입력*\
  복제할 이미지입니다. 중요: 이미지에 알파 채널이 있는 것이 이상적입니다!
* **마스크**: *회색 음영 입력*\
  노드의 효과를 마스킹하는 데 사용되는 마스크 슬롯입니다. 기본적으로 검정으로 설정됩니다!

### 매개변수

* **오프셋**: *-*\
  결과를 이동하거나 변환합니다. 양성은 왼쪽 위, 음성은 오른쪽 아래 작은 값을 사용하면 1.0 이상으로 설정하면 이미지 밖으로 이동합니다!
* **흐림 효과 마스크**: *0.0 - 10.0\
  흐림 효과 필터를 마스크에 적용하여 가장자리를 부드럽게 합니다.*

## 예제 이미지

| <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid_items_grid-cell1_position-par_dx_table_row-r0-column-c0_image" src="../../../../../../assets/clone-example.png" width="300px"/></div> |
| --- |
|  |

</td>
</tr>
</table>
