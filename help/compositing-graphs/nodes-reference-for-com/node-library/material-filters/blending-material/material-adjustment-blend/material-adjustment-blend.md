---
helpx_url: "https://helpx.adobe.com/kr/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/blending-material/material-adjustment-blend.html"
breadcrumb-title: ''
description: 재질 조정 블렌드 노드를 사용하여 재질 간에 재질 조정을 블렌딩하여 합성 효과를 미세 조정합니다.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > Blending (Material) > Material Adjustment Blend
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 재질 조정 블렌드
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '373'
ht-degree: 2%

---


# 재질 조정 블렌드

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](material-adjustment-blend.resources/material-adjustment-blend-01.png){width="128px"}

<b>내부:</b> 재질 필터 > 혼합

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 설명

이 노드는 마스크를 기반으로 전체 재질의 모든 채널을 조정할 수 있습니다. 전체 재질 워크플로우를 더 쉽고 빠르게 만들기 위한 것입니다.

이 효과는 동일한 마스크를 기반으로 재질의 몇 가지 채널을 조정하려는 경우(예: 확산을 더 밝게 하고 거칠기를 더 어둡게 하려는 경우)에 유용합니다.

</td>
</tr>
</table>

<a name="inputs"></a>

## 입력

|  |  |
|:---|:---|
| <b>색상 ID 마스크</b> <i>색상 입력</i> | 노드의 효과를 마스킹하는 데 사용되는 마스크 슬롯입니다. |
| <b>회색조 마스크</b> <i>회색 음영 입력</i> | 노드의 효과를 마스킹하는 데 사용되는 마스크 슬롯입니다. |

<a name="parameters"></a>

## 매개변수

|  |  |
|:---|:---|
| <b>채널</b> | 이 그룹에서 재질 채널을 켜거나 끕니다. 예를 들어 [금속]/[거칠음] 대신 [Specular/광택도 맵]을 사용하는 경우.<br><br>이렇게 하면 채널의 관련 그룹 모양이 활성화되고 비활성화됩니다. |
| <b>확산</b> | 마스크에 의해 정의된 영역에서 확산 채널에 대한 조정 작업을 수행합니다. |
| <b>기본 색상</b> | 마스크에 의해 정의된 영역의 [기준 색상] 채널에서 조정 작업을 수행합니다. |
| <b>표준</b> |  |
| <b>강도</b> <i>0.0 - 1.0</i> | 표준 강도를 낮춥니다. |
| <b>Specular</b> | 마스크에 의해 정의된 영역에서 Specular 채널에 대한 조정 작업을 수행합니다. |
| <b>발광</b> | 마스크에 의해 정의된 영역에서 Emissive 채널에 대한 조정 작업을 수행합니다. |
| <b>광택</b> | 마스크에 의해 정의된 영역의 [광도] 채널에서 조정 작업을 수행합니다. |
| <b>거칠음</b> | 마스크에 의해 정의된 영역에서 [거칠음] 채널에 대한 조정 작업을 수행합니다. |
| <b>금속</b> | 마스크에 의해 정의된 영역의 금속 채널에 대해 조정 작업을 수행합니다. |
| <b>Specular level</b> | 마스크에 의해 정의된 영역에서 Specular level 채널에 대한 조정 작업을 수행합니다. |
| <b>주변 오클루전</b> | 마스크에 의해 정의된 영역의 앰비언트 오클루전 채널에 대해 조정 작업을 수행합니다. |
| <b>Height</b> | 마스크에 의해 정의된 영역에서 Height 채널에 대한 조정 작업을 수행합니다. |
| <b>불투명도</b> | 마스크로 정의된 영역의 [불투명도] 채널에서 조정 작업을 수행합니다. |
| <b>색상 ID 마스크</b> <i>거짓/참</i> | 회색 음영 마스크 대신 색상 ID 마스크를 사용하도록 설정합니다. |
| <b>허용량</b> <i>0.01 - 1.0</i> | [색상 ID 마스크]를 활성화하면 색상 ID 선택 색상의 스프레드가 결정됩니다. |
| <b>색상</b> <i>(색상 값)</i> | 색상 ID 맵 및 마스크에서 선택할 색상을 설정합니다. |
| <b>패딩</b> <i>0.0 - 1.0</i> | 색상 ID 마스크의 혼합 대비/전환을 결정합니다. |
