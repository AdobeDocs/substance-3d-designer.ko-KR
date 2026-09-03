---
helpx_url: "https://helpx.adobe.com/kr/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/patterns/gradient-radial.html"
breadcrumb-title: ''
description: 그레이디언트 방사형 노드를 사용하여 원형 색상 전환을 위해 중심점에서 방사되는 방사형 그레이디언트를 만듭니다.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Patterns > Gradient Radial
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 방사형 그레이디언트
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '121'
ht-degree: 1%

---


# 방사형 그레이디언트

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](gradient-radial.resources/gradient-radial-01.png){width="128px"}

<b>내부:</b> 텍스처 생성기 > 패턴

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 설명

[원형 그레이디언트](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/gradient-circular/gradient-circular.md)와 비슷하게 방사형 방식으로 두 개의 사용자 정의 점으로 정의된 회색 음영 그레이디언트 전환을 만듭니다. 중심점과 반경으로 정의되는 a에서 b로의 변환입니다. 결과가 항상 바둑판식으로 나타나는 것은 아닙니다.

</td>
</tr>
</table>

<a name="parameters"></a>

## 매개변수

|  |  |
|:---|:---|
| <b>모양</b> <i>원뿔, 반구</i> | 전환 프로필을 결정합니다. Cone은 선명한 선형 전환이며, Hemisphere는 부드럽고 중앙이 둥글습니다. |
| <b>지점 1</b> | 그레이디언트의 중심점입니다. 흰색으로 시작합니다. |
| <b>지점 2</b> | 반경 포인트를 사용하여 그레이디언트의 범위를 결정합니다. 끝 검정. |
| <b>비정사각형 확장</b> <i>거짓/참</i> | 제곱이 아닌 비율로 스쿼시와 스트레치를 보정합니다. |
