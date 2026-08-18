---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/transforms-material/material-transform.html"
breadcrumb-title: ''
description: '[재질 변형] 노드를 사용하여 회전, 비율 및 오프셋을 비롯한 재질 출력에 변형을 적용합니다.'
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > Transforms (Material) > Material Transform
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 재질 변형
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '170'
ht-degree: 1%

---


# 재질 변형

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/material-transforms.png){width="128px"}

## 재질 변형

**내부:** *재질 필터/변형*

**단순**

</td>
<td style="border: 0;" valign="top">

## 설명

재질 변형은 간단히 [원자 변형 2D 노드](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/transformation-2d/transformation-2d.md)의 &quot;다중 채널&quot; 재질 버전입니다. 변형 2D와 동일한 인터페이스를 사용하여 입력 재질의 모든 채널을 동시에 변형합니다.

채널을 제대로 설정하기만 하면 됩니다! 기본적으로 [금속/거칠음] 및 [Specular/광택] 설정이 모두 활성화되어 있어서 약간의 혼동이 발생할 수 있습니다.

## 매개변수

* **변환**: *(변환 행렬)*\
  결과를 회전하고 크기를 조절합니다. 이동/패닝은 오프셋 매개 변수를 통해 수행됩니다
* **오프셋**: *-0.5 - 0.5*\
  결과를 이동하거나 변환합니다. 변형 컨트롤이 있으면 캔버스와 직접 상호 작용하여 결과를 수정할 수 있습니다.
* **표준 형식**\
  DirectX 및 OpenGL 형식(녹색으로 뒤집기) 중에서 선택합니다.
* **채널**\
  예를 들어 [금속]/[거칠음] 대신 [Specular/광택] 맵을 사용하는 경우 이 그룹에서 재질 채널을 켜거나 끌 수 있습니다.

## 예제 이미지

|  |
| --- |
| 이 페이지에 첨부된 이미지가 없습니다. |

</td>
</tr>
</table>
