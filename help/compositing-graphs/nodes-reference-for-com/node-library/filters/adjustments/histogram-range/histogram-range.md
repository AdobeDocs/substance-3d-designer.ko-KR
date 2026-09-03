---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/adjustments/histogram-range.html"
breadcrumb-title: ''
description: '[막대 그래프 범위] 노드를 사용하여 색상 교정 및 조정을 위해 막대 그래프 범위를 기반으로 막대 그래프 값을 다시 매핑할 수 있습니다.'
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Adjustments > Histogram Range
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 히스토그램 범위
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '130'
ht-degree: 5%

---


# 히스토그램 범위

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](histogram-range.resources/histogram-range-01.png){width="128px"}

<b>내부:</b> 필터 > 조정

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 설명

회색 음영 입력의 범위를 줄이거나 이동합니다. [대비 광도](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/contrast-luminosity/contrast-luminosity.md)와 비슷하게 전환을 다시 매핑하는 데 사용할 수 있지만, 상황에 따라 더 유용하게 사용할 수 있는 다양한 컨트롤을 사용할 수 있습니다.\
범위를 다시 매핑하는 더 유용한 다른 방법은 [막대 그래프 스캔](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/histogram-scan/histogram-scan.md)을 참조하십시오.

[히스토그램 범위에서 Substance 아카데미 비디오를 시청하려면 여기를 클릭하십시오.](https://www.youtube.com/watch?v=p9wcmJBFyGA&t=517s)

</td>
</tr>
</table>

<a name="parameters"></a>

## 매개변수

|  |  |
|:---|:---|
| <b>범위</b> <i>0.0 - 1.0</i> | 범위를 얼마나 줄일 수 있습니까? 이는 [최소 레벨] 및 [최대 레벨] 슬라이더를 모두 내부로 이동하는 것과 비슷합니다. |
| <b>위치</b> <i>0.0 - 1.0</i> | 범위 감소의 오프셋, 범위 감소의 다른 중간점 설정. |

## 예

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="histogram-range.resources/histogram-range-02.gif" />
        </td>
    </tr>
</table>
