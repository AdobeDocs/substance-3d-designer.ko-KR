---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/blending/dissolve.html"
breadcrumb-title: ''
description: 텍스처 간 전환 및 페이드 효과를 만들기 위해 디졸브 모드를 사용하여 텍스처를 혼합하려면 디졸브 노드를 사용합니다.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Blending > Dissolve
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 디졸브
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '89'
ht-degree: 7%

---


# 디졸브

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](dissolve.resources/dissolve-2.png){width="128px"}

<b>내부:</b> 필터 > 혼합

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 설명

두 입력을 흰색 노이즈와 함께 혼합하여 전환을 위한 마스크로 사용합니다.

</td>
</tr>
</table>

<a name="inputs"></a>

## 입력

|  |  |
|:---|:---|
| <b>전경</b> <i>색상 입력</i> |  |
| <b>배경</b> <i>색상 입력</i> |  |
| <b>마스크</b> <i>회색 음영 입력</i> | 노드의 효과를 마스킹하는 데 사용되는 마스크 슬롯입니다. |

<a name="parameters"></a>

## 매개변수

|  |  |
|:---|:---|
| <b>불투명도</b> <i>0.0 - 1.0</i> | 전경과 배경 간 불투명도 혼합. |
| <b>알파 혼합</b> <i>거짓/참</i> | 전경 및 배경 알파 채널의 혼합을 전환합니다. False로 설정하면 전경의 알파 채널이 무시됩니다. |
