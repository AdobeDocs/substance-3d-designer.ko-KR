---
helpx_url: "https://helpx.adobe.com/kr/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/blending-material/material-blend.html"
breadcrumb-title: ''
description: 재질 혼합 노드를 사용하면 복합 재질 효과를 만드는 데 사용할 마스크를 사용하여 전체 재질을 혼합할 수 있습니다.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > Blending (Material) > Material Blend
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 재질 혼합
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '458'
ht-degree: 6%

---


# 재질 혼합

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](material-blend.resources/material-blend.png){width="128px"}

<b>내부:</b> 재질 필터 > 혼합

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 설명

재질 혼합은 [원자 혼합 노드](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/blend/blend.md)에 해당하는 다중 채널의 전체 재질 혼합입니다. 회색 음영 마스크를 기반으로 하거나 선택적으로 색상 ID 마스크의 단일 색상을 기반으로 두 가지 전체 재질(가능한 모든 채널)을 혼합합니다.

이 노드는 두 재질을 혼합하고 회색 음영 맵을 만들지만 전체 색상 ID는 베이킹하지 않으려는 경우에 유용합니다. 색상 ID 베이크가 있고 두 개 이상의 재질을 혼합하려는 경우 [다중 재질 혼합](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/blending-material/multi-material-blend/multi-material-blend.md)을 사용하는 것이 좋습니다.

</td>
</tr>
</table>

<a name="inputs"></a>

## 입력

|  |  |
|:---|:---|
| <b>ColorID</b> <i>색상 입력</i> | 선택적 베이킹 색상 ID 맵입니다. |
| <b>회색조 마스크</b> <i>회색 음영 입력</i> | 노드의 효과를 마스킹하는 데 사용되는 마스크 슬롯입니다. |

<a name="parameters"></a>

## 매개변수

|  |  |
|:---|:---|
| <b>채널</b> | 예를 들어 [금속/거칠음] 대신 [Specular/광택] 맵을 사용하는 경우 이 그룹에서 재질 채널을 켜거나 끌 수 있습니다. |
| <b>확산</b> |  |
| <b>불투명도</b> <i>0.0 - 1.0</i> | 전경과 배경 간 불투명도 혼합 |
| <b>혼합 모드</b> <i>표준, 추가, 빼기, 곱하기, 추가/하위, 최대, 최소, 스위치</i> |  |
| <b>기본 색상</b> |  |
| <b>불투명도</b> <i>0.0 - 1.0</i> | 전경과 배경 간 불투명도 혼합 |
| <b>혼합 모드</b> <i>표준, 추가, 빼기, 곱하기, 추가/하위, 최대, 최소, 스위치</i> |  |
| <b>표준</b> |  |
| <b>불투명도</b> <i>0.0 - 1.0</i> | 전경과 배경 간 불투명도 혼합 |
| <b>Specular</b> |  |
| <b>불투명도</b> <i>0.0 - 1.0</i> | 전경과 배경 간 불투명도 혼합 |
| <b>혼합 모드</b> <i>표준, 추가, 빼기, 곱하기, 추가/하위, 최대, 최소, 스위치</i> |  |
| <b>발광</b> |  |
| <b>불투명도</b> <i>0.0 - 1.0</i> | 전경과 배경 간 불투명도 혼합 |
| <b>혼합 모드</b> <i>표준, 추가, 빼기, 곱하기, 추가/하위, 최대, 최소, 스위치</i> |  |
| <b>광택</b> |  |
| <b>불투명도</b> <i>0.0 - 1.0</i> | 전경과 배경 간 불투명도 혼합 |
| <b>혼합 모드</b> <i>표준, 추가, 빼기, 곱하기, 추가/하위, 최대, 최소, 스위치</i> |  |
| <b>거칠음</b> |  |
| <b>불투명도</b> <i>0.0 - 1.0</i> | 전경과 배경 간 불투명도 혼합 |
| <b>혼합 모드</b> <i>표준, 추가, 빼기, 곱하기, 추가/하위, 최대, 최소, 스위치</i> |  |
| <b>금속</b> |  |
| <b>불투명도</b> <i>0.0 - 1.0</i> | 전경과 배경 간 불투명도 혼합 |
| <b>혼합 모드</b> <i>표준, 추가, 빼기, 곱하기, 추가/하위, 최대, 최소, 스위치</i> |  |
| <b>Specular level</b> |  |
| <b>불투명도</b> <i>0.0 - 1.0</i> | 전경과 배경 간 불투명도 혼합 |
| <b>혼합 모드</b> <i>표준, 추가, 빼기, 곱하기, 추가/하위, 최대, 최소, 스위치</i> |  |
| <b>주변 오클루전</b> |  |
| <b>불투명도</b> <i>0.0 - 1.0</i> | 전경과 배경 간 불투명도 혼합 |
| <b>혼합 모드</b> <i>표준, 추가, 빼기, 곱하기, 추가/하위, 최대, 최소, 스위치</i> |  |
| <b>Height</b> |  |
| <b>불투명도</b> <i>0.0 - 1.0</i> | 전경과 배경 간 불투명도 혼합 |
| <b>혼합 모드</b> <i>표준, 추가, 빼기, 곱하기, 추가/하위, 최대, 최소, 스위치</i> |  |
| <b>불투명도</b> |  |
| <b>불투명도</b> <i>0.0 - 1.0</i> | 전경과 배경 간 불투명도 혼합 |
| <b>혼합 모드</b> <i>표준, 추가, 빼기, 곱하기, 추가/하위, 최대, 최소, 스위치</i> |  |
| <b>색상 ID 마스크</b> <i>거짓/참</i> | 회색 음영 마스크 대신 색상 ID 마스크를 사용합니다. 이 색상은 한 가지 색상에만 적용된다는 점을 기억하십시오! |
| <b>색상</b> <i>(색상 값)</i> | 선택하여 흰색으로 변환할 색상입니다. |
| <b>허용량</b> <i>0.01 - 1.0</i> | 선택한 색상이 인접 색상으로 혼합되는 정도입니다. |
| <b>패딩</b> <i>0.0 - 1.0</i> | 선택한 색상의 전환 대비입니다. |
