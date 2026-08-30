---
helpx_url: "https://helpx.adobe.com/kr/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/mask-generators/paint-wear.html"
breadcrumb-title: ''
description: 페인트 마모 노드를 사용하면 메시 형상을 기반으로 사실적인 페인트 조각 효과를 만들 수 있는 페인트 마모 마스크를 생성할 수 있습니다.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Mask Generators > Paint Wear
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 페인트 마모
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '202'
ht-degree: 6%

---


# 페인트 마모

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](paint-wear.resources/paint-wear.png){width="128px"}

<b>내부:</b> 메시 기반 생성기 > 마스크 생성기

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 설명

베이킹된 맵 및 사용자 설정을 기반으로 흑백 마스크를 생성합니다. [Painter](https://support.allegorithmic.com/documentation/display/SPDOC/Substance+Painter)의 [스마트 마스크](https://support.allegorithmic.com/documentation/display/SPDOC/Smart+Materials+and+Masks)와 비슷합니다.

이 마스크는 페인트가 벗겨져 가장자리가 닳아 없어지는 것을 나타냅니다.

</td>
</tr>
</table>

<a name="inputs"></a>

## 입력

|  |  |
|:---|:---|
| <b>주변 오클루전</b> <i>회색 음영 입력</i> | 내부 효과 및 마스크에 사용되는 베이킹된 맵. |
| <b>곡률</b> <i>회색 음영 입력</i> | 내부 효과 및 마스크에 사용되는 베이킹된 맵. |
| <b>변형 마스크</b> <i>회색 음영 입력</i> | 노드의 효과를 마스킹하는 데 사용되는 마스크 슬롯입니다. |
| <b>마스크(선택 사항)</b> <i>회색 음영 입력</i> | 노드의 효과를 마스킹하는 데 사용되는 마스크 슬롯입니다. |

<a name="parameters"></a>

## 매개변수

|  |  |
|:---|:---|
| <b>수준</b> <i>0.0 - 1.0</i> | 페인트 마모의 전체 양을 설정하여 점진적으로 표시합니다. |
| <b>대비</b> <i>0.0 - 1.0</i> | 결과의 대비를 조정합니다. |
| <b>오클루전</b> <i>0.0 - 1.0</i> | 구워진 AO가 어두운 영역에서의 마모를 방지하는 데 미치는 영향의 양을 설정합니다. |
| <b>반경</b> <i>0.0 - 2.0</i> | 볼록 가장자리에서 치핑 효과가 확산되는 거리를 설정합니다. |
| <b>변형</b> <i>0.0 - 1.0</i> | 효과에 혼합할 변형 양(그런지)을 설정합니다. |
| <b>변형 마스크 재정의</b> <i>거짓/참</i> | 사용자 지정 변형(그런지) 맵 입력 슬롯을 사용합니다. |

## 예

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="paint-wear.resources/paint-wear-ex.gif" />
        </td>
    </tr>
</table>
