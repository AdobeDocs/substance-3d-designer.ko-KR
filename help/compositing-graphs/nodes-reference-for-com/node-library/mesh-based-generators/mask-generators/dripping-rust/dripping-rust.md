---
helpx_url: "https://helpx.adobe.com/kr/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/mask-generators/dripping-rust.html"
breadcrumb-title: ''
description: 드리핑 녹 노드를 사용하여 메쉬 기하학과 중력 방향을 기반으로 녹 드립 패턴을 생성합니다.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Mask Generators > Dripping Rust
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 드리핑 녹
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '211'
ht-degree: 7%

---


# 드리핑 녹

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](dripping-rust.resources/dripping-rust-01.png){width="128px"}

<b>내부:</b> 메시 기반 생성기 > 마스크 생성기

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 설명

베이킹된 맵 및 사용자 설정을 기반으로 흑백 마스크를 생성합니다. [Painter](https://support.allegorithmic.com/documentation/display/SPDOC/Substance+Painter)의 [스마트 마스크](https://support.allegorithmic.com/documentation/display/SPDOC/Smart+Materials+and+Masks)와 비슷합니다.

이 마스크는 흘러내리는 누출과 함께 녹 플레이크 및 스펙을 나타냅니다.

</td>
</tr>
</table>

<a name="inputs"></a>

## 입력

|  |  |
|:---|:---|
| <b>곡률</b> <i>회색 음영 입력</i> | 녹 배치에 도움이 되도록 맵을 작성하거나 생성했습니다. |
| <b>주변 오클루전</b> <i>회색 음영 입력</i> | 녹 배치에 도움이 되도록 맵을 작성하거나 생성했습니다. |
| <b>위치</b> <i>회색 음영 입력</i> | 점적 방향에 대해 구워지거나 생성된 맵 |
| <b>마스크(선택 사항)</b> <i>회색 음영 입력</i> | 노드의 효과를 마스킹하는 데 사용되는 마스크 슬롯입니다. |

<a name="parameters"></a>

## 매개변수

|  |  |
|:---|:---|
| <b>녹 확산</b> <i>0.0 - 1.0</i> | 녹 양에 대한 기본 컨트롤입니다. |
| <b>녹 대비</b> <i>0.0 - 1.0</i> | 생성된 녹 스펙의 대비 정도를 설정합니다. 물방울에는 영향을 주지 않습니다. |
| <b>Smoothness 확산</b> <i>0.0 - 1.0</i> | 녹 얼개에 적용할 흐림/번짐 효과의 양입니다. |
| <b>드립 강도</b> <i>0.0 - 1.0</i> | 반점에서 물방울의 강도와 길이를 설정합니다. |
| <b>드립스 Smoothness</b> <i>0.0 - 1.0</i> | 물방울에 적용할 흐림 효과 및 매끄러움 정도입니다. |
| <b>드립스 샘플 양</b> <i>0 - 32</i> | 물방울 효과의 품질 수준(단계)을 설정합니다. 속도에 약간의 영향을 미칩니다. |

## 예

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="dripping-rust.resources/dripping-rust-02.gif" />
        </td>
    </tr>
</table>
