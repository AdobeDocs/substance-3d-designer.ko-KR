---
helpx_url: "https://helpx.adobe.com/kr/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/normal-map/normal-vector-rotation.html"
breadcrumb-title: ''
description: '[표준 벡터 회전] 노드를 사용하여 표면 조명 및 세부 방향 조정을 위한 표준 맵 벡터를 회전합니다.'
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Normal Map > Normal Vector Rotation
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 표준 벡터 회전
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '118'
ht-degree: 5%

---


# 표준 벡터 회전

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](normal-vector-rotation.resources/normal-vector-rotation.png){width="128px"}

<b>내부:</b> 필터 > 노멀 맵

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 설명

탄젠트 공간에서 입력 Normalmap의 모든 벡터를 회전하는 표준 유틸리티 노드입니다. 픽셀이 실제로 변형되는 것은 아니며 픽셀이 나타내는 값을 수정합니다. 선택적 맵을 사용하여 회색 음영 측면에 무작위 회전을 추가할 수 있습니다.

</td>
</tr>
</table>

<a name="inputs"></a>

## 입력

|  |  |
|:---|:---|
| <b>표준</b> <i>색상 입력</i> | 회전을 수행할 기본 맵 필수 여부. |
| <b>회전 맵(선택 사항)</b> <i>회색 음영 입력</i> | 회전 강도를 변조하는 회색 음영 맵입니다. |

<a name="parameters"></a>

## 매개변수

|  |  |
|:---|:---|
| <b>회전 각도</b> <i>0.0 - 1.0</i> | 표준 맵을 회전하는 각도를 설정합니다. |
| <b>표준 형식</b> <i>DirectX, OpenGL</i> | 다른 표준 맵 포맷 간 전환(녹색 채널을 반전함) |
