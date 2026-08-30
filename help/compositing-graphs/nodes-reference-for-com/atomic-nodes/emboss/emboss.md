---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/atomic-nodes/emboss.html"
breadcrumb-title: ''
description: '[엠보스] 노드를 사용하면 표면 세부 사항에 깊이 및 부조를 추가하기 위해 텍스처에 엠보스 효과를 만들 수 있습니다.'
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Atomic nodes > Emboss
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 엠보스
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '261'
ht-degree: 9%

---


# 엠보스

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![원자 노드: 엠보스](emboss.resources/comp_emboss_1.png "원자 노드: 엠보스"){width="200px"}

</td>
<td width="100.00%" style="border: 0;" valign="top">

지정된 광원의 방향에 따라 이미지에 있는 모양의 측면을 비춰 엠보싱 효과를 적용합니다.

즉, 노드는 2 개의 입력들에 기초하여, Height 및 깊이 변화들을 갖는 표면에 떨어지는 광을 시뮬레이션하는 간단한 2D 음영을 수행한다.

</td>
</tr>
</table>

이 노드는 PBR 유사 프로젝트에 자주 사용되지 않지만 텍스처에 단순하고 구워진 조명을 원하는 특정 경우에 사용할 수 있습니다. 또는 [광택이 있는 엠보스](../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/emboss-with-gloss/emboss-with-gloss.md) 및 [Uber 엠보스](../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/uber-emboss/uber-emboss.md)는 유사하지만 더 광범위한 기능을 제공합니다.

<table>
<tr style="border: 0;">
<td width="100.00%" style="border: 0;" valign="top">



</td>
<td width="83.33%" style="border: 0;" valign="top">



</td>
<td width="100.00%" style="border: 0;" valign="top">



</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

## 출력 커넥터

</td>
<td style="border: 0;" valign="top">

### 예

</td>
</tr>
</table>

## 매개변수

|  |  |
| --- | --- |
| <b>강도</b> *부동* | 조명 효과의 전체 강도를 조정합니다.   &quot;Height&quot; 맵의 강도 및 조명 효과의 강도를 설정합니다 |
| <b>조명 각도</b> *부동* | 조명이 시뮬레이션되는 각도를 설정합니다.   엠보싱 이미지의 밝은 영역의 조명 각도를 정의합니다 |
| <b>강조 색상</b> *Float/Float4* | 조명 각도를 향하는 영역의 색상을 설정합니다.   입력 이미지가 색상인 경우 강조 표시의 색상을 설정합니다. |
| <b>그림자 색상</b> *Float/Float4* | 밝은 각도에서 반대 방향으로 향하는 영역의 색상을 설정합니다.   엠보싱 이미지의 어두운 영역 색상을 설정합니다. |

## 입력 커넥터

|  |  |
| --- | --- |
| <b>입력</b> 기본 *회색 음영/색상* | 음영처리되지 않은 기본 색상을 제공합니다. 일종의 확산 또는 기본 색상 텍스처로 볼 수 있습니다. |
| <b>강도 입력</b> *회색 음영* | 표면의 조명을 계산하는 데 사용되는 높이 맵을 나타냅니다. 검정은 낮고 흰색은 높음 |

## 출력 커넥터

|  |  |
| --- | --- |
| <b>출력</b> *회색 음영/색상* |  |

## 예

*곧 출시 예정*
