---
helpx_url: "https://helpx.adobe.com/kr/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/blending/switch.html"
breadcrumb-title: ''
description: 조건부 텍스처 선택을 위해 마스크를 기준으로 두 입력 텍스처 간을 전환하려면 [전환] 노드를 사용합니다.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Blending > Switch
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 전환
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '134'
ht-degree: 3%

---


# 전환

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](switch.resources/switch-1.png){width="128px"}

![](switch.resources/switch-grayscale.png){width="128px"}

<b>내부:</b> 필터 > 혼합

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 설명

간단한 2위치 스위치 노드 Switch 매개 변수 설정에 따라 Input 1 또는 Input 2를 반환합니다. 결과가 수정되지 않았습니다. 고급 버전은 [다중 스위치](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/blending/multi-switch/multi-switch.md)를 참조하세요.

전체 옵션 선택에 대해 복잡한 드롭다운 목록이 아닌 단일 버튼만 있으면 되는, 그래프에 부울(True/False) 선택 사항을 표시하는 데 매우 유용합니다.

중요: 입력에 적합한 버전을 사용해야 합니다. 색상 입력에는 &quot;전환&quot;을 사용하고, 회색 음영 입력에는 &quot;회색 음영 전환&quot;을 사용합니다.

</td>
</tr>
</table>

<a name="inputs"></a>

## 입력

|  |  |
|:---|:---|
| <b>입력 1(True)</b> <i>색상 또는 회색 음영 입력</i> |  |
| <b>입력 2(False)</b> <i>색상 또는 회색 음영 입력</i> |  |

<a name="parameters"></a>

## 매개변수

|  |  |
|:---|:---|
| <b>전환</b> <i>거짓/참</i> | 입력 1(True)과 2(False) 사이를 전환합니다. |
