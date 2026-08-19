---
helpx_url: "https://helpx.adobe.com/kr/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/atomic-nodes/grayscale-conversion.html"
breadcrumb-title: ''
description: 다양한 변환 방법을 사용하여 색상 텍스처를 회색 음영으로 변환하려면 [회색 음영 변환] 노드를 사용합니다.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Atomic nodes > Grayscale conversion
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 회색 음영 전환
user-guide-description: ''
user-guide-title: ''
source-git-commit: ea96f5a148246d20263c4ecf0b67d0b4a51f28a8
workflow-type: tm+mt
source-wordcount: '282'
ht-degree: 7%

---


# 회색 음영 전환

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![원자 노드: 회색 음영 변환](../../../../assets/comp_grayscaleconversion_1.png "원자 노드: 회색 음영 변환"){width="200px"}

</td>
<td width="100.00%" style="border: 0;" valign="top">

각 컬러 채널의 휘도를 측정하여 컬러 이미지를 회색조로 변환합니다.

이 노드는 1로 설정되어야 하는 원하는 채널을 제외하고 모든 &#39;채널 가중치&#39; 값을 0으로 설정하여 컬러 이미지에서 회색 음영 채널을 추출하는 최적화된 방법으로 사용할 수 있습니다.

</td>
</tr>
</table>

대부분의 노드는 회색 음영이나 색상으로 출력하도록 설정할 수 있습니다. 여기서 전자는 단순성과 성능을 위해 선호됩니다.

실제로, [그레이디언트 맵](../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/gradient-map/gradient-map.md) 노드와 같은 노드를 사용하여 처음부터 회색 음영으로 작업하고 작업 과정 후반부에 이미지를 색상화하는 것이 좋습니다.

즉, 일반적으로 회색 음영 변환 노드는 컬러 이미지를 회색 음영으로 변환할 경우에만 예약되어 있습니다. 이러한 경우 [회색 음영 변환 고급](../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/grayscale-conversion-adv/grayscale-conversion-advanced.md) 및 [색상을 마스크로 변환](../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/color-to-mask/color-to-mask.md)도 살펴봅니다.

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

## 매개변수

</td>
<td style="border: 0;" valign="top">

### 입력 커넥터

</td>
<td style="border: 0;" valign="top">

### 출력 커넥터

</td>
<td style="border: 0;" valign="top">

### 예

</td>
</tr>
</table>

## 매개변수

|  |  |
| --- | --- |
| <b>채널 두께</b> *Float4* | 회색 음영 변환에 있는 각 RGBA 채널의 두께를 설정합니다.   기본적으로 RGB 채널 전체에서 균일 분할이 수행됩니다. |
| <b>알파 병합</b> *부울* | 회색 음영 값에는 Alpha 정보를 포함할 수 없으므로 최종 회색 음영 결과에서 Alpha의 동작을 설정합니다.   *True*&#x200B;이면 회색 음영 변환이 입력 이미지의 Alpha 채널에 곱해집니다 |
| <b>배경 값</b> *부동* | 입력에 알파 마스크가 있을 때 기본 배경 값을 설정합니다. 즉, 어떤 픽셀들이 투명도로 취급될 것인지를 결정한다.   *&#39;알파 병합&#39;이 &#39;True&#39;로 설정된 경우 사용할 수 있습니다.* |

## 입력 커넥터

|  |  |
| --- | --- |
| <b>입력</b> 기본 *색상* | 처리할 색상 이미지입니다. |

## 출력 커넥터

|  |  |
| --- | --- |
| <b>출력</b> *회색 음영* |  |

## 예

*곧 출시 예정*
