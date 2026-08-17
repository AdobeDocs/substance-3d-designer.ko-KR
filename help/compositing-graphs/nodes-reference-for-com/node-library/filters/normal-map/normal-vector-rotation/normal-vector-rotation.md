---
helpx_url: "https://helpx.adobe.com/kr/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/normal-map/normal-vector-rotation.html"
breadcrumb-title: ''
description: '[표준 벡터 회전] 노드를 사용하여 표면 조명 및 세부 방향 조정을 위한 표준 맵 벡터를 회전합니다.'
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Normal Map > Normal Vector Rotation
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 표준 벡터 회전
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '123'
ht-degree: 4%

---


# 표준 벡터 회전

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/normal-vector-rotation.png){width="128px"}

## 표준 벡터 회전

**내부:** *필터/표준 맵*

**단순**

</td>
<td style="border: 0;" valign="top">

## 설명

탄젠트 공간에서 입력 Normalmap의 모든 벡터를 회전하는 표준 유틸리티 노드입니다. 픽셀이 실제로 변형되는 것은 아니며 픽셀이 나타내는 값을 수정합니다. 선택적 맵을 사용하여 회색 음영 측면에 무작위 회전을 추가할 수 있습니다.

## 입력

* **표준**: *색상 입력*\
  회전을 수행할 기본 맵 필수 여부.
* **회전 맵(선택 사항)**: *회색 음영 입력*\
  회전 강도를 변조하는 회색 음영 맵입니다.

## 매개변수

* **회전 각도**: *0.0 - 1.0*\
  표준 맵을 회전하는 각도를 설정합니다.
* **표준 형식**: *DirectX, OpenGL*\
  다른 표준 맵 포맷 간 전환(녹색 채널을 반전함)

## 예

</td>
</tr>
</table>
