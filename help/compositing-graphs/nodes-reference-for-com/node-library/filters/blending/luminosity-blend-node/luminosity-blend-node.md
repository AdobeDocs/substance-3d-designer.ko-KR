---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/blending/luminosity-blend-node.html"
breadcrumb-title: ''
description: '[광도] 혼합 노드를 사용하면 명도 기반의 합성 효과를 만들기 위해 광도 값을 기준으로 텍스처를 혼합할 수 있습니다.'
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Blending > Luminosity (Blend Node)
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 광도(혼합 노드)
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6507710c6005db383ba88ce9e5c6ad9c34d87c9f
workflow-type: tm+mt
source-wordcount: '102'
ht-degree: 4%

---


# 광도(혼합 노드)

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

<b>내부:</b> 필터 > 혼합

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 설명

전경의 광도를 적용하면서 배경의 색조와 색차를 유지하는 [광도] 혼합 모드를 수행합니다.

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
