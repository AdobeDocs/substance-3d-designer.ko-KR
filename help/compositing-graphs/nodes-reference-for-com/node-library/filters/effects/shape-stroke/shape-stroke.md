---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/shape-stroke.html"
breadcrumb-title: ''
description: 모양 선 노드를 사용하여 테두리와 가장자리 효과를 만들기 위해 모양에 선 윤곽선을 추가합니다.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Shape Stroke
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 모양 선
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '158'
ht-degree: 4%

---


# 모양 선

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](shape-stroke.resources/shape-stroke-01.png){width="128px"}

![](shape-stroke.resources/shape-stroke-02.png){width="128px"}

<b>인:</b> 필터 > 효과

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 설명

다른 2D 이미지 편집 애플리케이션에서 익숙한 것처럼 흑백 마스크(회색 음영 버전) 또는 알파 채널이 있는 모양(색상 버전) 주위에 획이나 윤곽선을 추가합니다. [Edge Detect](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/edge-detect/edge-detect.md)의 더 완전한 버전으로 볼 수 있습니다.

다양한 이미지 편집 효과에 매우 유용합니다.

</td>
</tr>
</table>

<a name="parameters"></a>

## 매개변수

|  |  |
|:---|:---|
| <b>너비</b> <i>-1.0 - 1.0</i> | 선 효과의 폭입니다. |
| <b>불투명도</b> <i>0.0 - 1.0</i> | 효과의 전체 불투명도 |
| <b>(윤곽선) 색상</b> <i>(색상 값)</i> | 윤곽선 효과에 사용되는 색상입니다. |
| <b>마스크 색상</b> <i>(색상 값)(회색 음영 버전만)</i> | 투명도 매핑 출력에 사용되는 단색입니다. |
| <b>미리 곱하기</b> <i>False/True(색상 버전만)</i> | 입력을 미리 곱하기로 가정해야 하는지 여부입니다. |
| <b>미리 곱하기 출력</b> <i>거짓/참</i> | 출력을 미리 곱해야 하는지 여부입니다. |

## 예

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="shape-stroke.resources/shape-stroke-03.png" />
        </td>
    </tr>
</table>
