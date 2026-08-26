---
helpx_url: "https://helpx.adobe.com/kr/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/noises/messy-fibers-1.html"
breadcrumb-title: ''
description: Dirty Fibers 1 노드를 사용하여 패브릭과 텍스타일 텍스처의 세부 사항을 만들기 위한 기본 섬유 패턴을 생성합니다.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Noises > Messy fibers 1
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 지저분한 섬유 1
user-guide-description: ''
user-guide-title: ''
source-git-commit: 3c2ada78db14be2b9c3380eff9b307aec11d40dc
workflow-type: tm+mt
source-wordcount: '326'
ht-degree: 1%

---


# 지저분한 섬유 1

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![너저분한 섬유 1 - 아이콘](../../../../../../assets/messy_fibers_1.png "너저분한 섬유 1 - 아이콘"){width="200px"}

<b>내부:</b> 텍스처 생성기 > 노이즈

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 설명

<b>너저분한 섬유</b> 구조적 노이즈의 변형.

참고 항목: [너저분한 섬유 2](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/messy-fibers-2/messy-fibers-2.md), [너저분한 섬유 3](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/messy-fibers-3/messy-fibers-3.md)

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
| <b>장애 비등방성 각도</b> 부동 | &#39;Disorder 비등방성&#39; 매개 변수가 0이 아닌 경우 <b>Disorder</b> 매개 변수에 의해 적용된 변위의 방향을 제어합니다. |
| <b>각도</b> 부동 | 스레드의 방향을 설정할 때 사용되는 각도로, 회전 수와 수평 오른쪽부터 설정합니다. |
| <b>각도 무작위</b> 부동 | <b>각도</b> 값에 적용되는 최대 무작위 변형 양(회전 수)입니다. |
| <b>줄 번호</b> 부동 | 기본 스레드에 적용되는 타일링의 양이며 이 값이 높을수록 스레드가 더 조밀하고 얇아집니다. |
| <b>타일 오프셋</b> Float2 | 노이즈를 렌더링하는 데 사용되는 무한 평면 부분의 위치를 제어합니다. |
| <b>정사각형이 아닌 확장</b> 부울 | 정사각형이 아닌 이미지에서 생성된 타일 사각형을 유지하고 노이즈 생성을 이미지 경계까지 확장합니다. |

## 예

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![너저분한 섬유 1 - 아이콘](../../../../../../assets/messy_fibers_1_1.png "너저분한 섬유 1 - 아이콘"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![지저분한 섬유 1 - 예 2](../../../../../../assets/noise_messy_fibers_1_v2_speed0.1_aniso0.gif "지저분한 섬유 1 - 예 2"){zoomable="yes"}

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![지저분한 섬유 1 - 예 3](../../../../../../assets/noise_messy_fibers_1_v2_speed0.1_aniso1.gif "지저분한 섬유 1 - 예 3"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![지저분한 섬유 1 - 예 4](../../../../../../assets/noise_messy_fibers_1_v2_speed0.1_aniso0.6.gif "지저분한 섬유 1 - 예 4"){zoomable="yes"}

</td>
</tr>
</table>
