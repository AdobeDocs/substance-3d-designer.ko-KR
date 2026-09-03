---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/mask-generators/cloth-wear.html"
breadcrumb-title: ''
description: 천 마모 노드를 사용하여 메쉬 곡률 및 접촉 영역을 기반으로 천 표면에 마모 마스크를 생성합니다.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Mask Generators > Cloth Wear
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 천 마모
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '162'
ht-degree: 4%

---


# 천 마모

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](cloth-wear.resources/cloth-wear-01.png){width="128px"}

<b>내부:</b> 메시 기반 생성기 > 마스크 생성기

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 설명

베이킹된 맵 및 사용자 설정을 기반으로 흑백 마스크를 생성합니다. [Painter](https://support.allegorithmic.com/documentation/display/SPDOC/Substance+Painter)의 [스마트 마스크](https://support.allegorithmic.com/documentation/display/SPDOC/Smart+Materials+and+Masks)와 비슷합니다.

마스크는 천 재질의 가장자리가 마모된 것을 나타냅니다. 대부분의 룩을 결정하는 천 세부 묘사 Heightmap을 사용합니다. 적절한 맵이 없으면 효과는 매우 기본적인 것처럼 보입니다.

</td>
</tr>
</table>

<a name="inputs"></a>

## 입력

|  |  |
|:---|:---|
| <b>천 Height</b> <i>회색 음영 입력</i> | 천 패턴 전용 Height. 이것은 (구운) 오브젝트의 Height이 아니라 타일링 세부 패턴입니다. |
| <b>마스크(선택 사항)</b> <i>회색 음영 입력</i> | 노드의 효과를 마스킹하는 데 사용되는 마스크 슬롯입니다. |
| <b>곡률</b> <i>회색 음영 입력</i> | 구겨진/생성된 곡률로 솟아오른 모서리를 결정합니다. |

<a name="parameters"></a>

## 매개변수

|  |  |
|:---|:---|
| <b>하드 에지 양</b> <i>0.0 - 1.0</i> |  |
| <b>부드러움 착용</b> <i>0.0 - 5.0</i> | 마모된 가장자리가 얼마나 흐려지거나 부드러운지를 결정합니다. |

## 예

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="cloth-wear.resources/cloth-wear-02.gif" />
        </td>
    </tr>
</table>
