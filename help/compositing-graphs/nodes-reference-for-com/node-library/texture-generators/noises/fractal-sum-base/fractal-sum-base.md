---
helpx_url: "https://helpx.adobe.com/kr/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/noises/fractal-sum-base.html"
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
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '259'
ht-degree: 1%

---


# 프랙탈 합산 기반

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![프랙탈 합산 기반 - 아이콘](fractal-sum-base.resources/fractal-sum-base-01.png "프랙탈 합산 기반 - 아이콘"){width="200px"}

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

<a name="outputs"></a>

## 출력

|  |  |
|:---|:---|
| <b>출력</b> <i>회색 음영</i> | 회색 음영 비트맵으로 생성된 노이즈 |

<a name="parameters"></a>

## 매개변수

|  |  |
|:---|:---|
| <b>거칠음</b> <i>부동</i> | 노이즈 옥타브의 균형입니다.    이 값을 높이면 빈도수가 높은 옥타브가 더 많이 표시됩니다. |
| <b>분. 수준</b> <i>정수</i> | 노이즈에 사용되는 최소 옥타브입니다.    값이 높을수록 노이즈 주파수가 높아집니다. |
| <b>최대. 수준</b> <i>정수</i> | 노이즈에 사용되는 최대 옥타브입니다.    값이 높을수록 노이즈 주파수가 높아집니다. |
| <b>장애</b> <i>부동</i> | 소음의 성분을 제거합니다.    이 효과를 사용하면 노이즈에 애니메이션을 적용할 수 있습니다. |
| <b>장애 속도</b> <i>부동</i> | <b>Disorder</b> 매개 변수에 의해 적용된 변위의 거리를 조정합니다.    이 효과는 노이즈에 애니메이션을 적용할 때 변위 속도를 제어하는 데 사용할 수 있습니다. |
| <b>대비</b> <i>부동</i> | 최종 결과의 대비입니다. |
| <b>전역 불투명도</b> <i>부동</i> | 노이즈 옥타브의 불투명도가 최종 결과에 함께 추가되었습니다.    값이 높으면 영역이 흰색으로 탈 수 있습니다. |
| <b>정사각형이 아닌 확장</b> <i>부울</i> | 정사각형이 아닌 이미지에서 생성된 타일 사각형을 유지하고 노이즈 생성을 이미지 경계까지 확장합니다. |

## 예

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![프랙탈 합산 기반 - 예 1](fractal-sum-base.resources/fractal-sum-base-02.png "프랙탈 합산 기반 - 예 1"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![프랙탈 합산 기반 - 예 2](fractal-sum-base.resources/fractal-sum-base-03.gif "프랙탈 합산 기반 - 예 2"){zoomable="yes"}

</td>
</tr>
</table>
