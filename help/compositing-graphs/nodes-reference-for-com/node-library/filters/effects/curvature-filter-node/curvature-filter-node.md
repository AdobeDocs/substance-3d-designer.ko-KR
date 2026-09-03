---
helpx_url: "https://helpx.adobe.com/kr/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/curvature-filter-node.html"
breadcrumb-title: ''
description: 곡률 필터 노드를 사용하여 볼록 및 오목 서피스를 감지하기 위해 Height 맵에서 곡률 맵을 생성합니다.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Curvature (Filter Node)
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 곡률(필터 노드)
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '123'
ht-degree: 4%

---


# 곡률(필터 노드)

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](curvature-filter-node.resources/curvature-filter-node-01.png){width="128px"}

<b>인:</b> 필터 > 효과

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 설명

입력 [Normalmap](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/normal/normal.md)에 대해 간단하고 거친 단일 패스 곡률 변환을 수행합니다. 그 결과로 생성된 맵에는 볼록 영역의 흰색 색조와 오목 영역의 검은색 색조가 있습니다. 곡률은 항상 픽셀 가는 선과 선명한 전환을 생성합니다.

이 노드는 특정 가장자리를 빠르게 강조 표시하거나 어둡게 하는 데 유용합니다. 이는 [곡률 매끄럽게](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/curvature-smooth/curvature-smooth.md)(더 높은 품질 결과 생성) 및 [곡률 소벨](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/curvature-sobel/curvature-sobel.md)(더 많은 옵션 제공)과 비교하여 제한됩니다.

</td>
</tr>
</table>

<a name="parameters"></a>

## 매개변수

|  |  |
|:---|:---|
| <b>강도</b> <i>0.0 - 10.0</i> | 효과의 강도입니다. 결과의 대비를 높입니다. |
| <b>표준 형식</b> <i>DirectX, OpenGL</i> | 서로 다른 표준 맵 포맷 사이를 전환합니다(녹색 채널을 반전합니다). |

## 예

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="curvature-filter-node.resources/curvature-filter-node-02.png" />
        </td>
    </tr>
</table>
