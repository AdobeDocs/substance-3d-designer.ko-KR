---
helpx_url: "https://helpx.adobe.com/kr/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/mask-generators/bottom-to-top.html"
breadcrumb-title: ''
description: '[아래에서 위로] 노드를 사용하여 메시 세계 위치를 기준으로 아래에서 위로 그레이디언트 마스크를 생성합니다.'
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Mask Generators > Bottom To Top
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 아래에서 위로
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '199'
ht-degree: 5%

---


# 아래에서 위로

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](bottom-to-top.resources/bottom-to-top-01.png){width="128px"}

<b>내부:</b> 메시 기반 생성기 > 마스크 생성기

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 설명

베이킹된 맵 및 사용자 설정을 기반으로 흑백 마스크를 생성합니다. [Painter](https://experienceleague.adobe.com/ko/docs/substance-3d-painter/using/home)의 [스마트 마스크](https://experienceleague.adobe.com/ko/docs/substance-3d-painter/using/features/smart-materials-and-masks)와 비슷합니다.

그러면 모델의 아래쪽에서 위쪽으로 흰색에서 검정으로 전환되어 형상 기반 밝기 감소 및 선택 영역을 만드는 데 유용합니다.

</td>
</tr>
</table>

<a name="inputs"></a>

## 입력

|  |  |
|:---|:---|
| <b>위치</b> <i>색상 입력</i> | 위치 맵을 구웠습니다. 필수! |
| <b>거칠음</b> <i>회색 음영 입력</i> | 이는 PBR 거칠음과는 무관하지만 전환을 나누기 위한 (선택 사항) 변형 맵입니다. [거칠음]이 0보다 높게 설정된 경우에만 표시됩니다. |
| <b>마스크(선택 사항)</b> <i>회색 음영 입력</i> | 노드의 효과를 마스킹하는 데 사용되는 마스크 슬롯입니다. |

<a name="parameters"></a>

## 매개변수

|  |  |
|:---|:---|
| <b>수준</b> <i>0.0 - 1.0</i> | 명도 조정처럼 결과의 평균 레벨을 검정색이나 흰색으로 이동합니다. |
| <b>대비</b> <i>0.0 - 1.0</i> | 전환의 대비를 조정합니다. |
| <b>거칠음_변형</b> <i>0.0 - 1.0</i> | 변형을 위해 혼합할 거칠기 맵의 양을 결정합니다. 이 값을 0으로 늘리면 맵 슬롯이 표시됩니다. |

## 예

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="bottom-to-top.resources/bottom-to-top-02.gif" />
        </td>
    </tr>
</table>
