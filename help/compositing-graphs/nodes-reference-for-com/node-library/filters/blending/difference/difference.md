---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/blending/difference.html"
breadcrumb-title: ''
description: 차이 혼합 노드를 사용하면 반전 및 대비 효과를 만드는 차이 모드를 사용하여 텍스처를 혼합할 수 있습니다.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Blending > Difference
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 차이
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '99'
ht-degree: 7%

---


# 차이

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](difference.resources/difference.png){width="128px"}

<b>내부:</b> 필터 > 혼합

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 설명

전경 및 배경 입력 간 차이 혼합 모드를 수행합니다. 전경에서 배경을 빼서 절대 결과(음수 값이 아님)를 반환합니다.

</td>
</tr>
</table>

<a name="inputs"></a>

## 입력

|  |  |
|:---|:---|
| <b>배경</b> <i>색상 입력</i> |  |
| <b>전경</b> <i>색상 입력</i> |  |
| <b>마스크</b> <i>회색 음영 입력</i> | 노드의 효과를 마스킹하는 데 사용되는 마스크 슬롯입니다. |

<a name="parameters"></a>

## 매개변수

|  |  |
|:---|:---|
| <b>불투명도</b> <i>0.0 - 1.0</i> | 전경과 배경 간 불투명도 혼합. |
| <b>알파 혼합</b> <i>거짓/참</i> | 전경 및 배경 알파 채널의 혼합을 전환합니다. False로 설정하면 전경의 알파 채널이 무시됩니다. |
