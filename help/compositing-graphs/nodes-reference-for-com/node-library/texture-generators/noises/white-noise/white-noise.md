---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/noises/white-noise.html"
breadcrumb-title: ''
description: '[흰색 노이즈] 노드를 사용하면 텍스처 변형과 임의 효과를 만들기 위한 흰색 노이즈 패턴을 생성할 수 있습니다.'
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Noises > White noise
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 흰색 노이즈
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '151'
ht-degree: 5%

---


# 흰색 노이즈

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![흰색 노이즈 - 아이콘](white-noise.resources/white-noise-01.png "흰색 노이즈 - 아이콘"){width="200px"}

<b>내부:</b> 텍스처 생성기 > 노이즈

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 설명

다양한 히스토그램 모양을 대상으로 하는 세 가지 방법(균일, 가우시안, 삼각형) 중 하나를 사용하여 흰색 노이즈를 생성합니다.

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
| <b>노이즈 분포</b> <i>정수</i> | 막대 그래프 모양을 대상으로 하기 위해 재료를 배포하는 방법:<ul data-preserve-html="true"> <li data-preserve-html="true"><i>균일:</i> 플랫 히스토그램입니다.</li> <li data-preserve-html="true"><i>가우시안:</i> 벨 곡선과 유사한 정규 분포를 나타내는 막대 그래프입니다.</li> <li data-preserve-html="true"><i>삼각형:</i> 삼각형 히스토그램입니다.</li> </ul> |
| <b>장애</b> <i>부동</i> | 소음의 성분을 제거합니다.    이 효과를 사용하면 노이즈에 애니메이션을 적용할 수 있습니다. |
| <b>장애 속도</b> <i>부동</i> | <b>Disorder</b> 매개 변수에 의해 적용된 변위의 거리를 조정합니다.    이 효과는 노이즈에 애니메이션을 적용할 때 변위 속도를 제어하는 데 사용할 수 있습니다. |

## 예

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![흰색 노이즈 - 예 1](white-noise.resources/white-noise-02.png "흰색 노이즈 - 예 1"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![백색 잡음 - 예 2](white-noise.resources/white-noise-03.gif "백색 잡음 - 예 2"){zoomable="yes"}

</td>
</tr>
</table>
