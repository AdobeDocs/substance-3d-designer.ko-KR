---
helpx_url: "https://helpx.adobe.com/kr/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/normal-map/height-to-normal-world-units.html"
breadcrumb-title: ''
description: '[Height에서 일반 세계 단위로] 노드를 사용하면 정확한 세부 정보를 위해 세계 단위 비율을 사용하여 높이 맵을 노멀 맵으로 변환할 수 있습니다.'
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Normal Map > Height to Normal World Units
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 일반 월드 단위로 Height
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '122'
ht-degree: 4%

---


# 일반 월드 단위로 Height

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](height-to-normal-world-units.resources/height-to-normal-world-units-01.png){width="128px"}

<b>내부:</b> 필터 > 노멀 맵

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 설명

변환 중에 실제 단위를 사용하는 고급 Height-일반 변환 노드입니다.

소스 Heightmap의 크기를 알고 스캔한 재질 등을 사용하여 작업하는 경우와 같이 가장 정확한 변환을 수행하려는 경우에 유용합니다.

</td>
</tr>
</table>

<a name="parameters"></a>

## 매개변수

|  |  |
|:---|:---|
| <b>표면 크기(cm)</b> <i>0.0 - 1000.0</i> | 입력 Heightmap의 Dimension |
| <b>Height 깊이(cm)</b> <i>0.0 - 100.0</i> | Heightmap 세부 정보의 최대 깊이. |
| <b>표준 형식</b> <i>OpenGL, DirectX</i> | 서로 다른 표준 맵 포맷 사이를 전환합니다(녹색 채널을 반전합니다). |
| <b>샘플링</b> <i>표준, Sobel</i> | 정확도를 결정하는 두 샘플링 모드 간의 전환입니다. |
