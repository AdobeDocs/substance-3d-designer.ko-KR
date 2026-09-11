---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/normal-map/normal-sobel.html"
breadcrumb-title: ''
description: 표면 세부 사항에 대해 소벨 모서리 검색을 사용하여 높이 맵에서 노멀 맵을 생성하려면 표준 소벨 노드를 사용합니다.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Normal Map > Normal Sobel
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 보통 소벨
user-guide-description: ''
user-guide-title: ''
source-git-commit: 67f8f59bf50387b87e9009b042f269208c665c65
workflow-type: tm+mt
source-wordcount: '79'
ht-degree: 5%

---


# 보통 소벨

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](normal-sobel.resources/normal-hq.png){width="128px"}

<b>내부:</b> 필터 > 노멀 맵

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 설명

Heightmap 입력을 정규맵 출력으로 변환합니다. [일반 Atomic Node](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/normal/normal.md)의 약간 더 진보된 버전인 이 노드는 표준 샘플링 방법이 아닌 Sobel 샘플링을 사용합니다.

</td>
</tr>
</table>

<a name="parameters"></a>

## 매개변수

|  |  |
|:---|:---|
| <b>강도</b> <i>0.0 - 3.0</i> | 변환된 표준의 강도입니다. |
| <b>표준 형식</b> <i>OpenGL, DirectX</i> | 서로 다른 표준 맵 포맷 사이를 전환합니다(녹색 채널을 반전합니다). |
