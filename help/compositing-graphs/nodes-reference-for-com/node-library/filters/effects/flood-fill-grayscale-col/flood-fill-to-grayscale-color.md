---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/flood-fill-to-grayscale-color.html"
breadcrumb-title: ''
description: '[회색 음영 색상 Flood Fill]를 사용하여 연결된 영역을 회색 음영 색상으로 채워 단색 패턴을 만듭니다.'
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Flood Fill to GrayscaleColor
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: GrayscaleColor로 Flood Fill
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '162'
ht-degree: 4%

---


# 회색 음영/색상 Flood Fill

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](flood-fill-to-grayscale-color.resources/flood-fill-to-grayscale-color-01.png){width="128px"}

![](flood-fill-to-grayscale-color.resources/flood-fill-to-grayscale-color-02.png){width="128px"}

<b>인:</b> 필터 > 효과

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 설명

Flood Fill 데이터를 사용하여 회색 음영 또는 색상 값 견본을 생성합니다. [임의 회색 음영에 Flood Fill](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/flood-fill-random-gra/flood-fill-to-random-grayscale.md)와 달리, 이 두 노드를 사용하면 더 많은 컨트롤을 통해 정확한 변형 및 톤을 설정할 수 있으며 셀 단위로 임의화할 기본 값을 결정하는 추가 입력 맵이 제공됩니다.

이 시스템은 모든 셀에 고유한 값이나 색상을 제공하면서도 제어를 유지하고 미리 정해진 입력을 제거하는 강력한 시스템입니다.

</td>
</tr>
</table>

<a name="inputs"></a>

## 입력

|  |  |
|:---|:---|
| <b>Flood Fill</b> <i>색상 입력</i> |  |
| <b>회색 음영/색상 입력</b> <i>회색 음영/색상 입력</i> |  |

<a name="parameters"></a>

## 매개변수

|  |  |
|:---|:---|
| <b>광도/색상 조정</b> <i>-1.0 - 1.0</i> | 노드에 대한 바이어스 또는 기준 값을 설정합니다. [회색 음영] 또는 [색상] 입력을 사용할 때 이 입력을 사용하여 초기 값을 시작점으로 변경할 수 있습니다. |
| <b>광도/색상 무작위</b> <i>-1.0 - 1.0</i> | 변화의 양을 설정합니다. |
