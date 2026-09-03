---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/noises/directional-scratches.html"
breadcrumb-title: ''
description: 방향 Scratches 노드를 사용하여 방향 스크래치 패턴을 만들어 재료에 마모 및 손상 효과를 추가합니다.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Noises > Directional scratches
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 직접 스크래치
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '360'
ht-degree: 1%

---


# 직접 스크래치

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![방향 스크래치 - 아이콘](directional-scratches.resources/directional-scratches-01.png "방향 스크래치 - 아이콘"){width="200px"}

<b>내부:</b> 텍스처 생성기 > 노이즈

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 설명

각도 및 크기를 조정할 수 있는 스크래치 패턴의 임의 분산.

</td>
</tr>
</table>

<a name="outputs"></a>

## 출력

|  |  |
|:---|:---|
| <b>출력</b> <i>회색 음영</i> | 회색 음영 비트맵으로 생성된 노이즈 |

<a name="parameters"></a>

## 매개변수

|  |  |
|:---|:---|
| <b>크기 조절</b> <i>정수</i> | 노이즈 타일을 생성하는 데 사용되는 격자의 하위 분할입니다.    값이 높을수록 더 많은 타일이 그려지고 노이즈가 더 많아집니다. |
| <b>장애</b> <i>부동</i> | 소음의 성분을 제거합니다.    이 효과를 사용하면 노이즈에 애니메이션을 적용할 수 있습니다. |
| <b>장애 속도</b> <i>부동</i> | <b>Disorder</b> 매개 변수에 의해 적용된 변위의 거리를 조정합니다.    이 효과는 노이즈에 애니메이션을 적용할 때 변위 속도를 제어하는 데 사용할 수 있습니다. |
| <b>장애 비등방성</b> <i>부동</i> | <b>Disorder</b> 매개 변수에 의해 적용된 변위의 방향 범위를 제어합니다. 값이 높을수록 방향이 더 좁고 정의됩니다.    방향은 <b>장애 비등방성 각도</b> 매개 변수에 의해 제어됩니다. |
| <b>장애 비등방성 각도</b> <i>부동</i> | <b>장애 비등방성</b> 매개 변수가 0이 아닌 경우 <b>장애</b> 매개 변수에 의해 적용된 변위의 방향을 제어합니다. |
| <b>각도</b> <i>부동</i> | 스크래치 방향을 설정하는 데 사용되는 각도로, 회전 수와 수평 오른쪽부터 시작됩니다. |
| <b>각도 무작위</b> <i>부동</i> | <b>각도</b> 값에 적용되는 최대 무작위 변형 양(회전 수)입니다. |
| <b>패턴 양</b> <i>부동</i> | 흩어져 있는 스크래치 패턴 양에 대한 승수입니다. |
| <b>패턴 크기</b> <i>Float2</i> | 스크래치 패턴에 대한 테두리 상자의 크기입니다.    Y 값은 스크래치의 최대 길이를 제어합니다. |
| <b>패턴 크기 무작위</b> <i>Float2</i> | 스크래치에 적용되는 임의 다운스케일링 양에 대한 승수입니다.    Y 값은 해당 스크래치 길이에 적용됩니다. |
| <b>타일 오프셋</b> <i>Float2</i> | 노이즈를 렌더링하는 데 사용되는 무한 평면 부분의 위치를 제어합니다. |
| <b>정사각형이 아닌 확장</b> <i>부울</i> | 정사각형이 아닌 이미지에서 생성된 타일 사각형을 유지하고 노이즈 생성을 이미지 경계까지 확장합니다. |

## 예

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![방향 스크래치 - 예 1](directional-scratches.resources/directional-scratches-02.png "방향 스크래치 - 예 1"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![방향 스크래치 - 예 2](directional-scratches.resources/directional-scratches-03.gif "방향 스크래치 - 예 2"){zoomable="yes"}

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![방향 스크래치 - 예 3](directional-scratches.resources/directional-scratches-04.gif "방향 스크래치 - 예 3"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![방향 스크래치 - 예 4](directional-scratches.resources/directional-scratches-05.gif "방향 스크래치 - 예 4"){zoomable="yes"}

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![방향 스크래치 - 예 5](directional-scratches.resources/directional-scratches-06.gif "방향 스크래치 - 예 5"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">



</td>
</tr>
</table>
