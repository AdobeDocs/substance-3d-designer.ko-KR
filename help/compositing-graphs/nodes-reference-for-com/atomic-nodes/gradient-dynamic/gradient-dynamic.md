---
helpx_url: "https://helpx.adobe.com/kr/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/atomic-nodes/gradient-dynamic.html"
breadcrumb-title: ''
description: 입력 매개 변수 및 값으로 제어할 수 있는 동적 그레이디언트를 만들려면 [그레이디언트(동적)] 노드를 사용합니다.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Atomic nodes > Gradient (Dynamic)
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 그래디언트(동적)
user-guide-description: ''
user-guide-title: ''
source-git-commit: ea96f5a148246d20263c4ecf0b67d0b4a51f28a8
workflow-type: tm+mt
source-wordcount: '318'
ht-degree: 9%

---


# 그래디언트(동적)

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Atomic node: Gradient dynamic](../../../../assets/comp_dyngradient_1.png "Atomic node: Gradient dynamic"){width="200px"}

</td>
<td width="100.00%" style="border: 0;" valign="top">

다른 이미지의 픽셀 행 또는 열이 제공되는 그레이디언트를 사용하여 이미지의 회색 음영 값을 재매핑합니다.

이 기능은 그레이디언트 노드의 간단한 대체 역할을 하지만 그레이디언트 노드와 달리 그레이디언트 색상 키는 내부적으로 정의되지 않고 외부 입력에서 가져옵니다.

</td>
</tr>
</table>

이는 주로 색상에 대한 파라미터가 노드 밖으로 이동되기 때문에 파라미터를 노출할 수 없는 문제를 회피할 수 있게 한다. 이것이 그것을 &quot;역동적인&quot; 것으로 만드는 것이다.

그레이디언트(동적) 자체는 사용하기 어려운 노드가 아니지만 사용 방법은 좀 더 고급입니다. 대부분의 표준 사용법은 일반 그레이디언트 노드에서 다룰 수 있습니다.

이 노드는 그레이디언트 편집기의 키 시스템에 의해 너무 제한되어 있고 색상 및 경사 위치가 그래프의 다른 입력, 매개 변수 및 부분에 의해 제어되도록 하려는 경우에 사용할 수 있습니다.

또는 단일 경사 입력 내부에 저장된 여러 그레이디언트를 번갈아 사용하는 데 그레이디언트 입력 위치 슬라이더를 사용할 수 있습니다.

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
| <b>그레이디언트 주소 지정</b> *부울* | 그라디언트가 반복(타일)되는지 또는 클램프되는지를 설정합니다.   이 매개 변수는 회색 음영 입력의 [0, 1] 범위 HDR 픽셀을 처리하는 방법을 결정합니다. 클램프하거나 [0, 1]까지 접습니다. |
| <b>그레이디언트 방향</b> *정수* | &#39;그레이디언트 입력&#39;을 샘플링할 축을 설정합니다.<ul data-preserve-html="true"> <li data-preserve-html="true"><i>가로:</i> X축을 기준으로 픽셀 행을 샘플링합니다.</li> <li data-preserve-html="true"><i>세로:</i> Y축에서 픽셀 열을 샘플링합니다.</li> </ul> |
| <b>그레이디언트 입력 위치</b> *부동* | &#39;그레이디언트 입력&#39;에서 샘플링할 픽셀의 행 또는 열의 정규화된 위치입니다. |

## 입력 커넥터

|  |  |
| --- | --- |
| <b>회색 음영 입력</b> *회색 음영* 기본 | 다시 매핑할 회색 음영 이미지입니다. |
| <b>그레이디언트 입력</b> *색상/회색 음영* | 이 이미지에서 그레이디언트가 샘플링됩니다 |

## 출력 커넥터

|  |  |
| --- | --- |
| <b>출력</b> *색상/회색 음영* |  |

## 예

*곧 출시 예정*
