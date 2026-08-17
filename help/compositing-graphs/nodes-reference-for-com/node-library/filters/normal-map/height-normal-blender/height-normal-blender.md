---
helpx_url: "https://helpx.adobe.com/kr/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/normal-map/height-normal-blender.html"
breadcrumb-title: ''
description: Height 표준 블렌더 노드를 사용하여 표면 세부 정보를 결합하기 위해 Height과 표준 맵을 블렌딩합니다.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Normal Map > Height Normal Blender
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Height 표준 블렌더
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '140'
ht-degree: 2%

---


# Height 표준 블렌더

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/height-normal-blender.png){width="128px"}

## Height 표준 블렌더

**내부:** *필터/표준 맵*

**단순**

</td>
<td style="border: 0;" valign="top">

## 설명

회색 음영 Heightmap을 표준 맵에 혼합하는 단축키 노드입니다. Height 입력이 내부적으로 표준 맵으로 변환된 다음 표준 입력과 올바르게 혼합됩니다.

이렇게 하면 개별 노드를 사용하여 수동으로 세부 사항을 혼합하는 것보다 더 빠르게 혼합할 수 있지만, 특정 요구 사항에 대한 컨트롤 및 개선 사항이 일부 부족할 수 있습니다.

## 매개변수

### 입력

* **Height**: *회색 음영 입력*\
  혼합할 회색 음영 높이 맵
* **표준**: *색상 입력*\
  혼합할 기본 Normalmap.

### 매개변수

* **표준 강도**: *0.0 - 16.0* Height 입력의 표준 변환 강도.
* **표준 형식**: *DirectX, OpenGL*\
  서로 다른 표준 맵 포맷 사이를 전환합니다(녹색 채널을 반전합니다).

## 예제 이미지

|  |
| --- |
| 이 페이지에 첨부된 이미지가 없습니다. |

</td>
</tr>
</table>
