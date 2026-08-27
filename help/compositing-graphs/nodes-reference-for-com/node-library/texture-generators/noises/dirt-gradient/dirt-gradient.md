---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/noises/dirt-gradient.html"
breadcrumb-title: ''
description: Dirt 그레이디언트 노드를 사용하여 방향성 풍화 및 누적 효과를 만드는 그레이디언트 기반 Dirt 패턴을 생성합니다.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Noises > Dirt gradient
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Dirt 그라디언트
user-guide-description: ''
user-guide-title: ''
source-git-commit: 3c2ada78db14be2b9c3380eff9b307aec11d40dc
workflow-type: tm+mt
source-wordcount: '221'
ht-degree: 1%

---


# Dirt 그라디언트

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Dirt 그레이디언트 - 아이콘](../../../../../../assets/dirt_gradient.png "Dirt 그레이디언트 - 아이콘"){width="200px"}

<b>내부:</b> 텍스처 생성기 > 노이즈

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 설명

방향성 밝기 감소 그레이디언트를 특징으로 하는 거친 <b>Dirt</b> 노이즈의 변형.

참고 항목: [Dirt 1](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/dirt-1/dirt-1.md), [Dirt 2](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/dirt-2/dirt-2.md), [Dirt 3](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/dirt-3/dirt-3.md), [Dirt 4](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/dirt-4/dirt-4.md), [Dirt 5](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/dirt-5/dirt-5.md)

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
| <b>장애</b> 부동 | 소음의 성분을 제거합니다.    이 효과를 사용하면 노이즈에 애니메이션을 적용할 수 있습니다. |
| <b>장애 속도</b> 부동 | <b>Disorder</b> 매개 변수에 의해 적용된 변위의 거리를 조정합니다.    이 효과는 노이즈에 애니메이션을 적용할 때 변위 속도를 제어하는 데 사용할 수 있습니다. |
| <b>장애 비등방성</b> 부동 | <b>Disorder</b> 매개 변수에 의해 적용된 변위의 방향 범위를 제어합니다. 값이 높을수록 방향이 더 좁고 정의됩니다.    방향은 <b>장애 비등방성 각도</b> 매개 변수에 의해 제어됩니다. |
| <b>장애 비등방성 각도</b> 부동 | <b>장애 비등방성</b> 매개 변수가 0이 아닌 경우 <b>장애</b> 매개 변수에 의해 적용된 변위의 방향을 제어합니다. |
| <b>정사각형이 아닌 확장</b> 부울 | 정사각형이 아닌 이미지에서 생성된 타일 사각형을 유지하고 노이즈 생성을 이미지 경계까지 확장합니다. |

## 예

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Dirt 그레이디언트 - 예 1](../../../../../../assets/dirt_gradient_1.png "Dirt 그레이디언트 - 예 1"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![Dirt 그레이디언트 - 예 2](../../../../../../assets/noise_dirt_gradient_v2_speed0.6_aniso0.gif "Dirt 그레이디언트 - 예 2"){zoomable="yes"}

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Dirt 그레이디언트 - 예 3](../../../../../../assets/noise_dirt_gradient_v2_speed0.6_aniso1.gif "Dirt 그레이디언트 - 예 3"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![Dirt 그레이디언트 - 예 4](../../../../../../assets/noise_dirt_gradient_v2_speed0.3_aniso0.6.gif "Dirt 그레이디언트 - 예 4"){zoomable="yes"}

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
