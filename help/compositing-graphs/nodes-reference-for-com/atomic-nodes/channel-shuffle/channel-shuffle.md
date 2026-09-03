---
helpx_url: "https://helpx.adobe.com/kr/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/atomic-nodes/channel-shuffle.html"
breadcrumb-title: ''
description: 색상 효과를 만들고 채널을 바꾸기 위해 텍스처의 색상 채널을 재정렬하려면 [채널 재편성] 노드를 사용합니다.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Atomic nodes > Channels shuffle
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 채널 셔플
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '269'
ht-degree: 7%

---


# 채널 셔플

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Atomic node: 채널 재편성](channel-shuffle.resources/channel-shuffle-01.png "Atomic node: 채널 재편성"){width="200px"}

</td>
<td width="100.00%" style="border: 0;" valign="top">

하나 또는 두 개의 입력 이미지의 색상 채널을 출력 이미지로 재정렬합니다.

즉, 두 개의 입력을 취하여 빨간색, 녹색, 파란색 및 Alpha 채널 중 하나를 전환하거나 입력의 채널 중 하나로 설정한 상태에서 출력을 반환할 수 있습니다.

기본적으로 이를 통해 가능한 모든 방식으로 RGB 채널을 포장하고 교체할 수 있습니다. 회색 음영 입력은 [색상]인 것처럼 처리됩니다. [빨강], [녹색], [파랑] 및 [Alpha] 모두 동일한 값을 반환합니다.

</td>
</tr>
</table>

Alpha 재편에는 기본 옵션이 있지만 대부분의 경우 채널 패킹 또는 채널 채널을 분리하고 설정하는 경우 [RGBA 병합](../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/channels/rgba-merge/rgba-merge.md), [RGBA 분할](../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/channels/rgba-split/rgba-split.md), [Alpha 병합](../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/channels/alpha-merge/alpha-merge.md) 및 [Alpha 분할](../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/channels/alpha-split/alpha-split.md)을 사용하는 것이 더 빠릅니다. 이 옵션은 여러 매개 변수를 변경하지 않고 나중에 회색 음영으로 변환할 필요가 없는 기본 작업을 수행하도록 설정됩니다. 더 많은 혼합 옵션이 포함된 고급 버전을 원하는 경우에는 [채널 혼합](../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/channel-mixer/channel-mixer.md)을 참조하세요.

<table>
<tr style="border: 0;">
<td width="100.00%" style="border: 0;" valign="top">



</td>
<td width="83.33%" style="border: 0;" valign="top">



</td>
<td width="100.00%" style="border: 0;" valign="top">



</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

## 출력 커넥터

</td>
<td style="border: 0;" valign="top">

### 예

</td>
</tr>
</table>

## 매개변수

|  |  |
| --- | --- |
| <b>빨강 채널</b> *정수* | 출력 이미지의 빨강 채널에 삽입할 소스 채널을 선택합니다. |
| <b>녹색 채널</b> *정수* | 출력 이미지의 녹색 채널에 삽입할 소스 채널을 선택합니다. |
| <b>파란색 채널</b> *정수* | 출력 이미지의 파란색 채널에 삽입할 소스 채널을 선택합니다. |
| <b>Alpha 채널</b> *정수* | 출력 이미지의 Alpha 채널에 삽입할 소스 채널을 선택합니다. |

## 입력 커넥터

|  |  |
| --- | --- |
| <b>입력 1</b> 기본 *색상/회색 음영* | 기본 입력 이미지입니다. |
| <b>입력 2</b> *색상/회색 음영* | 2차 입력 이미지. |

## 출력 커넥터

|  |  |
| --- | --- |
| <b>출력</b> *회색 음영/색상* |  |

## 예

*곧 출시 예정*
