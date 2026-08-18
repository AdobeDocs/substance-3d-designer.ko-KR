---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/normal-map/normal-transform.html"
breadcrumb-title: ''
description: 벡터 방향을 올바르게 유지하면서 표준 맵에 변형을 적용하려면 [표준 변형] 노드를 사용합니다.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Normal Map > Normal Transform
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 표준 변형
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '104'
ht-degree: 1%

---


# 표준 변형

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/normal-transform.png){width="128px"}

## 표준 변형

**내부:** *필터/표준 맵*

**단순**

</td>
<td style="border: 0;" valign="top">

## 설명

원자 변환 2D 노드와 마찬가지로, 탄젠트 공간을 파괴하지 않고 정규맵을 변환할 수 있지만 즉석에서 다시 계산되어 항상 정확한 정규맵을 생성합니다.

## 매개변수

* **Matrix2x2**: *(변환 행렬):*\
  입력을 회전하거나 크기를 조정합니다.
* **오프셋**: *-0.5 - 0.5*\
  결과를 이동하거나 변환합니다. 변형 컨트롤이 있으면 캔버스와 직접 상호 작용하여 결과를 수정할 수 있습니다.
* **표준 형식**: *DirectX, OpenGL*\
  다른 표준 맵 포맷 간 전환(녹색 채널을 반전함)

</td>
</tr>
</table>
