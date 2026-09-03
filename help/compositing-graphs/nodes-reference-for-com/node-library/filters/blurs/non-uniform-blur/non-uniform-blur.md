---
helpx_url: "https://helpx.adobe.com/kr/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/blurs/non-uniform-blur.html"
breadcrumb-title: ''
description: 비균일 흐림 효과 노드를 사용하면 비등방성 효과를 내기 위해 X 방향과 Y 방향으로 강도를 달리하는 흐림 효과를 적용할 수 있습니다.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Blurs > Non Uniform Blur
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 균일하지 않은 흐림 효과
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '177'
ht-degree: 9%

---


# 균일하지 않은 흐림 효과

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](non-uniform-blur.resources/non-uniform-blur-01.png){width="128px"}

![](non-uniform-blur.resources/non-uniform-blur-02.png){width="128px"}

<b>인:</b> 필터 > 흐림 효과

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 설명

고품질 흐림 효과를 수행합니다. 여기서 강도는 입력 마스크에 의해 구동됩니다. 옵션을 사용하여 비등방성 및 측정 기능을 추가할 수 있습니다.

</td>
</tr>
</table>

<a name="inputs"></a>

## 입력

|  |  |
|:---|:---|
| <b>흐림 효과 맵</b> <i>회색 음영 입력</i> | 마스크 맵을 사용하여 효과 강도를 설정합니다. |

<a name="parameters"></a>

## 매개변수

|  |  |
|:---|:---|
| <b>강도</b> <i>0.0 - 50.0</i> | 흐림 효과를 적용할 최대 강도입니다. 흐림 효과 맵으로 마스크되어 이 설정은 해당 맵의 검정 영역에는 영향을 주지 않습니다. |
| <b>비등방성</b> <i>0.0 - 1.0</i> | 필요에 따라 흐림 효과에 방향성을 추가합니다. 각도 매개변수에 의해 제어됩니다. |
| <b>비대칭</b> <i>0.0 - 1.0</i> | 선택적으로 샘플링에 편의를 추가합니다. 각도 매개변수에 의해 제어됩니다. |
| <b>각도</b> <i>0.0 - 1.0</i> | 각도 - 방향성과 샘플링 편향을 설정합니다. |
| <b>샘플</b> <i>1 - 16</i> | 샘플의 양에 따라 품질이 결정됩니다. 블레이드의 양을 곱합니다. |
| <b>블레이드</b> <i>1 - 9</i> | 샘플링 섹터의 양은 품질을 결정합니다. 샘플 양을 곱합니다. |

## 예

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="non-uniform-blur.resources/non-uniform-blur-03.gif" /><br><i>아래 예제는 [흐림 효과 맵] 슬롯의 90도 경사도에 의해 구동됩니다.</i>
        </td>
    </tr>
</table>
