---
helpx_url: "https://helpx.adobe.com/kr/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/weathering/cracks-weathering.html"
breadcrumb-title: ''
description: 균열 풍화 노드를 사용하여 메쉬 곡률과 응력점을 기반으로 재료에 균열 패턴을 추가합니다.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Weathering > Cracks Weathering
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 균열 웨더링
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '210'
ht-degree: 3%

---


# 균열 웨더링

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](cracks-weathering.resources/cracks-weathering-01.png){width="128px"}

<b>내부:</b> 메시 기반 생성기 > 풍화

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 설명

여러 채널에서 한 번에 작동하는 전체 재질 효과입니다. 스프레드와 깊이를 제어하는 무작위 크랙 패턴을 추가합니다.

전체 재질을 사용하여 작업할 때는 [링크 만들기 모드](../../../../../../interface/the-graph-view/link-creation-modes/link-creation-modes.md)를 올바르게 이해해야 합니다.

</td>
</tr>
</table>

<a name="inputs"></a>

## 입력

|  |  |
|:---|:---|
| <b>곡률</b> <i>회색 음영 입력</i> | 내부 효과 및 마스크에 사용되는 구워지거나 생성된 맵 |
| <b>Height</b> <i>회색 음영 입력</i> | 내부 효과 및 마스크에 사용되는 구워지거나 생성된 맵 |
| <b>마스크</b> <i>회색 음영 입력</i> | 노드의 효과를 마스킹하는 데 사용되는 마스크 슬롯입니다. &quot;마스크&quot; 매개 변수로 전환할 수 있습니다. |

<a name="parameters"></a>

## 매개변수

|  |  |
|:---|:---|
| <b>채널</b> | 예를 들어 [금속]/[거칠음] 대신 [Specular/광택] 맵을 사용하는 경우 이 그룹에서 재질 채널을 켜거나 끌 수 있습니다. |
| <b>고급</b> |  |
| <b>표준 형식</b> <i>DirectX, OpenGL</i> | 서로 다른 표준 맵 포맷 사이를 전환합니다(녹색 채널을 반전합니다). |
| <b>마스크</b> <i>거짓/참</i> | 마스크 맵 사용을 설정하거나 해제합니다. |
| <b>효과</b> |  |
| <b>균열 전파</b> <i>0.0 - 1.0</i> | 균열의 확산 범위입니다. 이 효과의 기본 컨트롤입니다. |
| <b>균열 깊이</b> <i>0.0 - 1.0</i> | 균열 효과의 깊이. 이는 대부분 Height에 영향을 미치고, 시각적 Thickness에 약간 영향을 미친다. |
| <b>혼합</b> | 각 결과 채널에 효과가 얼마나 강하게 혼합되는지 제어합니다. |

## 예

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="cracks-weathering.resources/cracks-weathering-02.gif" />
        </td>
    </tr>
</table>
