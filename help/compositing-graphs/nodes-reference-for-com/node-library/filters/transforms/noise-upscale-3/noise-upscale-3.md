---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/transforms/noise-upscale-3.html"
breadcrumb-title: ''
description: 높은 해상도에서 세부 사항을 유지하기 위해 고급 노이즈 기반 알고리즘을 사용하여 텍스처를 확대하려면 노이즈 확대/축소 3 노드를 사용합니다.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Transforms > Noise Upscale 3
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 노이즈 고급 3
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '132'
ht-degree: 2%

---


# 노이즈 고급 3

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](noise-upscale-3.resources/noise-upscale.png){width="128px"}

<b>필터</b>:

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 설명

입력 노이즈를 절차적으로 가져와 최대 2배의 해상도로 크기를 조절하며, 세부 사항은 유지하지만 너무 많은 타일링을 가져오지 않습니다. 사용자정의 마스크를 사용하여 원본 비율 위에 노이즈를 혼합합니다.

이 노드는 대부분 크고 무거운 노이즈를 사용하는 느린 그래프를 최적화하기 위한 것입니다. 이를 통해 너무 많은 추가 컴퓨팅 시간을 도입하지 않고도 더 높은 해상도를 사용할 수 있습니다.

대부분의 경우 타일링을 숨기는 것이 더 나은 경향이 있는 [노이즈 확대 1](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/transforms/noise-upscale-1/noise-upscale-1.md) 및 [노이즈 확대 2](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/transforms/noise-upscale-2/noise-upscale-2.md)을(를) 참조하십시오.

</td>
</tr>
</table>

<a name="inputs"></a>

## 입력

|  |  |
|:---|:---|
| <b>회색 음영</b> <i>회색 음영 입력</i> | 대상 노이즈 이미지입니다. |
| <b>마스크</b> <i>회색 음영 입력</i> | 노드의 효과를 마스킹하는 데 사용되는 마스크 슬롯입니다. |

## 예

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="noise-upscale-3.resources/noise3ex.png" />
        </td>
    </tr>
</table>
