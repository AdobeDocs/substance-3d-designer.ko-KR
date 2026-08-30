---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/effects-material/height-blend.html"
breadcrumb-title: ''
description: Height 혼합 노드를 사용하여 사실적인 재질 전환을 만들기 위해 높이 맵을 기반으로 텍스처를 혼합합니다.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > Effects (Material) > Height Blend
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Height 블렌드
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '153'
ht-degree: 5%

---


# Height 블렌드

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](height-blend.resources/height-blend.png){width="128px"}

<b>내부:</b> 재질 필터 > 효과

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 설명

Height 정보를 기반으로 두 개의 Heightmap을 결합합니다. 혼합 하이트맵을 생성하지만 다른 곳에서 사용할 수 있는 흑백 마스크도 생성합니다.

이 기능은 결합할 두 개의 고품질 Heightmaps가 있지만 [재질 Height 혼합](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/effects-material/material-height-blend/material-height-blend.md)에 필요한 전체 재질이 아닐 경우 유용합니다.

</td>
</tr>
</table>

<a name="inputs"></a>

## 입력

|  |  |
|:---|:---|
| <b>Height 상위</b> <i>회색 음영 입력</i> |  |
| <b>Height 아래쪽</b> <i>회색 음영 입력</i> |  |
| <b>마스크(선택 사항)</b> <i>회색 음영 입력</i> | 노드의 효과를 마스킹하는 데 사용되는 마스크 슬롯입니다. |

<a name="parameters"></a>

## 매개변수

|  |  |
|:---|:---|
| <b>Height 오프셋</b> <i>0.0 - 1.0</i> | 블렌드 레벨이 Height 축을 따라 이동되도록 높이 맵을 오프셋합니다. 혼합에 대한 기본 컨트롤입니다. |
| <b>대비</b> <i>0.0 - 1.0</i> | 혼합의 대비를 조정하고 전환을 더 선명하게 합니다. |
| <b>모드</b> <i>균형 잡힌 Height, 하위 Height 우선 순위</i> |  |
| <b>불투명도</b> <i>0.0 - 1.0</i> | 전경 Height의 불투명도를 혼합하면 안쪽이나 바깥쪽으로 페이드됩니다. |
