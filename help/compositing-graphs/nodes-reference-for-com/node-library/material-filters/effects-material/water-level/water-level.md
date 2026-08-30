---
helpx_url: "https://helpx.adobe.com/kr/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/effects-material/water-level.html"
breadcrumb-title: ''
description: '[수위] 노드를 사용하면 수위 Height을 기반으로 재질을 블렌딩하여 사실적인 수위 효과를 만들 수 있습니다.'
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > Effects (Material) > Water Level
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 수위
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '282'
ht-degree: 8%

---


# 수위

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](water-level.resources/water-level.png){width="128px"}

<b>내부:</b> 재질 필터 > 효과

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 설명

전체 재질 입력에 수위를 추가하는 올인원 효과입니다. 효과가 작동하려면 입력 재질에 양질의 Heightmap이 있어야 합니다. 결과는 PBR이 올바릅니다.

</td>
</tr>
</table>

<a name="inputs"></a>

## 입력

|  |  |
|:---|:---|
| <b>마스크</b> <i>회색 음영 입력</i> | 노드의 효과를 마스킹하는 데 사용되는 마스크 슬롯입니다. |

<a name="parameters"></a>

## 매개변수

|  |  |
|:---|:---|
| <b>채널</b> | 예를 들어 [금속]/[거칠음] 대신 [Specular/광택] 맵을 사용하는 경우 이 그룹에서 재질 채널을 켜거나 끌 수 있습니다. |
| <b>수위</b> <i>0.0 - 1.0</i> | 수위를 높이거나 낮추기 위한 주 제어. |
| <b>물 농도</b> <i>0.0 - 1.0</i> | 물의 일반적인 &quot;투명도&quot;를 설정합니다. |
| <b>가장자리 젖음</b> <i>0.0 - 1.0</i> | 물의 가장자리가 얼마나 젖어 있는지 결정합니다. |
| <b>가장자리 젖음 거리</b> <i>0.0 - 1.0</i> | 젖은 가장자리가 닿는 거리를 설정합니다. |
| <b>깊이 흐림 정도</b> <i>0.0 - 1.0</i> | 수면 아래의 깊이를 기준으로 흐림 효과의 양을 설정합니다. 흐림 효과 반경을 수정합니다. |
| <b>깊이 흐림 효과 불투명도</b> <i>0.0 - 1.0</i> | 흐림 효과를 낮추는 데 사용할 수 있는 깊이 흐림 효과의 혼합 정도를 결정합니다. |
| <b>슬러지 색상</b> <i>(색상 값)</i> | 슬러지 효과의 색상을 설정합니다. |
| <b>슬러지 깊이</b> <i>0.0 - 1.0</i> | 슬러지가 나타나기 시작하는 깊이를 수위를 기준으로 설정합니다. |
| <b>슬러지 불투명도</b> <i>0.0 - 1.0</i> | 슬러지 효과의 전체 불투명도를 설정합니다. |
| <b>서리</b> <i>0.0 - 1.0</i> | 서리의 양을 설정합니다. 바깥쪽 가장자리에서 시작하여 안쪽으로 이동합니다. |
| <b>서리 강도</b> <i>0.0 - 1.0</i> | 서리의 강도를 설정하고 효과의 &quot;불투명도&quot;를 제어합니다. |
| <b>프로스트 균열</b> <i>0.0 - 1.0</i> | 전환에서 동결에서 액체로 전환되는 균열 양을 설정합니다. |
| <b>일반 형식</b> 프로스트 <i>DirectX/OpenGL</i> | Frost Normalmap 효과 녹색 채널을 전환합니다. |
