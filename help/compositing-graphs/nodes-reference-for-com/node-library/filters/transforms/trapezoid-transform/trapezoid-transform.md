---
helpx_url: "https://helpx.adobe.com/kr/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/transforms/trapezoid-transform.html"
breadcrumb-title: ''
description: '[사다리꼴 변형] 노드를 사용하여 텍스처에 사다리꼴 왜곡을 적용하여 원근 교정 효과를 만듭니다.'
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Transforms > Trapezoid Transform
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 사다리꼴 변형
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '104'
ht-degree: 6%

---


# 사다리꼴 변형

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](trapezoid-transform.resources/trapeze-transform.png){width="128px"}

![](trapezoid-transform.resources/trapeze-transform-grayscale.png){width="128px"}

<b>필터</b>:

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 설명

원근/사다리꼴 뒤틀기 방식으로 입력을 수정하는 특수 변형 노드입니다. 위/아래 스트레치에 대한 컨트롤이 있습니다. 더 강한 효과를 위해 값을 한도를 넘어 푸시할 수 있습니다.

</td>
</tr>
</table>

<a name="parameters"></a>

## 매개변수

|  |  |
|:---|:---|
| <b>상단 늘리다</b> <i>0.0 - 1.0</i> | 상단의 스쿼시(squash)의 양을 설정합니다. |
| <b>밑단(bottom)</b> <i>0.0 - 1.0</i> | 바닥에 깔거나 쪼는 양을 설정합니다. |
| <b>배경색</b> <i>(회색 음영/색상 값)</i> | 타일링이 꺼진 경우 단색 배경색을 설정합니다. |
| <b>샘플링</b> <i>쌍선형, 가장 가까운</i> | 샘플링 품질을 설정합니다. |

## 예

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="trapezoid-transform.resources/trapeze-example.gif" />
        </td>
    </tr>
</table>
