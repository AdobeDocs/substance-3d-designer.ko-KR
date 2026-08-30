---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/blending/color-dodge.html"
breadcrumb-title: ''
description: '[색상 닷지 혼합] 노드를 사용하면 대비를 줄여 밝은 영역과 광선 효과를 만들어 텍스처를 밝게 할 수 있습니다.'
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Blending > Color Dodge
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 색상 닷지
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '91'
ht-degree: 9%

---


# 색상 닷지

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](color-dodge.resources/color-dodge.png){width="128px"}

<b>내부:</b> 필터 > 혼합

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 설명

색상 닷지 혼합을 수행합니다. 수학적으로 공식은 Background / (1-Foreground)입니다.

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
