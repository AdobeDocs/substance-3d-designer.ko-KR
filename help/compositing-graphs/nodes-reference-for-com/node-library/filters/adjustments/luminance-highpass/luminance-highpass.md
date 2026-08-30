---
helpx_url: "https://helpx.adobe.com/kr/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/adjustments/luminance-highpass.html"
breadcrumb-title: ''
description: '[광도 하이패스] 노드를 사용하면 텍스처에서 높은 주파수의 광도 세부 사항을 추출하여 표면 세부 사항을 향상시킬 수 있습니다.'
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Adjustments > Luminance Highpass
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 광도 하이패스
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '102'
ht-degree: 9%

---


# 광도 하이패스

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](luminance-highpass.resources/luminance-highpass.png){width="128px"}

<b>내부:</b> 필터 > 조정

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 설명

입력의 광도 값에 [하이패스](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/highpass/highpass.md)를 수행하여 조명 정보를 취소합니다. 조명 정보를 사용하여 촬영한 텍스처를 수정하는 데 유용합니다. [Substance 3D Designer](https://www.adobe.com/kr/products/substance3d-designer.html)에서 다중 패스와 결합하여 조명 세부 사항의 다른 주파수를 제거할 수 있습니다.

[조명을 사용하여 저주파를 취소하는 것보다 색상을 유지하는 것이 더 낫습니까?](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/lighting-cancel-low-fre/lighting-cancel-low-frequencies.md)

</td>
</tr>
</table>

<a name="parameters"></a>

## 매개변수

|  |  |
|:---|:---|
| <b>반경</b> <i>0.0 - 64.0</i> | 하이패스 효과의 반경입니다. 반경이 작을수록 더 작은 조명이 상쇄되고 입력 이미지에 맞게 조정됩니다. |

## 예

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="luminance-highpass.resources/luminance-highpass-example.png" />
        </td>
    </tr>
</table>
