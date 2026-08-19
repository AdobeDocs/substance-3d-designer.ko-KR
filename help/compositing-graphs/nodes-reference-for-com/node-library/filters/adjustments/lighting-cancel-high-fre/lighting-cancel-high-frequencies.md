---
helpx_url: "https://helpx.adobe.com/kr/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/adjustments/lighting-cancel-high-frequencies.html"
breadcrumb-title: ''
description: '[조명 취소 고주파] 노드를 사용하여 재료 분석을 위해 텍스처에서 고주파 조명 세부 사항을 제거합니다.'
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Adjustments > Lighting Cancel High Frequencies
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 고주파수 조명 취소
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '99'
ht-degree: 2%

---


# 고주파수 조명 취소

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/lighting-cancel-high-frequencies.png){width="128px"}

## 고주파수 조명 취소

**내부:** *필터/조정*

**단순**

</td>
<td style="border: 0;" valign="top">

## 설명

[하이패스](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/highpass/highpass.md)와 비슷하지만, 풀 컬러 이미지에 더 적합합니다(결과물의 채도가 많이 떨어지지는 않음). 이 노드는 높은 빈도의 작은 조명 세부 사항을 취소하려고 합니다.

또한 [조명 취소 저주파수](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/lighting-cancel-low-fre/lighting-cancel-low-frequencies.md) 및 더 진보된 권장 [광도 하이패스](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/luminance-highpass/luminance-highpass.md)를 참조하세요.

## 매개변수

* **강도**: *0.0 -* 1.0\
  조명 취소 효과의 강도입니다.
* **반경**: *0.0 - 10.0*&#x200B;취소할 조명 세부 정보의 반경 또는 크기입니다.

## 예제 이미지

| <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid_items_grid-cell1_position-par_dx_table_row-r0-column-c0_image" src="../../../../../../assets/lighting-cancel-highfrequencies-example.png" width="300px"/></div> |
| --- |
|  |

</td>
</tr>
</table>
