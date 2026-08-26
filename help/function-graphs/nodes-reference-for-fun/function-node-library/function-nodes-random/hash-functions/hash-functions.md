---
helpx_url: "https://helpx.adobe.com/kr/substance-3d-designer/function-graphs/nodes-reference-for-function-graphs/function-node-library/function-nodes-random/hash-functions.html"
breadcrumb-title: ''
description: 함수 그래프에 해시 함수를 사용하여 입력 좌표에 따라 결정론적 난수 값을 생성한다.
helpx_creative_field: ""
helpx_description: Designer > Function graphs > Nodes reference for function graphs > Function node library > Random > Hash
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 해시 함수
user-guide-description: ''
user-guide-title: ''
source-git-commit: 5b9c9d12e2ccd76f75ec2a74815f9c68c43c06a2
workflow-type: tm+mt
source-wordcount: '154'
ht-degree: 1%

---


# 해시 함수

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![해시 노드: 아이콘](../../../../../assets/hash-icon.png "해시 노드: 아이콘"){width="200px"}

<b>내부:</b> 함수 > 임의

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 설명

시드로 사용된 입력 값을 기준으로 0에서 1 사이의 의사(pseudo) 난수 값을 계산합니다.

제목의 숫자는 값 입력 및 값 출력 유형을 표시합니다. 예를 들어, 해시(23)는 float2 값을 입력으로서 취하고 float3 값을 출력한다.

</td>
</tr>
</table>

해시 노드가 여러 구성 요소의 값을 출력하는 경우, 각 구성 요소는 서로 다른 의사-랜덤 값을 갖는다.

입력 유형 및 출력 유형이 있는 사용 가능한 버전:

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

<b>해시 11:</b> 부동 → 부동

<b>해시 14:</b> Float → Float4

<b>해시 21:</b> Float2 → Float

<b>해시 22:</b> Float2 → Float2

</td>
<td style="border: 0;" valign="top">

<b>해시 24:</b> Float2 → Float4

<b>Hash31:</b> Float3 → Float

<b>해시 32:</b> Float3 → Float2

</td>
</tr>
</table>

## 입력 커넥터

|  |  |
| --- | --- |
| <b>입력</b> | 의사(pseudo) 임의 출력을 계산하는 시드로 사용되는 값입니다. |

## 예

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![해시 14 예](../../../../../assets/hash14-example.png "해시 14 예"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![해시 32 예](../../../../../assets/hash32-example.png "해시 32 예"){zoomable="yes"}

</td>
</tr>
</table>
