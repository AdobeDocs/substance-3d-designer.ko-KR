---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/mask-generators/light.html"
breadcrumb-title: ''
description: 조명 노드를 사용하여 사실적인 재질 변형을 만들기 위해 메시 조명 조건을 기반으로 마스크를 생성합니다.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Mask Generators > Light
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 조명
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '138'
ht-degree: 9%

---


# 조명

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](light.resources/light-01.png){width="128px"}

<b>내부:</b> 메시 기반 생성기 > 마스크 생성기

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 설명

베이킹된 맵 및 사용자 설정을 기반으로 흑백 마스크를 생성합니다. [Painter](https://support.allegorithmic.com/documentation/display/SPDOC/Substance+Painter)의 [스마트 마스크](https://support.allegorithmic.com/documentation/display/SPDOC/Smart+Materials+and+Masks)와 비슷합니다.

이 마스크는 다른 Generator와 약간 다릅니다. 순수하게 World Space Normalmap을 기반으로 가짜 조명을 수행하여 흑백 &quot;라이트맵&quot; 마스크를 반환합니다.

</td>
</tr>
</table>

<a name="parameters"></a>

## 매개변수

|  |  |
|:---|:---|
| <b>수평 각도</b> <i>0.0 - 1.0</i> | 페이크 라이트의 수평 각도를 설정합니다. |
| <b>수직 각도</b> <i>0.0 - 1.0</i> | 페이크 라이트의 수직 각도를 설정합니다. |
| <b>밝은 광택</b> <i>0.0 - 0.999</i> | 강조 표시된 영역의 밝기 감소 스프레드를 설정합니다. |
| <b>밝은 영역 수준</b> <i>0.0 - 1.0</i> | 강조 표시된 영역의 명도 레벨을 설정합니다. |

## 예

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="light.resources/light-02.gif" />
        </td>
    </tr>
</table>
