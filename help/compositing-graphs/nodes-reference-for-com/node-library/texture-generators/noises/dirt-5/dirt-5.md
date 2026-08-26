---
helpx_url: "https://helpx.adobe.com/kr/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/noises/dirt-5.html"
breadcrumb-title: ''
description: Dirt 5 노드를 사용하여 풍화 및 오래된 표면 세부 사항을 만들기 위한 고급 Dirt 패턴을 생성합니다.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Noises > Dirt 5
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: DIRT 5
user-guide-description: ''
user-guide-title: ''
source-git-commit: 3c2ada78db14be2b9c3380eff9b307aec11d40dc
workflow-type: tm+mt
source-wordcount: '258'
ht-degree: 1%

---


# DIRT 5

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Dirt 5 - 아이콘](../../../../../../assets/dirt_5.png "Dirt 5 - 아이콘"){width="200px"}

<b>내부:</b> 텍스처 생성기 > 노이즈

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 설명

거친 <b>Dirt</b> 노이즈의 변형.

참고 항목: [Dirt 1](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/dirt-1/dirt-1.md), [Dirt 2](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/dirt-2/dirt-2.md), [Dirt 3](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/dirt-3/dirt-3.md), [Dirt 4](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/dirt-4/dirt-4.md), [Dirt 그레이디언트](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/dirt-gradient/dirt-gradient.md)

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
| <b>타일 오프셋</b> Float2 | 노이즈를 렌더링하는 데 사용되는 무한 평면 부분의 위치를 제어합니다. |
| <b>정사각형이 아닌 확장</b> 부울 | 정사각형이 아닌 이미지에서 생성된 타일 사각형을 유지하고 노이즈 생성을 이미지 경계까지 확장합니다. |

## 예

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Dirt 5 - 예 1](../../../../../../assets/dirt_5_1.png "Dirt 5 - 예 1"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![Dirt 5 - 예 2](../../../../../../assets/noise_dirt_5_v2_speed0.6_aniso0.gif "Dirt 5 - 예 2"){zoomable="yes"}

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Dirt 5 - 예 3](../../../../../../assets/noise_dirt_5_v2_speed0.6_aniso1.gif "Dirt 5 - 예 3"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![Dirt 5 - 예 4](../../../../../../assets/noise_dirt_5_v2_speed0.3_aniso0.6.gif "Dirt 5 - 예 4"){zoomable="yes"}

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
