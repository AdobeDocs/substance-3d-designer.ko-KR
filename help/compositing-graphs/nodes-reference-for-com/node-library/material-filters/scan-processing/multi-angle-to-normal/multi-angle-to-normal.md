---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/scan-processing/multi-angle-to-normal.html"
breadcrumb-title: ''
description: '[다중 각도와 표준] 노드를 사용하면 정확한 표면 세부 묘사를 위해 다중 각도 스캔 이미지에서 노멀 맵을 생성할 수 있습니다.'
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > Scan Processing > Multi-Angle to Normal
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 다중 각도에서 표준으로
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '245'
ht-degree: 3%

---


# 다중 각도에서 표준으로

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](multi-angle-to-normal.resources/multi-angle-to-normal-01.png){width="128px"}

<b>내부:</b> 재질 필터 > 스캔 처리

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 설명

이 노드는 다른 조명 조건에서 만들어진 사진/스캔 세트로부터 정규맵을 구성한다. 하나의 단일 알베도 이미지에서 표준을 추출할 때보다 훨씬 더 정확한 표준맵 변환을 수행할 수 있습니다.

입력에 대해 설정된 정확한 조명 각도를 사용해야 하므로 [알베도에 대한 다중 각도](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/multi-angle-to-albedo/multi-angle-to-albedo.md)보다 복잡합니다. 모든 샘플의 조명 각도는 균등한 간격으로 배치되어야 하고 샘플은 순서대로 입력해야 합니다. 따라서 3개의 샘플의 경우 조명 각도는 0, 120, 240 또는 90, 210, 330과 같은 그 어떤 균일한 오프셋에서 취해야 합니다.

>[!NOTE]
>
> 이 알베도의 알베도 버전은 [다중 각도 대 노드](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/multi-angle-to-albedo/multi-angle-to-albedo.md)를 참조하십시오. 입력을 사전 처리하려면 [다중 Color Equalizer](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/multi-color-equalizer/multi-color-equalizer.md), [다중 자르기](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/multi-crop/multi-crop.md) 및 [다중 복제 패치](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/multi-clone-patch/multi-clone-patch.md)를 사용할 수 있습니다. 이러한 노드를 결합해야 합니다.

</td>
</tr>
</table>

<a name="inputs"></a>

## 입력

|  |  |
|:---|:---|
| <b>입력 1-8</b> <i>색상 입력</i> |  |

<a name="parameters"></a>

## 매개변수

|  |  |
|:---|:---|
| <b>표준 형식</b> <i>DirectX, OpenGL</i> | 서로 다른 표준 맵 포맷 사이를 전환합니다(녹색 채널을 반전합니다). |
| <b>샘플 양</b> <i>2 - 8</i> | 처리할 샘플(입력) 양을 설정합니다. |
| <b>강도</b> <i>0.0 - 1.0</i> | 표준 맵 강도를 설정합니다. |
| <b>첫 번째 샘플 조명 각도</b> <i>0.0 - 360.0</i> | 첫 번째 입력의 조명 각도 방향을 설정합니다. |
| <b>다음 샘플 조명 각도</b> <i>시계 반대 방향, 시계 방향</i> | 다음 샘플의 조명이 이동하는 방향을 설정합니다. |
