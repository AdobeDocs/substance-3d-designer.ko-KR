---
helpx_url: "https://helpx.adobe.com/kr/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/scan-processing/multi-angle-to-albedo.html"
breadcrumb-title: ''
description: '[다중 각도와 알베도] 노드를 사용하여 다중 각도 스캔 이미지에서 깔끔한 재질 색상을 위한 알베도 맵을 추출할 수 있습니다.'
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > Scan Processing > Multi-Angle to Albedo
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 다중 각도-알베도
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '238'
ht-degree: 2%

---


# 다중 각도-알베도

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](multi-angle-to-albedo.resources/multi-angle-to-albedo.png){width="128px"}

<b>내부:</b> 재질 필터 > 스캔 처리

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 설명

이 노드는 다른 조명 각도 아래에서 촬영된 입력 사진/스캔 세트에서 모든 조명 정보를 제거하려고 시도합니다. 모든 샘플을 조명 중립적이어야 하는 하나의 단일 이미지로 결합하므로 가능한 한 PBR 교정이 가능합니다.

샘플 수가 많을수록 그리고 조명 각도의 차이가 클수록 더 큰 성공을 거둘 수 있다는 점을 명심하십시오. 4개의 샘플 이후에는 입력 이미지에 따라 거의 완벽한 결과를 얻을 수 있습니다. 입력 이미지는 삼각대로 촬영해야 하며 다른 각도에서 조명을 제외하고 약간의 차이가 있거나 이상적으로는 차이가 없어야 합니다!

>[!NOTE]
>
> 이 노드의 Normalmap 버전에 대해서는 [Multi-Angle to Normal](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/multi-angle-to-normal/multi-angle-to-normal.md)을 참조하십시오. 입력을 사전 처리하려면 [다중 Color Equalizer](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/multi-color-equalizer/multi-color-equalizer.md), [다중 자르기](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/multi-crop/multi-crop.md) 및 [다중 복제 패치](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/multi-clone-patch/multi-clone-patch.md)를 이러한 노드와 결합해야 하므로 유용할 수 있습니다.
> 
> [블로그 게시물 &quot;스마트폰은 재료 스캐너입니다&quot;는 이 프로세스를 좀 더 잘 보여줍니다.](https://www.allegorithmic.com/blog/your-smartphone-material-scanner)

</td>
</tr>
</table>

<a name="inputs"></a>

## 입력

|  |  |
|:---|:---|
| <b>입력 1-8</b> <i>색상 입력</i> | 입력 수는 Samples Amount 매개 변수에 따라 결정됩니다. |

<a name="parameters"></a>

## 매개변수

|  |  |
|:---|:---|
| <b>샘플 양</b> <i>2 - 8</i> | 처리에 사용할 샘플(입력) 수를 설정합니다. |
