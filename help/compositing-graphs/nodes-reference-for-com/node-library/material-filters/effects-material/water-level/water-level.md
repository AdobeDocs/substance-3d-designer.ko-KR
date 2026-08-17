---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/effects-material/water-level.html"
breadcrumb-title: ''
description: '[수위] 노드를 사용하면 수위 Height을 기반으로 재질을 블렌딩하여 사실적인 수위 효과를 만들 수 있습니다.'
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > Effects (Material) > Water Level
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 수위
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '284'
ht-degree: 1%

---


# 수위

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/water-level.png){width="128px"}

## 수위

**내부:** *재질 필터/효과*

**복합**

</td>
<td style="border: 0;" valign="top">

## 설명

전체 재질 입력에 수위를 추가하는 올인원 효과입니다. 효과가 작동하려면 입력 재질에 양질의 Heightmap이 있어야 합니다. 결과는 PBR이 올바릅니다.

## 매개변수

### 입력

* **마스크**: *회색 음영 입력*\
  노드의 효과를 마스킹하는 데 사용되는 마스크 슬롯입니다.

### 매개변수

* **채널**\
  예를 들어 [금속]/[거칠음] 대신 [Specular/광택] 맵을 사용하는 경우 이 그룹에서 재질 채널을 켜거나 끌 수 있습니다.
* **수위**: *0.0 - 1.0*&#x200B;수위를 높이거나 낮추는 기본 컨트롤.
* **물의 어두움**: *0.0 - 1.0*&#x200B;물의 일반적인 &quot;투명도&quot;를 설정합니다.
* **가장자리 젖음**: *0.0 - 1.0*&#x200B;물 가장자리의 젖은 정도를 결정합니다.
* **가장자리 젖음 거리**: *0.0 - 1.0*&#x200B;젖은 가장자리가 닿는 거리를 설정합니다.
* **깊이 흐림 양**: *0.0 - 1.0*&#x200B;물 아래의 깊이에 따라 흐림 양을 설정합니다. 흐림 효과 반경을 수정합니다.
* **깊이 흐림 효과 불투명도**: *0.0 - 1.0*&#x200B;깊이 흐림 효과의 혼합 정도를 결정합니다.
* **슬러지 색상**: *(색상 값)*슬러지 효과의 색상을 설정합니다.
* **슬러지 깊이**: *0.0 - 1.0*&#x200B;슬러지가 나타나는 깊이를 수위에 따라 설정합니다.
* **슬러지 불투명도**: *0.0 - 1.0*&#x200B;슬러지 효과의 전체 불투명도를 설정합니다.
* **서리**: *0.0 - 1.0*&#x200B;서리의 양을 설정합니다. 바깥쪽 가장자리에서 시작하여 안쪽으로 이동합니다.
* **서리 강도**: *0.0 - 1.0*&#x200B;서리 강도를 설정하고 효과의 &quot;불투명도&quot;를 제어합니다.
* **동결 균열**: *0.0 - 1.0*&#x200B;동결에서 액체로 전환되는 균열의 양을 설정합니다.
* **Frost Normal 형식**: *DirectX/OpenGL* Frost Normalmap 효과 녹색 채널을 전환합니다.

## 예제 이미지

|  |
| --- |
| 이 페이지에 첨부된 이미지가 없습니다. |

</td>
</tr>
</table>
