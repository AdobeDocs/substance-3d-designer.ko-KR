---
helpx_url: "https://helpx.adobe.com/kr/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/scan-processing/ao-cancellation.html"
breadcrumb-title: ''
description: AO 취소 노드를 사용하여 깨끗한 텍스처 처리를 위해 스캔한 재질에서 주변 오클루전을 제거합니다.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > Scan Processing > AO Cancellation
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: AO 취소
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '133'
ht-degree: 4%

---


# AO 취소

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](ao-cancellation.resources/ao-cancellation-01.png){width="128px"}

<b>내부:</b> 재질 필터 > 스캔 처리

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 설명

이 노드는 별도의 AO 맵 입력을 기반으로 알베도(기본 색상) 맵에서 앰비언트 오클루전 조명 정보를 제거하려고 시도합니다. 알베도 정보가 PBR로 정확하고 대부분 (강한) 조명 정보가 없는지 확인하는 데 사용할 수 있습니다.

스캔한 메쉬에서 AO 맵을 불러올 때 또는 Height 또는 일반 정보에서 생성된 AO 맵을 불러올 때 유용한 노드입니다.

</td>
</tr>
</table>

<a name="parameters"></a>

## 매개변수

|  |  |
|:---|:---|
| <b>AO 취소</b> <i>0.0 - 1.0</i> | 조명 정보를 제거하는 강도입니다. |
| <b>AO 채도</b> <i>0.0 - 1.0</i> | (De)조명이 제거된 영역에 대한 채도 보상. 이를 사용하여 어두운 영역에서 색상 손실을 되돌릴 수 있습니다. |
