---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/flood-fill-to-gradient.html"
breadcrumb-title: ''
description: '[그레이디언트 Flood Fill] 노드를 사용하여 부드러운 색상 전환을 만들기 위해 그레이디언트 값으로 영역을 채웁니다.'
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Flood Fill to Gradient
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 그레이디언트로 Flood Fill
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '206'
ht-degree: 7%

---


# 그레이디언트로 Flood Fill

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](flood-fill-to-gradient.resources/floodfill-to-gradient.png){width="128px"}

<b>인:</b> 필터 > 효과

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 설명

[임의 그레이디언트(임의 그레이디언트)로 &#x200B;](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/flood-fill/flood-fill.md)Flood Fill 타일이 임의로 기울어진 높이 맵을 만드는 데 매우 유용합니다.

</td>
</tr>
</table>

<a name="inputs"></a>

## 입력

|  |  |
|:---|:---|
| <b>Flood Fill</b> <i>색상 입력</i> | 기본 Flood Fill 데이터. |
| <b>각도 입력</b> <i>회색 음영 입력</i> | 외부 맵을 사용하여 셀별 각도를 결정하는 옵션 맵 |
| <b>경사 입력</b> <i>회색 음영 입력</i> | 셀별 그레이디언트 경사 강도를 결정하는 선택적 맵입니다. |

<a name="parameters"></a>

## 매개변수

|  |  |
|:---|:---|
| <b>각도</b> <i>0.0 - 1.0</i> | 모든 타일에 대해 균일한 글로벌 각도/방향을 설정합니다. |
| <b>각도 변형</b> <i>0.0 - 1.0</i> | 각 타일의 각도를 개별적으로 임의화합니다. 이것은 가장 유용하고 강력한 매개 변수입니다! |
| <b>테두리 상자 크기에 곱하기</b> <i>0.0 - 1.0</i> | 타일의 개별 테두리 상자 크기에 따라 전체 선형 효과의 크기를 조절합니다. 즉, 더 작은 타일이 더 큰 타일보다 더 어두워집니다. |
| <b>각도 이미지 입력 승수</b> <i>0.0 - 1.0</i> | 생성된 그레이디언트 방향에 대한 선택적 각도 입력 맵의 영향 설정 |
| <b>경사 이미지 입력 승수</b> <i>0.0 - 1.0</i> | 생성된 그레이디언트 경사 강도에 대한 선택적 경사 입력 맵의 영향을 설정합니다. |
| <b>경사 강도로 곱하기</b> <i>0.0 - 1.0</i> |  |
| <b>플랫 경사 색상</b> <i>(회색 음영 값)</i> | 플랫 경사에 대해 실선 값을 설정할 수 있습니다. |

## 예

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="flood-fill-to-gradient.resources/floodgradient-ex2.png" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="flood-fill-to-gradient.resources/floodgradient-ex1.png" />
        </td>
    </tr>
</table>
