---
helpx_url: "https://helpx.adobe.com/kr/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/atomic-nodes/directional-blur.html"
breadcrumb-title: ''
description: 동작 흐림 효과 및 줄무늬 효과를 만들기 위해 방향 흐림 효과 노드를 사용하여 특정 방향으로 흐림 효과를 적용합니다.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Atomic nodes > Directional blur
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 방향성 흐림 효과
user-guide-description: ''
user-guide-title: ''
source-git-commit: ea96f5a148246d20263c4ecf0b67d0b4a51f28a8
workflow-type: tm+mt
source-wordcount: '205'
ht-degree: 9%

---


# 방향성 흐림 효과

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![원자 노드: 방향 흐림 효과](../../../../assets/comp_dirmotionblur_1.png "원자 노드: 방향 흐림 효과"){width="200px"}

</td>
<td width="100.00%" style="border: 0;" valign="top">

강도 맵에 따라 지정된 방향으로 흐림 효과를 적용합니다.

이 노드는 입력에 대한 동작 흐림 효과와 유사한 동작을 수행한다. 모든 방향으로 동일하게 흐려지는 일반 &#39;[흐림](../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/blur/blur.md)&#39; 노드와 달리, &#39;방향 흐림&#39;은 사용자 정의 각도를 따라 작동합니다.

</td>
</tr>
</table>

흐림 효과와 유사하게 더 빠르고 낮은 품질의 작업이기도 합니다. 확장된 고품질 대안이 [비등방성 흐림 효과](../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/blurs/anisotropic-blur/anisotropic-blur.md)에서 제공되며, 성능 절충이 가능합니다

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

## 방향 및 비등방성 흐림 효과

아래 이미지는 유사한 매개 변수를 사용하여 동일한 입력 모양에서 방향 흐림 효과와 [비등방성 흐림 효과](../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/blurs/anisotropic-blur/anisotropic-blur.md)를 보여줍니다. [비등방성 흐림 효과]는 전체 비등방성 및 고품질로 설정되었습니다.

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

<b>방향 흐림</b>

![방향 흐림 효과 비교](../../../../assets/dirblur-01.png "방향 흐림 효과 비교"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

<b>비등방성 흐림 효과</b>

![비등방성 흐림 효과 비교](../../../../assets/aniso-01.png "비등방성 흐림 효과 비교"){zoomable="yes"}

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

### 매개변수

</td>
<td style="border: 0;" valign="top">

### 입력 커넥터

</td>
<td style="border: 0;" valign="top">

### 출력 커넥터

</td>
<td style="border: 0;" valign="top">

### 예

</td>
</tr>
</table>

## 매개변수

|  |  |
| --- | --- |
| <b>강도</b> *부동* | 흐림 반경(픽셀 단위)을 설정합니다. |
| <b>각도</b> *부동* | 회전 수에 따른 흐림 효과의 방향은 시계 방향으로, 수평(예: 방향 벡터 (1, 0))부터 시작됩니다. |

## 입력 커넥터

|  |  |
| --- | --- |
| <b>입력</b> *회색 음영/색상* [기본](../../../../glossary/glossary.md) | 처리할 이미지. |

## 출력 커넥터

|  |  |
| --- | --- |
| <b>출력</b> *회색 음영/색상* |  |

## 예

*곧 출시 예정*
