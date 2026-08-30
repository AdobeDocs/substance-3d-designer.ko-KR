---
helpx_url: "https://helpx.adobe.com/kr/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/atomic-nodes/normal.html"
breadcrumb-title: ''
description: '[표준] 노드를 사용하면 표면 세부 사항 및 조명을 제어하기 위한 표준 맵 텍스처를 처리하고 조작할 수 있습니다.'
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Atomic nodes > Normal
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 법선
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '222'
ht-degree: 8%

---


# 법선

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Atomic node: Normal](normal.resources/comp_normal_1.png "Atomic node: Normal"){width="200px"}

</td>
<td width="100.00%" style="border: 0;" valign="top">

높이 맵으로 해석되는 회색 음영 이미지에서 일반 맵을 계산합니다.

노드는 입력 회색 음영 맵을 접선-공간 표준 맵 출력으로 변환합니다. 강도와 인코딩을 설정할 수 있는 몇 가지 사용자 옵션이 있습니다.

</td>
</tr>
</table>

이 노드는 실시간으로 사용할 수 있도록 Height 맵 입력을 일반 맵으로 변환하는 데 자주 사용되는 매우 유용한 노드입니다. [일반 소벨](../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/normal-map/normal-sobel/normal-sobel.md) 및 일반 세계 단위로의 Height에서 찾을 수 있는 대안이 있습니다.

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
| <b>강도</b> *부동* | Height 맵의 강도를 수정합니다.   정규화로 변환하기 위해 입력 Height 맵을 해석하는 강도를 설정합니다. 입력 맵에 따라 100보다 큰 값은 더 큰 효과가 없습니다. |
| <b>일반 형식</b> *부울* | Height 맵의 Y 좌표를 반전합니다(OpenGL).   녹색(Y) 채널의 인코딩 방법을 설정합니다. 기본적으로 &quot;Flip Green/Y&quot; 스위치입니다. |
| <b>Alpha 채널 콘텐츠</b> *부울* | 표준 맵의 알파 채널을 입력 텍스처로 채웁니다.   [입력/강제] Alpha을 1로 하여 Alpha 채우기: 이 옵션을 선택하면 [입력]을 추가 Alpha으로 사용하지 않고 Alpha 채널을 단색으로 설정할 수 있습니다. |

## 입력 커넥터

|  |  |
| --- | --- |
| <b>입력</b> *회색 음영* 기본 | Height 맵으로 해석되는 입력 이미지입니다. |

## 출력 커넥터

|  |  |
| --- | --- |
| <b>출력</b> *색상* |  |

## 예

*곧 출시 예정*
