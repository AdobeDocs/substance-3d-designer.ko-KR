---
helpx_url: "https://helpx.adobe.com/kr/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/3d-view-library/hdri-tools/gradient-linear-hdri.html"
breadcrumb-title: ''
description: 사용자 정의 조명 설정을 위해 HDRI 환경에서 선형 그레이디언트를 만들려면 [그레이디언트 선형 HDRI] 노드를 사용합니다.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > 3D View (Library) > HDRI Tools > Gradient Linear (HDRI)
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 선형 그레이디언트(HDRI)
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '102'
ht-degree: 4%

---


# 선형 그레이디언트(HDRI)

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](gradient-linear-hdri.resources/gradient-linear-hdri-01.png){width="200px"}

<b>내부:</b> 3D 보기 > HDRI 도구

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 설명

사용자가 놓은 점으로 중앙을 가로질러 [선형 그레이디언트]를 만듭니다. 일반 [그레이디언트 선형 1](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/gradient-linear-1/gradient-linear-1.md)과 달리 구형 투영에 맞게 최종 결과가 조정됩니다.

</td>
</tr>
</table>

<a name="parameters"></a>

## 매개변수

|  |  |
|:---|:---|
| <b>포인트 위치</b> | 그레이디언트 방향을 결정하는 데 사용되는 색조의 위치입니다. |
| <b>위쪽 색상</b> <i>(색상 값)</i> | 그라디언트 위쪽 부분의 색상(지점) |
| <b>아래쪽 색상</b> <i>(색상 값)</i> | 그레이디언트 아랫부분의 색상(점에서 반대 방향). |
| <b>대비</b> <i>0.0 - 1.0</i> | 결과의 대비를 조정합니다. |

## 예

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="gradient-linear-hdri.resources/gradient-linear-hdri-02.gif" />
        </td>
    </tr>
</table>
