---
helpx_url: "https://helpx.adobe.com/kr/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/noises/directional-scratches.html"
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
source-git-commit: ea96f5a148246d20263c4ecf0b67d0b4a51f28a8
workflow-type: tm+mt
source-wordcount: '363'
ht-degree: 1%

---


# 직접 스크래치

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![방향 스크래치 - 아이콘](../../../../../../assets/directional_scratches.png "방향 스크래치 - 아이콘"){width="200px"}

<b>내부:</b> 텍스처 생성기 > 노이즈

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 설명

각도 및 크기를 조정할 수 있는 스크래치 패턴의 임의 분산.

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

### 출력

</td>
<td style="border: 0;" valign="top">

### 매개변수

</td>
<td style="border: 0;" valign="top">

### 예

</td>
</tr>
</table>

## 출력

|  |  |
| --- | --- |
| <b>출력</b> *회색 음영* | 회색 음영 비트맵으로 생성된 노이즈 |

## 매개변수

|  |  |
| --- | --- |
| <b>비율</b> 정수 | 노이즈 타일을 생성하는 데 사용되는 격자의 하위 분할입니다.    값이 높을수록 더 많은 타일이 그려지고 노이즈가 더 많아집니다. |
| <b>장애</b> 부동 | 소음의 성분을 제거합니다.    이 효과를 사용하면 노이즈에 애니메이션을 적용할 수 있습니다. |
| <b>장애 속도</b> 부동 | <b>Disorder</b> 매개 변수에 의해 적용된 변위의 거리를 조정합니다.    이 효과는 노이즈에 애니메이션을 적용할 때 변위 속도를 제어하는 데 사용할 수 있습니다. |
| <b>장애 비등방성</b> 부동 | <b>Disorder</b> 매개 변수에 의해 적용된 변위의 방향 범위를 제어합니다. 값이 높을수록 방향이 더 좁고 정의됩니다.    방향은 <b>장애 비등방성 각도</b> 매개 변수에 의해 제어됩니다. |
| <b>장애 비등방성 각도</b> 부동 | <b>장애 비등방성</b> 매개 변수가 0이 아닌 경우 <b>장애</b> 매개 변수에 의해 적용된 변위의 방향을 제어합니다. |
| <b>각도</b> 부동 | 스크래치 방향을 설정하는 데 사용되는 각도로, 회전 수와 수평 오른쪽부터 시작됩니다. |
| <b>각도 무작위</b> 부동 | <b>각도</b> 값에 적용되는 최대 무작위 변형 양(회전 수)입니다. |
| <b>패턴 양</b> 부동 | 흩어져 있는 스크래치 패턴 양에 대한 승수입니다. |
| <b>패턴 크기</b> 부동 소수점2 | 스크래치 패턴에 대한 테두리 상자의 크기입니다.    Y 값은 스크래치의 최대 길이를 제어합니다. |
| <b>패턴 크기 무작위</b> Float2 | 스크래치에 적용되는 임의 다운스케일링 양에 대한 승수입니다.    Y 값은 해당 스크래치 길이에 적용됩니다. |
| <b>타일 오프셋</b> Float2 | 노이즈를 렌더링하는 데 사용되는 무한 평면 부분의 위치를 제어합니다. |
| <b>정사각형이 아닌 확장</b> 부울 | 정사각형이 아닌 이미지에서 생성된 타일 사각형을 유지하고 노이즈 생성을 이미지 경계까지 확장합니다. |

## 예

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![방향 스크래치 - 예 1](../../../../../../assets/directional_scratches_1.png "방향 스크래치 - 예 1"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![방향 스크래치 - 예 2](../../../../../../assets/noise-directional-scratches-speed0.3-aniso0.gif "방향 스크래치 - 예 2"){zoomable="yes"}

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![방향 스크래치 - 예 3](../../../../../../assets/noise-directional-scratches-speed0.3-aniso0.6.gif "방향 스크래치 - 예 3"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![방향 스크래치 - 예 4](../../../../../../assets/noise-directional-scrat-1.gif "방향 스크래치 - 예 4"){zoomable="yes"}

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![방향 스크래치 - 예 5](../../../../../../assets/noise-directional-scrat-2.gif "방향 스크래치 - 예 5"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">



</td>
</tr>
</table>

</td>
<td style="border: 0;" valign="top">



</td>
<td style="border: 0;" valign="top">



</td>
</tr>
</table>
