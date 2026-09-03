---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/3d-view-library/hdri-tools/physical-sun-sky.html"
breadcrumb-title: ''
description: 실제 SunSky 노드를 사용하여 사실적인 재질 미리보기를 위해 물리적으로 정확한 태양과 하늘 조명 환경을 생성합니다.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > 3D View (Library) > HDRI Tools > Physical SunSky
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 실제 SunSky
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '155'
ht-degree: 9%

---


# 물리적 태양/하늘

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](physical-sun-sky.resources/physical-sun-sky-01.png){width="200px"}

<b>내부:</b> 3D 보기 > HDRI 도구

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 설명

Hosek-Wikie skylight 모델을 기반으로 한 물리적 태양과 하늘 구현 인공적인 HDRI를 위한 탁월한 기반을 제공합니다.

</td>
</tr>
</table>

<a name="parameters"></a>

## 매개변수

|  |  |
|:---|:---|
| <b>태양 위치</b> | range = [0,1]x[0,1] (경도-위도 각도) |
| <b>탁도</b> <i>1.0 - 10.0</i> | 탁도는 1~10입니다. |
| <b>알베도</b> <i>0.0 - 1.0</i> | 알베도 범위는 0에서 1까지입니다. |
| <b>배경색</b> <i>(색상 값)</i> | 지표 평면의 색입니다. |
| <b>노출(EV)</b> <i>-1.0 - 4.0</i> | 결과 출력의 노출 값입니다. |
| <b>태양 크기</b> <i>0.0 - 4.0</i> | 태양의 크기, 1과 다른 모든 값은 물리적으로 정확하지 않습니다. 값에 미묘한 효과가 있습니다! |
| <b>태양 강도</b> <i>0.0 - 1.0</i> | 태양 디스크의 강도입니다. 태양 원반은 상당히 작아서 효과가 즉시 보이지 않는다. |
| <b>하늘 강도</b> <i>0.0 - 1.0</i> | 하늘의 강렬함입니다. 또한 디스크 자체가 아니라 하늘의 태양이 산란하는 데에도 영향을 미칩니다. |

## 예

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="physical-sun-sky.resources/physical-sun-sky-02.gif" />
        </td>
    </tr>
</table>
