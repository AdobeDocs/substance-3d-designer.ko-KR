---
helpx_url: "https://helpx.adobe.com/kr/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/adjustments/histogram-scan.html"
breadcrumb-title: ''
description: '[막대 그래프 스캔] 노드를 사용하여 색상 교정 및 조정을 위한 텍스처 막대 그래프를 스캔하고 분석할 수 있습니다.'
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Adjustments > Histogram Scan
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 막대 그래프 스캔
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '146'
ht-degree: 4%

---


# 막대 그래프 스캔

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](histogram-scan.resources/histogram-scan-01.png){width="128px"}

<b>내부:</b> 필터 > 조정

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 설명

입력 회색 음영 이미지의 대비와 명도를 다시 매핑하는 직관적인 방법을 제공하는 매우 간단하면서도 유용한 노드입니다. 동적 방식으로 마스크를 &quot;확장&quot; 및 &quot;축소&quot;하는 데 사용할 수 있습니다.

[히스토그램 작업에 대한 Substance 아카데미 비디오를 시청하려면 여기를 클릭하십시오.](https://www.youtube.com/watch?v=p9wcmJBFyGA&t=427s)

</td>
</tr>
</table>

<a name="parameters"></a>

## 매개변수

|  |  |
|:---|:---|
| <b>위치</b> <i>0.0 - 1.0</i> | 명도 컨트롤과 비슷하게 결과의 중간점을 이동합니다. 그라디언트 입력에 사용하면 전환점이 확장되고 축소됩니다.<br><br>중요: 기본값이 0이면 끝 결과가 항상 검정색이므로 0.5부터 시작해 보세요! |
| <b>대비</b> <i>0.0 - 1.0</i> | 결과의 대비를 조정합니다. 전환의 경도를 설정하는 데 사용할 수 있습니다. |
| <b>위치 반전</b> <i>거짓/참</i> | 최종 결과를 반전합니다. |

## 예

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="histogram-scan.resources/histogram-scan-02.gif" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="histogram-scan.resources/histogram-scan-03.gif" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="histogram-scan.resources/histogram-scan-04.gif" />
        </td>
    </tr>
</table>
