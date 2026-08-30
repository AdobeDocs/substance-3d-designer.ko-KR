---
helpx_url: "https://helpx.adobe.com/kr/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/mask-generators/dirt.html"
breadcrumb-title: ''
description: Dirt 노드를 사용하여 메쉬 곡률, 위치, 오클루전을 기반으로 Dirt 누적 마스크를 생성합니다.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Mask Generators > Dirt
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 흙
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '252'
ht-degree: 7%

---


# 흙

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](dirt.resources/dirt.png){width="128px"}

<b>내부:</b> 메시 기반 생성기 > 마스크 생성기

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 설명

베이킹된 맵 및 사용자 설정을 기반으로 흑백 마스크를 생성합니다. [Painter](https://support.allegorithmic.com/documentation/display/SPDOC/Substance+Painter)의 [스마트 마스크](https://support.allegorithmic.com/documentation/display/SPDOC/Smart+Materials+and+Masks)와 비슷합니다.

이 마스크는 적용된 AO 및 곡률을 기반으로, 오목하고 함몰된 가장자리 및 모퉁이의 Dirt을 나타냅니다.

</td>
</tr>
</table>

<a name="inputs"></a>

## 입력

|  |  |
|:---|:---|
| <b>곡률</b> <i>회색 음영 입력</i> | 내부 효과 및 마스크에 사용되는 베이킹된 맵. 필수! |
| <b>주변 오클루전</b> <i>회색 음영 입력</i> | 내부 효과 및 마스크에 사용되는 베이킹된 맵. 필수! |
| <b>그런지 입력</b> <i>회색 음영 입력</i> | 사용자 정의 그런지 맵 입력(선택 사항), 매개 변수에 의해 활성화됨 |
| <b>마스크(선택 사항)</b> <i>회색 음영 입력</i> | 노드의 효과를 마스킹하는 데 사용되는 마스크 슬롯입니다. |
| <b>월드 스페이스 표준</b> <i>색상 입력</i> | Triplanar에만 사용됩니다. |
| <b>위치</b> <i>색상 입력</i> | Triplanar에만 사용됩니다. |

<a name="parameters"></a>

## 매개변수

|  |  |
|:---|:---|
| <b>Dirt 수준</b> <i>0.0 - 1.0</i> | Dirt 양에 대한 기본 컨트롤입니다. |
| <b>Dirt 대비</b> <i>0.0 - 1.0</i> | 마스크에 있는 Dirt의 기본 대비를 제어합니다. |
| <b>그런지 양</b> <i>0.0 - 1.0</i> | Dirt의 그런지 정도를 설정합니다. 완벽한 Dirt을 위해 0으로 설정합니다. |
| <b>가장자리 마스크</b> <i>0.0 - 1.0</i> | 융기된 모서리에서 제거할 Dirt 양입니다(곡률 맵에 따라 다름). |
| <b>사용자 지정 그런지 사용</b> <i>거짓/참</i> | 기본 제공 그런지 대신 사용자 지정 그런지 맵 입력을 사용할 수 있도록 합니다. |
| <b>그런지 크기</b> <i>1 - 16</i> | 그런지 세부 사항의 타일링 비율을 설정합니다. |
| <b>Triplanar 사용</b> <i>거짓/참</i> | 그런지 매핑에 [삼평면 투영](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/mesh-based-generators/utilities-mesh-based-gen/tri-planar/tri-planar.md)을 사용하여 이음새를 제거합니다. |
| <b>삼평면 혼합 대비</b> <i>0.001 - 1.0</i> | 삼면형 투영의 대비를 설정합니다. |

## 예

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="dirt.resources/dirt-ex.gif" />
        </td>
    </tr>
</table>
