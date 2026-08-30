---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/scan-processing/material-clone-patch.html"
breadcrumb-title: ''
description: '[재질 복제 패치] 노드를 사용하여 스캔한 재질의 가공물을 복구하기 위해 텍스처 영역을 복제하고 패치합니다.'
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > Scan Processing > Material Clone Patch
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 재질 복제 패치
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '326'
ht-degree: 4%

---


# 재질 복제 패치

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](material-clone-patch.resources/clone-patch-material.png){width="128px"}

<b>내부:</b> 재질 필터 > 스캔 처리

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 설명

[복제 패치](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/clone-patch/clone-patch.md)의 다중 채널, 전체 재질 버전입니다. 재질의 모든 채널에 대해 복제 패치를 수행합니다. [자세한 내용은 원래 버전을 참조하세요!](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/clone-patch/clone-patch.md)

재질의 모든 채널에서 세부 묘사를 제거하려는 경우 매우 유용합니다. 여러 채널에 대한 디버그 이미지를 출력하여 스마트 패치 영역의 모양을 정확하게 확인합니다.

</td>
</tr>
</table>

<a name="inputs"></a>

## 입력

|  |  |
|:---|:---|
| <b>마스크</b> <i>회색 음영 입력</i> | 노드의 효과를 마스킹하는 데 사용되는 마스크 슬롯입니다. &quot;마스크&quot; 매개 변수로 전환할 수 있습니다. |

<a name="parameters"></a>

## 매개변수

|  |  |
|:---|:---|
| <b>채널</b> | 예를 들어 [금속]/[거칠음] 대신 [Specular/광택] 맵을 사용하는 경우 이 그룹에서 재질 채널을 켜거나 끌 수 있습니다. |
| <b>모양</b> <i>정사각형, 디스크</i> | 스탬프 모양을 설정합니다. 기본으로만 사용됩니다. |
| <b>가장자리</b> |  |
| <b>임계값(여러 채널용)</b> <i>0.0 - 1.0</i> | 혼합 영역이 도달할 거리를 설정합니다. 이는 대상 영역의 모양을 따라 단계별로 성장하므로 균일한 배경을 사용하는 효과는 거의 없습니다. 채널 간에 너무 많이 변경하면 시각적 차이가 발생할 수 있으므로 주의해야 합니다. |
| <b>흐림 효과</b> <i>0.0 - 2.0</i> | 더 부드러운 전환이 필요한 경우 스탬프 영역의 가장자리를 흐리게 합니다. |
| <b>Smoothness</b> <i>0.0 - 2.0</i> | 도장 모양의 가장자리를 반올림하여 외곽선이 더 부드럽게 흐르도록 합니다. |
| <b>격자 해상도</b> <i>1 - 11</i> | 혼합 분석의 품질 해상도를 설정합니다. 값이 높을수록 더 정확한 혼합을 의미합니다. |
| <b>변환</b> |  |
| <b>원본 행렬</b> <i>(변환 행렬)</i> | 소스(크기 및 회전) 캔버스에서는 수행할 수 없으며 이러한 매개 변수만 변경하십시오. |
| <b>원본 오프셋</b> <i>-0.5 - 0.5</i> | 소스 위치를 변환합니다. 캔버스에서는 수행할 수 없으며 이러한 매개 변수만 변경하십시오. *이 매개 변수는 아마도 변경할 기본 매개 변수입니다!* |
| <b>대상 행렬</b> <i>(변환 행렬)</i> | 대상 위치(크기 및 회전) 캔버스에서 gizmo를 통해 수행할 수도 있습니다. |
| <b>대상 오프셋</b> <i>-0.5 - 0.5</i> | 대상 위치를 변환합니다. 캔버스에서 gizmo를 통해 수행할 수도 있습니다. |
