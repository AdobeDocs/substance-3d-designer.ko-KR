---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/blending/multi-switch.html"
breadcrumb-title: ''
description: 조건부 텍스처 선택을 위한 선택기를 기반으로 다중 스위치 노드를 사용하여 여러 입력 텍스처 간에 전환할 수 있습니다.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Blending > Multi Switch
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 다중 스위치
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '147'
ht-degree: 4%

---


# 다중 스위치

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](multi-switch.resources/multi-switch-greyscale.png){width="128px"}

![](multi-switch.resources/multi-switch.png){width="128px"}

<b>내부:</b> 필터 > 혼합

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 설명

&#39;Input Selection&#39; 매개 변수에 정의된 입력만 전달하는 스위치 상자로 작동합니다. 따라서 두 개의 입력이 연결된 경우 사용자의 선택에 따라 그 중 하나만 반환(수정되지 않음)됩니다.

그래프에 다양한 옵션을 추가하는 데 매우 유용합니다. [노출](../../../../../../compositing-graphs/manage-parameters/exposing-a-parameter/exposing-a-parameter.md)(바람직하게는 드롭다운 목록)과 함께 사용하면 많은 사용자 지정이 가능합니다.

중요: 입력에 적합한 버전을 사용해야 합니다. 색상 입력에는 &quot;다중 스위치&quot;를 사용하고 회색 음영 입력에는 &quot;다중 스위치 회색 음영&quot;을 사용합니다.

</td>
</tr>
</table>

<a name="inputs"></a>

## 입력

|  |  |
|:---|:---|
| <b>입력 1-20</b> <i>색상 입력</i> |  |

<a name="parameters"></a>

## 매개변수

|  |  |
|:---|:---|
| <b>입력 번호</b> <i>2 - 20</i> | 표시할 입력의 양입니다. 중요: 연결 수가 줄어들면 연결을 제거하지 않습니다. |
| <b>선택 항목 입력</b> <i>1 - 20</i> | 결과로 반환할 입력 |
