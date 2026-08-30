---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/mask-generators/edge-select.html"
breadcrumb-title: ''
description: 가장자리 선택 노드를 사용하면 가장자리 기반 풍화 및 마모 효과를 만들기 위해 메시 가장자리를 선택하는 마스크를 생성할 수 있습니다.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Mask Generators > Edge Select
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 가장자리 선택
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '276'
ht-degree: 7%

---


# 가장자리 선택

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](edge-select.resources/edge-select.png){width="128px"}

<b>내부:</b> 메시 기반 생성기 > 마스크 생성기

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 설명

베이킹된 맵 및 사용자 설정을 기반으로 흑백 마스크를 생성합니다. [Painter](https://support.allegorithmic.com/documentation/display/SPDOC/Substance+Painter)의 [스마트 마스크](https://support.allegorithmic.com/documentation/display/SPDOC/Smart+Materials+and+Masks)와 비슷합니다.

이 마스크는 곡률을 기준으로 가장자리를 선택하는 가장 좋은 방법입니다. 어떤 레벨이나 대비에서도 볼록하거나 오목할 수 있으므로 [레벨 노드](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/levels/levels.md)를 통해 이러한 작업을 수동으로 수행하지 않도록 하는 탁월한 단축키를 제공합니다.

</td>
</tr>
</table>

<a name="inputs"></a>

## 입력

|  |  |
|:---|:---|
| <b>곡률</b> <i>회색 음영 입력</i> | 가장자리를 강조하는 데 사용되는 베이킹된 맵. 필수! |
| <b>마스크(선택 사항)</b> <i>회색 음영 입력</i> | 노드의 효과를 마스킹하는 데 사용되는 마스크 슬롯입니다. |

<a name="parameters"></a>

## 매개변수

|  |  |
|:---|:---|
| <b>수준</b> <i>0.0 - 1.0</i> | 볼록 및 오목 모두에 대해 총 가장자리 강조표시 양을 설정합니다. |
| <b>대비</b> <i>0.0 - 1.0</i> | [볼록]과 [오목] 모두에 대해 강조 표시의 대비를 조정합니다. |
| <b>볼록</b> |  |
| <b>볼록 가장자리 너비</b> <i>0.0 - 1.0</i> | 가장자리가 볼록하도록 강조 표시의 폭을 설정합니다. [부드러움]을 약간 늘리면 가장자리가 더 얇아질 수 있습니다. |
| <b>볼록 부드러움</b> <i>0.0 - 1.0</i> | 가장자리가 볼록하도록 전환의 부드러움을 설정합니다. |
| <b>볼록 강도</b> <i>0.0 - 1.0</i> | 가장자리가 볼록할 때의 가장자리 강조 최대 강도를 설정합니다. 강조 표시를 하지 않으려면 0으로 설정합니다. |
| <b>오목</b> |  |
| <b>오목 가장자리 너비</b> <i>0.0 - 1.0</i> | 오목 모서리의 강조표시 폭을 설정합니다. [부드러움]을 약간 늘리면 가장자리가 더 얇아질 수 있습니다. |
| <b>오목 부드러움</b> <i>0.0 - 1.0</i> | 오목 모서리에 대한 변환의 부드러움을 설정합니다. |
| <b>오목 강도</b> <i>0.0 - 1.0</i> | 오목한 가장자리에 대한 가장자리 강조 표시의 최대 강도를 설정합니다. 강조 표시를 하지 않으려면 0으로 설정합니다. |

## 예

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="edge-select.resources/edge-select-ex.gif" />
        </td>
    </tr>
</table>
