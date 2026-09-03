---
helpx_url: "https://helpx.adobe.com/kr/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/normal-map/normal-transform.html"
breadcrumb-title: ''
description: 벡터 방향을 올바르게 유지하면서 노멀 맵에 변환을 적용하려면 일반 변환 노드를 사용합니다.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Normal Map > Normal Transform
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Normal
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '101'
ht-degree: 3%

---


# Normal

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](normal-transform.resources/normal-transform-01.png){width="128px"}

<b>내부:</b> 필터 > 노멀 맵

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 설명

원자 변환 2D 노드와 유사하게, 이것은 탄젠트-공간을 파괴하지 않고 노말맵의 변환을 허용하지만, 대신 그것은 항상 정확한 노말맵으로 재계산된다.

</td>
</tr>
</table>

<a name="parameters"></a>

## 매개변수

|  |  |
|:---|:---|
| <b>Matrix2x2</b> <i>(변환 행렬):</i> | 입력을 회전하거나 크기를 조정합니다. |
| <b>오프셋</b> <i>-0.5 - 0.5</i> | 결과를 이동하거나 변환합니다. 변형 컨트롤이 있으면 캔버스와 직접 상호 작용하여 결과를 수정할 수 있습니다. |
| <b>표준 형식</b> <i>DirectX, OpenGL</i> | 다른 표준 맵 포맷 간 전환(녹색 채널을 반전함) |
