---
helpx_url: "https://helpx.adobe.com/kr/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/transforms-material/material-transform.html"
breadcrumb-title: ''
description: 회전, 비율 조정, 오프셋 등의 재질 출력에 변환을 적용하려면 [자료] 노드를 사용합니다.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > Transforms (Material) > Material Transform
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 재질 변형
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '157'
ht-degree: 2%

---


# 재질 변형

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](material-transform.resources/material-transforms.png){width="128px"}

<b>재질 필터:</b> 변환 >

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 설명

재질 2D 변환 버전은 간단히 [원자 채널](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/transformation-2d/transformation-2d.md)입니다. 입력 자료가 같은 시간, 변환 2D와 같은 모든 채널에서의 변환.

채널을 제대로 설정하기만 하면 됩니다! 기본적으로 [금속/거칠음] 및 [Specular/광택도] 모두 활성화되어 있어서 약간의 혼동이 발생할 수 있습니다.

</td>
</tr>
</table>

<a name="parameters"></a>

## 매개변수

|  |  |
|:---|:---|
| <b>변환</b> <i>(변환 행렬)</i> | 결과를 회전하고 크기를 조절합니다. 이동/패닝은 오프셋 매개 변수를 통해 수행됩니다 |
| <b>오프셋</b> <i>-0.5 - 0.5</i> | 결과를 이동하거나 변환합니다. 변형 컨트롤이 있으면 캔버스와 직접 상호 작용하여 결과를 수정할 수 있습니다. |
| <b>표준 형식</b> | DirectX 및 OpenGL 형식(녹색으로 뒤집기) 중에서 선택합니다. |
| <b>채널</b> | 예를 들어 [금속]/[거칠음] 대신 [Specular/광택] 맵을 사용하는 경우 이 그룹에서 재질 채널을 켜거나 끌 수 있습니다. |
