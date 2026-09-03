---
helpx_url: "https://helpx.adobe.com/kr/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/transforms/quad-transform.html"
breadcrumb-title: ''
description: 원근 교정 및 뒤틀기를 위해 4차원 변형을 텍스처에 적용하려면 [4차원 변형] 노드를 사용합니다.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Transforms > Quad Transform
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 쿼드 변형
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '110'
ht-degree: 2%

---


# 쿼드 변형

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](quad-transform.resources/quad-transform-01.png){width="128px"}

![](quad-transform.resources/quad-transform-02.png){width="128px"}

<b>필터</b>:

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 설명

모퉁이점과의 상호 작용을 통해 쿼드 모양의 변형을 허용하는 특별한 변형 노드. 매우 구체적인 변형 작업을 직접 수행할 수 있습니다.

</td>
</tr>
</table>

<a name="parameters"></a>

## 매개변수

|  |  |
|:---|:---|
| <b>p00</b> | 왼쪽 상단. |
| <b>p01</b> | 왼쪽 아래 점 |
| <b>p10</b> | 오른쪽 상단 |
| <b>p11</b> | 오른쪽 하단 포인트. |
| <b>컬링</b> <i>앞면 전용, 뒷면 전용, 앞면/뒷면</i> | 점이 서로 교차할 때 모양의 컬링/숨기기를 설정합니다. |
| <b>타일링 사용</b> <i>거짓/참</i> |  |
| <b>배경색</b> <i>(회색 음영 값)</i> | 타일링이 꺼져 있는 경우 단색 배경색입니다. |
| <b>샘플링</b> <i>쌍선형, 가장 가까운</i> | 샘플링 품질을 설정합니다. |

## 예

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="quad-transform.resources/quad-transform-03.gif" />
        </td>
    </tr>
</table>
