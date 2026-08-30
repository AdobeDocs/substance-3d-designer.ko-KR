---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/mask-generators/edge-damages.html"
breadcrumb-title: ''
description: '[가장자리 손상] 노드를 사용하면 메시 가장자리에 손상 마스크를 생성하여 사실적인 가장자리 마모 및 파손 효과를 만들 수 있습니다.'
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Mask Generators > Edge Damages
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 가장자리 손상
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '152'
ht-degree: 6%

---


# 가장자리 손상

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](edge-damages.resources/edge-damages.png){width="128px"}

<b>내부:</b> 메시 기반 생성기 > 마스크 생성기

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 설명

베이킹된 맵 및 사용자 설정을 기반으로 흑백 마스크를 생성합니다. [Painter](https://support.allegorithmic.com/documentation/display/SPDOC/Substance+Painter)의 [스마트 마스크](https://support.allegorithmic.com/documentation/display/SPDOC/Smart+Materials+and+Masks)와 비슷합니다.

이 마스크는 곡률 및 베이킹된 AO를 기반으로 하여 상승된 볼록 에지에 대한 손상을 나타낸다.

</td>
</tr>
</table>

<a name="inputs"></a>

## 입력

|  |  |
|:---|:---|
| <b>곡률</b> <i>회색 음영 입력</i> | 효과 배치에 사용되는 베이킹된 맵. 필수! |
| <b>주변 오클루전</b> <i>회색 음영 입력</i> | 효과 배치에 사용되는 베이킹된 맵. 필수! |
| <b>마스크(선택 사항)</b> <i>회색 음영 입력</i> | 노드의 효과를 마스킹하는 데 사용되는 마스크 슬롯입니다. |

<a name="parameters"></a>

## 매개변수

|  |  |
|:---|:---|
| <b>수준</b> <i>0.0 - 1.0</i> | 적용할 가장자리 손상의 양입니다. |
| <b>대비</b> <i>0.0 - 1.0</i> | 결과의 대비를 조정합니다. |
| <b>손상 강도</b> <i>0.0 - 1.0</i> | 낡고, 일관된 모습과 혼란스럽고, 긁히고, 심하게 손상된 모습 사이의 변화. |

## 예

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="edge-damages.resources/edge-damages-ex.gif" />
        </td>
    </tr>
</table>
