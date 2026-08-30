---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/mask-generators/metal-edge-wear.html"
breadcrumb-title: ''
description: 금속 Edge Wear 노드를 사용하여 메쉬 곡률과 위치를 기반으로 금속 가장자리에 마모 마스크를 생성합니다.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Mask Generators > Metal Edge Wear
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 금속 Edge Wear
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '279'
ht-degree: 7%

---


# 금속 Edge Wear

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](metal-edge-wear.resources/metal-edge-wear.png){width="128px"}

<b>내부:</b> 메시 기반 생성기 > 마스크 생성기

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 설명

베이킹된 맵 및 사용자 설정을 기반으로 흑백 마스크를 생성합니다. [Painter](https://support.allegorithmic.com/documentation/display/SPDOC/Substance+Painter)의 [스마트 마스크](https://support.allegorithmic.com/documentation/display/SPDOC/Smart+Materials+and+Masks)와 비슷합니다.

이 마스크는 금속 오브젝트의 가장자리 마모를 나타내며, 가장자리가 볼록하게 솟아오른 곳에 스크래치와 칩이 표시되어 구운 AO 어두운 영역으로 마스크될 수 있습니다.

</td>
</tr>
</table>

<a name="inputs"></a>

## 입력

|  |  |
|:---|:---|
| <b>곡률</b> <i>회색 음영 입력</i> | 내부 효과 및 마스크에 사용되는 베이킹된 맵. |
| <b>주변 오클루전</b> <i>회색 음영 입력</i> | 내부 효과 및 마스크에 사용되는 베이킹된 맵. |
| <b>그런지 입력</b> <i>회색 음영 입력</i> |  |
| <b>마스크(선택 사항)</b> <i>회색 음영 입력</i> | 노드의 효과를 마스킹하는 데 사용되는 마스크 슬롯입니다. |
| <b>월드 스페이스 표준</b> <i>색상 입력</i> |  |
| <b>위치</b> <i>색상 입력</i> |  |

<a name="parameters"></a>

## 매개변수

|  |  |
|:---|:---|
| <b>마모 수준</b> <i>0.0 - 1.0</i> | 점진적으로 드러나는 마모의 총 양을 설정합니다. |
| <b>대비 착용</b> <i>0.0 - 1.0</i> | 최종 결과의 대비를 설정합니다. |
| <b>가장자리 Smoothness</b> <i>0.0 - 16.0</i> | 곡률의 모서리에서 밝기 감소 Smoothness을 설정합니다. |
| <b>그런지 양</b> <i>0.0 - 1.0</i> | 가장자리 사이에서 혼합할 그런지 양을 설정합니다. |
| <b>그런지 크기</b> <i>1 - 16</i> | 그런지 배율을 설정합니다. |
| <b>앰비언트 오클루전 마스크</b> <i>0.0 - 1.0</i> | AO가 마스킹되는 어두운 영역인 최종 효과에 미치는 영향의 양을 설정합니다. |
| <b>곡률 두께</b> <i>0.0 - 1.0</i> | [곡률]의 [볼록] 가장자리가 최종 효과에 미치는 영향의 양을 설정합니다. |
| <b>사용자 지정 그런지 사용</b> <i>거짓/참</i> | 사용자 지정 그런지 맵 입력 슬롯을 활성화합니다. |
| <b>Triplanar 사용</b> <i>거짓/참</i> | 솔기를 숨기려면 [평면](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/mesh-based-generators/utilities-mesh-based-gen/tri-planar/tri-planar.md) 프로젝션을 사용하세요. |
| <b>삼평면 혼합 대비</b> <i>0.0 - 1.0</i> | 삼면형 투영의 혼합 대비를 설정합니다. |

## 예

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="metal-edge-wear.resources/metal-edge-wear-ex.gif" />
        </td>
    </tr>
</table>
