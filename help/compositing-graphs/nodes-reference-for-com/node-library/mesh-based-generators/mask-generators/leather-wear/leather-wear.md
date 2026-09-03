---
helpx_url: "https://helpx.adobe.com/kr/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/mask-generators/leather-wear.html"
breadcrumb-title: ''
description: 가죽 마모 노드를 사용하여 메쉬 곡률과 접촉점을 기반으로 가죽 표면에 마모 마스크를 생성합니다.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Mask Generators > Leather Wear
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 가죽 마모
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '253'
ht-degree: 5%

---


# 가죽 마모

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](leather-wear.resources/leather-wear-01.png){width="128px"}

<b>내부:</b> 메시 기반 생성기 > 마스크 생성기

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 설명

베이킹된 맵 및 사용자 설정을 기반으로 흑백 마스크를 생성합니다. [Painter](https://support.allegorithmic.com/documentation/display/SPDOC/Substance+Painter)의 [스마트 마스크](https://support.allegorithmic.com/documentation/display/SPDOC/Smart+Materials+and+Masks)와 비슷합니다.

이 마스크는 가죽 패턴의 마모를 나타내며, 곡률을 기반으로 가장자리가 더 마모됩니다. 기능상 [섬유 유리 Edge Wear](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/mesh-based-generators/mask-generators/fiber-glass-edge-wear/fiber-glass-edge-wear.md)과(와) 비슷하며 대부분 동일한 매개 변수를 사용합니다.

</td>
</tr>
</table>

<a name="inputs"></a>

## 입력

|  |  |
|:---|:---|
| <b>곡률</b> <i>회색 음영 입력</i> | 가장자리 배치에 사용되는 베이킹된 맵. 필수! |
| <b>주변 오클루전</b> <i>회색 음영 입력</i> | 베이킹된 맵은 특정 영역을 폐쇄하는 데 사용되었습니다. 권장되지만 필수는 아닙니다. |
| <b>그런지 입력</b> <i>회색 음영 입력</i> | &quot;사용자 지정 그런지 사용&quot; 매개 변수를 통해 전환할 수 있는 선택적 그런지 맵 입력 슬롯입니다. |
| <b>마스크(선택 사항)</b> <i>회색 음영 입력</i> | 노드의 효과를 마스킹하는 데 사용되는 마스크 슬롯입니다. |

<a name="parameters"></a>

## 매개변수

|  |  |
|:---|:---|
| <b>마모 수준</b> <i>0.0 - 1.0</i> | 전체적인 마모 수준을 설정하여 점진적으로 표시합니다. |
| <b>대비 착용</b> <i>0.0 - 1.0</i> | 효과의 대비를 설정합니다. |
| <b>그런지 양</b> <i>0.0 - 1.0</i> | 가장자리 사이에서 혼합할 그런지(기본 가죽 패턴)의 양을 설정합니다. |
| <b>앰비언트 오클루전 마스크</b> <i>0.0 - 1.0</i> | AO가 마모 효과를 가리는 정도를 설정합니다. |
| <b>곡률 두께</b> <i>0.0 - 1.0</i> | 곡률의 가장자리가 최종 결과에 영향을 주는 정도를 설정합니다. 0으로 설정해도 곡률 맵이 필요합니다. |
| <b>사용자 지정 그런지 사용</b> <i>거짓/참</i> | 기본 내장된 가죽 패턴을 재정의할 수 있습니다. 대신 사용자 정의 입력 슬롯을 사용합니다. |

## 예

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="leather-wear.resources/leather-wear-02.gif" />
        </td>
    </tr>
</table>
