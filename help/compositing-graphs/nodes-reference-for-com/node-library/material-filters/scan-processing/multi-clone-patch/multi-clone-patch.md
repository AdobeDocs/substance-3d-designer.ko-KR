---
helpx_url: "https://helpx.adobe.com/kr/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/scan-processing/multi-clone-patch.html"
breadcrumb-title: ''
description: 다중 복제 패치 노드 를 사용하여 스캔한 재료 가공물을 복구하기 위해 여러 텍스처 채널을 복제하고 패치합니다.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > Scan Processing > Multi Clone Patch
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 다중 복제 패치
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '305'
ht-degree: 5%

---


# 다중 복제 패치

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](multi-clone-patch.resources/clone-patch-multi.png){width="128px"}

![](multi-clone-patch.resources/clone-patch-multi-grayscale.png){width="128px"}

<b>내부:</b> 재질 필터 > 스캔 처리

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 설명

이 노드는 [복제 패치](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/clone-patch/clone-patch.md)의 다중 입력 버전입니다. 최대 8개의 입력을 서로 연결하고 모든 입력에 대해 정확히 동일한 클론 패치 작업을 수행합니다. 주로 다각 사진에 사용하기 위한 것으로, 다각 사진은 [알베도에 대한 다각](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/multi-angle-to-albedo/multi-angle-to-albedo.md) 또는 [보통 사진에 대한 다각](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/multi-angle-to-normal/multi-angle-to-normal.md)과 결합됩니다.

>[!NOTE]
>
> 자세한 내용은 [복제 패치](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/clone-patch/clone-patch.md)를 참조하고 재질 버전에 대한 [재질 복제 패치](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/material-clone-patch/material-clone-patch.md)를 참조하십시오.

</td>
</tr>
</table>

<a name="parameters"></a>

## 매개변수

|  |  |
|:---|:---|
| <b>입력 수</b> <i>1 - 8</i> | 동일한 패치 작업을 수신할 입력 양을 설정합니다. |
| <b>일반(색상에만 해당)</b> <i>거짓/참</i> | 입력이 정규맵인지 여부와 혼합을 정규맵으로 처리할지 여부를 설정합니다. |
| <b>모양</b> <i>정사각형, 디스크</i> | 스탬프 모양을 설정합니다. 기본으로만 사용됩니다. |
| <b>가장자리</b> |  |
| <b>임계값</b> <i>0.0 - 1.0</i> | 혼합 영역이 도달할 거리를 설정합니다. 이는 대상 영역의 모양을 따라 단계별로 성장하며, 균일한 배경의 효과는 거의 없습니다. |
| <b>흐림 효과</b> <i>0.0 - 2.0</i> | 더 부드러운 전환이 필요한 경우 스탬프 영역의 가장자리를 흐리게 합니다. |
| <b>Smoothness</b> <i>0.0 - 2.0</i> | 도장 모양의 가장자리를 반올림하여 외곽선이 더 부드럽게 흐르도록 합니다. |
| <b>격자 해상도</b> <i>1 - 11</i> | 혼합 분석의 품질 해상도를 설정합니다. 값이 높을수록 더 정확한 혼합을 의미합니다. |
| <b>변환</b> |  |
| <b>원본 행렬</b> <i>(변환 행렬)</i> | 소스(크기 및 회전) 캔버스에서는 수행할 수 없으며 이러한 매개 변수만 변경하십시오. |
| <b>원본 오프셋</b> <i>-0.5 - 0.5</i> | 소스 위치를 변환합니다. 캔버스에서는 수행할 수 없으며 이러한 매개 변수만 변경하십시오. *이 매개 변수는 아마도 변경할 기본 매개 변수입니다!* |
| <b>대상 행렬</b> <i>(변환 행렬)</i> | 대상 위치(크기 및 회전) 캔버스에서 gizmo를 통해 수행할 수도 있습니다. |
| <b>대상 오프셋</b> <i>-0.5 - 0.5</i> | 대상 위치를 변환합니다. 캔버스에서 gizmo를 통해 수행할 수도 있습니다. |
