---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/noises/fractal-sum-base.html"
breadcrumb-title: ''
description: '[프랙탈 합산 기본] 노드를 사용하여 복잡한 유기 텍스처를 만들기 위한 기본 프랙탈 노이즈 패턴을 생성합니다.'
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Noises > Fractal sum base
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 프랙탈 합산 기반
user-guide-description: ''
user-guide-title: ''
source-git-commit: ea96f5a148246d20263c4ecf0b67d0b4a51f28a8
workflow-type: tm+mt
source-wordcount: '262'
ht-degree: 2%

---


# 프랙탈 합산 기반

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![프랙탈 합산 기반 - 아이콘](../../../../../../assets/fractal_sum_base.png "프랙탈 합산 기반 - 아이콘"){width="200px"}

<b>내부:</b> 텍스처 생성기 > 노이즈

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 설명

옥타브의 범위와 균형을 조정할 수 있는 사용자 정의 가능한 프랙탈 노이즈입니다.

<b>프랙탈 합산</b> 잡음 계열은 모두 이 노드를 기반으로 합니다.

참고 항목: [프랙탈 합산 1](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/fractal-sum-1/fractal-sum-1.md), [프랙탈 합산 2](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/fractal-sum-2/fractal-sum-2.md), [프랙탈 합산 3](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/fractal-sum-3/fractal-sum-3.md), [프랙탈 합산 4](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/fractal-sum-4/fractal-sum-4.md)

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
| <b>거칠음</b> 부동 | 노이즈 옥타브의 균형입니다.    이 값을 높이면 빈도수가 높은 옥타브가 더 많이 표시됩니다. |
| <b>분. 레벨</b> 정수 | 노이즈에 사용되는 최소 옥타브입니다.    값이 높을수록 노이즈 주파수가 높아집니다. |
| <b>최대. 레벨</b> 정수 | 노이즈에 사용되는 최대 옥타브입니다.    값이 높을수록 노이즈 주파수가 높아집니다. |
| <b>장애</b> 부동 | 소음의 성분을 제거합니다.    이 효과를 사용하면 노이즈에 애니메이션을 적용할 수 있습니다. |
| <b>장애 속도</b> 부동 | <b>Disorder</b> 매개 변수에 의해 적용된 변위의 거리를 조정합니다.    이 효과는 노이즈에 애니메이션을 적용할 때 변위 속도를 제어하는 데 사용할 수 있습니다. |
| <b>대비</b> 부동 | 최종 결과의 대비입니다. |
| <b>전역 불투명도</b> 부동 | 노이즈 옥타브의 불투명도가 최종 결과에 함께 추가되었습니다.    값이 높으면 영역이 흰색으로 탈 수 있습니다. |
| <b>정사각형이 아닌 확장</b> 부울 | 정사각형이 아닌 이미지에서 생성된 타일 사각형을 유지하고 노이즈 생성을 이미지 경계까지 확장합니다. |

## 예

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![프랙탈 합산 기반 - 예 1](../../../../../../assets/fractal_sum_base_1.png "프랙탈 합산 기반 - 예 1"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![프랙탈 합산 기반 - 예 2](../../../../../../assets/noise_fractal_sum_base_v2_speed0.6_aniso0.gif "프랙탈 합산 기반 - 예 2"){zoomable="yes"}

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
