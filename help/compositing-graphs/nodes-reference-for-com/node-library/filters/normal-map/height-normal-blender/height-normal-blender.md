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
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '126'
ht-degree: 3%

---


# Height 표준 블렌더

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](height-normal-blender.resources/height-normal-blender.png){width="128px"}

<b>내부:</b> 필터 > 노멀 맵

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 설명

회색 음영 Heightmap을 표준 맵에 혼합하는 단축키 노드입니다. Height 입력이 내부적으로 표준 맵으로 변환된 다음 표준 입력과 올바르게 혼합됩니다.

이렇게 하면 개별 노드를 사용하여 수동으로 세부 사항을 혼합하는 것보다 더 빠르게 혼합할 수 있지만, 특정 요구 사항에 대한 컨트롤 및 개선 사항이 일부 부족할 수 있습니다.

</td>
</tr>
</table>

<a name="inputs"></a>

## 입력

|  |  |
|:---|:---|
| <b>Height</b> <i>회색 음영 입력</i> | 혼합할 회색 음영 높이 맵 |
| <b>표준</b> <i>색상 입력</i> | 혼합할 기본 Normalmap. |

<a name="parameters"></a>

## 매개변수

|  |  |
|:---|:---|
| <b>표준 강도</b> <i>0.0 - 16.0</i> | Height 입력의 일반 변환 강도입니다. |
| <b>표준 형식</b> <i>DirectX, OpenGL</i> | 서로 다른 표준 맵 포맷 사이를 전환합니다(녹색 채널을 반전합니다). |
