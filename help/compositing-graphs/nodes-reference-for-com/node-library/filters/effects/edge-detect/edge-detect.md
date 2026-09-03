---
helpx_url: "https://helpx.adobe.com/kr/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/edge-detect.html"
breadcrumb-title: ''
description: '[가장자리 감지] 노드를 사용하면 윤곽선 및 가장자리 기반 마스크 효과를 만들기 위한 텍스처의 가장자리를 감지할 수 있습니다.'
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Edge Detect
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 가장자리 감지
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '122'
ht-degree: 7%

---


# 가장자리 감지

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](edge-detect.resources/edge-detect-01.png){width="128px"}

<b>인:</b> 필터 > 효과

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 설명

흑백 이미지의 대비를 감지한 다음 대비를 강조하는 흑백 마스크를 만듭니다.

가장자리를 위한 일종의 마스크가 필요한 많은 경우에 유용합니다. 이 옵션은 고대비 입력에서 가장 효과적이라는 점에 유의하십시오. 필요한 경우 이 노드에 내용을 전달하기 전에 대비를 조정하십시오.

</td>
</tr>
</table>

<a name="parameters"></a>

## 매개변수

|  |  |
|:---|:---|
| <b>가장자리 너비</b> <i>1.0 - 16.0</i> | 가장자리 주위의 검색된 영역의 폭입니다. |
| <b>모서리 둥글기</b> <i>0.0 - 16.0</i> | 생성된 마스크를 함께 둥글게 하고, 흐리게 하고, 매끄럽게 합니다. |
| <b>반전</b> <i>거짓/참</i> | 결과를 반전합니다. |
| <b>허용치</b> <i>0.0 - 1.0</i> | 모서리가 나타나야 하는 위치의 공차 범위 요소입니다. |

## 예

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="edge-detect.resources/edge-detect-02.png" />
        </td>
    </tr>
</table>
