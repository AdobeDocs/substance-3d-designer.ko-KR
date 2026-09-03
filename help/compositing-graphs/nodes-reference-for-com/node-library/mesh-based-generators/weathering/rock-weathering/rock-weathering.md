---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/weathering/rock-weathering.html"
breadcrumb-title: ''
description: 암석 풍화 노드를 사용하여 사실적인 침식 효과를 위해 메쉬 형상을 기반으로 암석 표면에 풍화 패턴을 생성합니다.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Weathering > Rock Weathering
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 암석 풍화
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '266'
ht-degree: 16%

---


# 암석 풍화

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](rock-weathering.resources/rock-weathering-01.png){width="128px"}

<b>내부:</b> 메시 기반 생성기 > 풍화

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 설명

</td>
</tr>
</table>

<a name="inputs"></a>

## 입력

|  |  |
|:---|:---|
| <b>주변 오클루전</b> <i>회색 음영 입력</i> | 내부 효과 및 마스크에 사용되는 베이킹된 맵. |
| <b>곡률</b> <i>회색 음영 입력</i> | 내부 효과 및 마스크에 사용되는 베이킹된 맵. |
| <b>일반 WS</b> <i>색상 입력</i> | 내부 효과 및 마스크에 사용되는 Baked World Space Normalmap |
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
| <b>Dust</b> <i>0.0 - 1.0</i> |  |
| <b>더러움</b> <i>0.0 - 1.0</i> |  |
| <b>가장자리 마모</b> <i>0.0 - 1.0</i> |  |
| <b>사용된 바위</b> <i>0.0 - 1.0</i> |  |
| <b>균열 비율</b> <i>1.0 - 60.0</i> |  |
| <b>균열 강도</b> <i>0.0 - 1.0</i> |  |
| <b>나이</b> <i>0.0 - 1.0</i> |  |
| <b>연령 임계값</b> <i>0.0 - 1.0</i> |  |
| <b>선명한 가장자리 Scratches 크기 조절</b> <i>1.0 - 32.0</i> |  |
| <b>선명한 가장자리 Scratches 뒤틀기 강도</b> <i>0.0 - 1.0</i> |  |
| <b>사용된 바위 채도 감소</b> <i>0.0 - 1.0</i> |  |
| <b>사용된 바위 밝기</b> <i>0.0 - 1.0</i> |  |
| <b>혼합</b> |  |
| <b>확산 강도</b> <i>0.0 - 1.0</i> | 확산 영역의 혼합 강도입니다. |
| <b>기본 색상 강도</b> <i>0.0 - 1.0</i> | 기본 색상의 혼합 강도입니다. |
| <b>표준 강도</b> <i>0.0 - 64.0</i> | 표준의 혼합 강도입니다. |
| <b>Specular 강도</b> <i>0.0 - 1.0</i> | Specular의 혼합 강도입니다. |
| <b>광택도 강도</b> <i>0.0 - 1.0</i> | 광택의 혼합 강도입니다. |
| <b>거칠음 강도</b> <i>0.0 - 1.0</i> | 거칠기의 혼합 강도입니다. |
| <b>앰비언트 오클루전 강도</b> <i>0.0 - 1.0</i> | 주변 오클루전의 혼합 강도입니다. |
| <b>Height 강도</b> <i>0.0 - 1.0</i> | Height의 혼합 강도입니다. |

## 예

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="rock-weathering.resources/rock-weathering-02.gif" />
        </td>
    </tr>
</table>
