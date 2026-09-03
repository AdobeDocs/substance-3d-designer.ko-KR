---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/effects-material/material-height-blend.html"
breadcrumb-title: ''
description: '[재질 Height 혼합] 노드를 사용하면 레이어 재질 효과를 만들기 위해 Height 맵을 기반으로 여러 재질을 혼합할 수 있습니다.'
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > Effects (Material) > Material Height Blend
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 재질 Height 혼합
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '203'
ht-degree: 4%

---


# 재질 Height 혼합

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](material-height-blend.resources/material-height-blend-01.png){width="128px"}

<b>내부:</b> 재질 필터 > 효과

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 설명

이 노드는 두 재질을 높이 맵을 기준으로 혼합하는 [Height 혼합](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/effects-material/height-blend/height-blend.md)의 고급 버전입니다. 사용자정의 마스크가 없으므로 각 재질에 대해 하나씩 두 개의 [높이 맵]이 있어야 하며 이 중 하나 이상은 균일 값이 아닙니다.

이는 고품질 혼합 마스크 없이 서로 다른 두 개의 고품질 재료를 결합하는 데 유용할 수 있습니다.

물이나 눈 속에서 섞이고 싶다면 [Snow 표지](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/effects-material/snow-cover/snow-cover.md) 및 [수위](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/effects-material/water-level/water-level.md) 노드를 대신 사용할 수 있습니다.

</td>
</tr>
</table>

<a name="parameters"></a>

## 매개변수

|  |  |
|:---|:---|
| <b>채널</b> | 예를 들어 [금속]/[거칠음] 대신 [Specular/광택] 맵을 사용하는 경우 이 그룹에서 재질 채널을 켜거나 끌 수 있습니다. |
| <b>Height 오프셋</b> <i>0.0 - 1.0</i> | 블렌드 레벨이 Height 축을 따라 이동되도록 높이 맵을 오프셋합니다. 혼합에 대한 기본 컨트롤입니다. |
| <b>대비</b> <i>0.0 - 1.0</i> | 혼합의 대비를 조정하고 전환을 더 선명하게 합니다. |
| <b>모드</b> <i>균형 잡힌 Height, 하위 Height 우선 순위</i> |  |
| <b>불투명도</b> <i>0.0 - 1.0</i> | 전경 Height의 불투명도를 혼합하면 안쪽이나 바깥쪽으로 페이드됩니다. |
| <b>알베도 일치</b> <i>0.0 - 1.0</i> | 알베도 색상 간에 수행할 내부 색상 일치의 양입니다. |
