---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/weathering/fabric-weathering.html"
breadcrumb-title: ''
description: Fabric Weathering 노드를 사용하여 메쉬 형상 및 곡률을 기반으로 패브릭 재질에 마모 및 에이징 효과를 추가합니다.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Weathering > Fabric Weathering
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 섬유 풍화
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '483'
ht-degree: 8%

---


# 섬유 풍화

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](fabric-weathering.resources/fabric-weathering.png){width="128px"}

<b>내부:</b> 메시 기반 생성기 > 풍화

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 설명

여러 채널에서 한 번에 작동하는 전체 재질 효과입니다. 그것은 나이와 더러운 것에 대한 제어와 함께 무작위 직물 마모 효과를 추가합니다.<br>이 효과는 제대로 된 AO와 World Space Normalmaps가 연결되어 있지 않으면 제대로 작동하지 않습니다. 이러한 효과를 사용하려면 모든 것을 적절히 계산하고 생성해야 하기 때문입니다.

전체 재질을 사용하여 작업할 때는 [링크 만들기 모드](../../../../../../interface/the-graph-view/link-creation-modes/link-creation-modes.md)를 완전히 이해해야 합니다.

</td>
</tr>
</table>

<a name="inputs"></a>

## 입력

|  |  |
|:---|:---|
| <b>주변 오클루전</b> <i>회색 음영 입력</i> | 내부 효과 및 마스크에 사용되는 베이킹된 맵. |
| <b>일반 월드 공간</b> <i>색상 입력</i> |  |
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
| <b>Dust</b> <i>0.0 - 1.0</i> | 월드 공간 표준 지도에서 위를 향하는 영역을 기반으로 하는 어두운 Dust 효과의 혼합. |
| <b>더러움</b> <i>0.0 - 1.0</i> | 혼합은 주로 AO에서 가려진 영역(어두운 영역)을 기반으로 하는 전역 Dirt/손가락 효과입니다. |
| <b>가장자리 마모</b> <i>0.0 - 1.0</i> | [재질 표준]을 기준으로 가장자리에 선명 효과/격감 효과를 추가합니다. |
| <b>사용됨</b> <i>0.0 - 1.0</i> | 매우 어두운 혼합의 Dirt은 AO를 기반으로 구겨진 상태로 누적됩니다. 최대값 및 최소값은 극단적인 경향이 있으므로 주의해서 사용하십시오. |
| <b>나이</b> <i>0.0 - 1.0</i> | 글로벌 타일링 마모 패턴에 대한 혼합. 아래의 Treshold 컨트롤은 AO 영향을 제어합니다. 최댓값과 최솟값은 극단적인 경향이 있습니다. |
| <b>연령 임계값</b> <i>0.0 - 1.0</i> | AO가 Age 매개 변수에 영향을 주는 정도를 설정합니다. |
| <b>연령 감소</b> <i>0.0 - 1.0</i> | [나이] 효과에서 미세하게 추가 주름의 혼합을 제어합니다. |
| <b>선명한 가장자리 Scratches 크기 조절</b> <i>1.0 - 32.0</i> | 사용된 스크래치 및 노화 효과를 주로 긁어내는 작은 스크래치 비율을 설정합니다. |
| <b>선명한 가장자리 Scratches 뒤틀기 강도</b> <i>0.0 - 1.0</i> | 위의 작은 스크래치에 대한 뒤틀기 강도를 설정합니다. |
| <b>이전 패브릭 채도 감소</b> <i>0.0 - 1.0</i> | [나이] 효과의 채도를 조절합니다. |
| <b>이전 패브릭 밝기</b> <i>0.0 - 1.0</i> | [나이] 효과의 명도를 제어합니다. *이것은 원하는 모양을 얻기 위해 변경하는 데 매우 중요한 매개 변수입니다. 하지만 극단적인 결과를 얻을 수 있습니다. 하위 변경 내용에 사용하십시오.* |
| <b>혼합</b> |  |
| <b>확산 강도</b> <i>0.0 - 1.0</i> | 확산 영역의 혼합 강도입니다. |
| <b>기본 색상 강도</b> <i>0.0 - 1.0</i> | 기본 색상의 혼합 강도입니다. |
| <b>표준 강도</b> <i>0.0 - 1.0</i> | 표준의 혼합 강도입니다. |
| <b>Specular 강도</b> <i>0.0 - 1.0</i> | Specular의 혼합 강도입니다. |
| <b>광택도 강도</b> <i>0.0 - 1.0</i> | 광택의 혼합 강도입니다. |
| <b>거칠음 강도</b> <i>0.0 - 1.0</i> | 거칠기의 혼합 강도입니다. |
| <b>앰비언트 오클루전 강도</b> <i>0.0 - 1.0</i> | 주변 오클루전의 혼합 강도입니다. |
| <b>Height 강도</b> <i>0.0 - 1.0</i> | Height의 혼합 강도입니다. |

## 예

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="fabric-weathering.resources/fabric-ex.gif" />
        </td>
    </tr>
</table>
