---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/noises/perlin-noise.html"
breadcrumb-title: ''
description: Perlin Noise 노드를 사용하면 유기적인 질감과 변형을 생성하기 위해 매끄럽고 자연스러워 보이는 노이즈 패턴을 생성할 수 있습니다.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Noises > Perlin noise
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 펄린 노이즈
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '178'
ht-degree: 2%

---


# 펄린 노이즈

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![펄린 노이즈 - 아이콘](perlin-noise.resources/perlin_noise.png "펄린 노이즈 - 아이콘"){width="200px"}

<b>내부:</b> 텍스처 생성기 > 노이즈

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 설명

일반적으로 사용되는 회색 음영 값의 매끄러운 분포인 Perlin 노이즈를 생성합니다.

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
| <b>타일 오프셋</b> <i>Float2</i> | 노이즈를 렌더링하는 데 사용되는 무한 평면 부분의 위치를 제어합니다. |
| <b>정사각형이 아닌 확장</b> <i>부울</i> | 정사각형이 아닌 이미지에서 생성된 타일 사각형을 유지하고 노이즈 생성을 이미지 경계까지 확장합니다. |

## 예

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![펄린 노이즈 - 예 1](perlin-noise.resources/perlin_noise_1.png "펄린 노이즈 - 예 1"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![펄린 노이즈 - 예 2](perlin-noise.resources/noise_perlin_noise_v2_speed0.6_aniso0.gif "펄린 노이즈 - 예 2"){zoomable="yes"}

</td>
</tr>
</table>
