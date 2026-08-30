---
helpx_url: "https://helpx.adobe.com/kr/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/adjustments/highpass.html"
breadcrumb-title: ''
description: '[하이패스] 노드를 사용하면 텍스처에서 높은 주파수의 세부 정보를 추출하여 선명 효과 및 세부 사항 향상 효과를 만들 수 있습니다.'
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Adjustments > Highpass
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 하이패스
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '103'
ht-degree: 4%

---


# 하이패스

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](highpass.resources/high-pass-greyscale.png){width="128px"}

![](highpass.resources/high-pass.png){width="128px"}

<b>내부:</b> 필터 > 조정

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 설명

회색 음영 버전뿐만 아니라 컬러로도 사용할 수 있는 하이패스 필터를 수행합니다. 이름이 같은 Photoshop 액션과 유사합니다.\
타일링을 위해 텍스처를 정리하는 경우처럼 이미지에서 큰 광도 차이를 제거하는 데 유용합니다.

중요: 입력에 적합한 버전을 사용해야 합니다. 색상 입력에는 &quot;하이패스&quot;를 사용하고 회색 음영 입력에는 &quot;하이패스 회색 음영&quot;을 사용합니다.

</td>
</tr>
</table>

<a name="parameters"></a>

## 매개변수

|  |  |
|:---|:---|
| <b>반경</b> <i>0.0 - 64.0</i> | 필터 반경: 작은 반경은 작은 차이를 제거하고, 큰 반경은 큰 영역을 제거합니다. |

## 예

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="highpass.resources/highpass.gif" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="highpass.resources/highpass-example.png" />
        </td>
    </tr>
</table>
