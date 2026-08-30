---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/adjustments/replace-color-range.html"
breadcrumb-title: ''
description: 색상 범위 바꾸기 노드를 사용하여 지정된 범위 내의 색상을 색상 교정을 위한 새 색상으로 바꿉니다.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Adjustments > Replace Color Range
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 색상 범위 바꾸기
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '124'
ht-degree: 5%

---


# 색상 범위 바꾸기

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](replace-color-range.resources/replace-color-range.png){width="128px"}

<b>내부:</b> 필터 > 조정

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 설명

소스 색상을 대상 색상으로 대체하고 추가 컨트롤을 사용합니다. 예를 들어 재질 ID 맵의 일부를 다시 채색하는 데 사용할 수 있습니다(bake).

고급 버전은 [색상 일치](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/color-match/color-match.md)를 참조하세요.

</td>
</tr>
</table>

<a name="parameters"></a>

## 매개변수

|  |  |
|:---|:---|
| <b>소스 색상</b> <i>(색상 값)</i> | 대체할 색상입니다. |
| <b>대상 색상</b> <i>(색상 값)</i> | 대체할 색상입니다. |
| <b>원본 범위</b> <i>0.0 - 1.0</i> | 선택된 출처의 범위 또는 허용한도입니다. 인접한 다른 색상에 색조가 변경되도록 추가할 수 있습니다. |
| <b>임계값</b> <i>0.0 - 1.0</i> | 범위를 위한 밝기 감소/대비. 소스 색상만 바꾸려면 [낮음]으로 설정하고, 소스로의 혼합 색상도 바꾸려면 [높음]으로 설정합니다. |

## 예

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="replace-color-range.resources/replace-color-range-example.png" />
        </td>
    </tr>
</table>
