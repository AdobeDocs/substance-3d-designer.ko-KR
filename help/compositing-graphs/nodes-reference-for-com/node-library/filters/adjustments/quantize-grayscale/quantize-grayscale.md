---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/adjustments/quantize-grayscale.html"
breadcrumb-title: ''
description: '[회색 음영 분석] 노드를 사용하여 포스터화 효과의 회색 음영 레벨 수를 줄입니다.'
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Adjustments > Quantize Grayscale
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 회색 음영 정량화
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '158'
ht-degree: 1%

---


# 회색 음영 정량화

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![회색 음영 아이콘 정량화](../../../../../../assets/quantize-grayscale.png "회색 음영 아이콘 정량화"){width="200px"}

<b>내부:</b> 필터 > 조정

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 설명

원 모양으로 단일 스플라인을 생성합니다.

</td>
</tr>
</table>

## 매개변수

<b>단계</b> *정수*&#x200B;입력 범위를 근사해야 하는 별도의 값 수입니다.

<b>오프셋</b> *부동*&#x200B;입력 범위에 오프셋을 적용하여 범위에 따라 결과를 *이동*&#x200B;합니다.

<b>경사</b> *부동*&#x200B;대략적인 값 사이의 *전환*&#x200B;에 경사 그레이디언트를 *단계의 전체 범위*&#x200B;까지 적용합니다.

<b>경사 곡선</b> *정수*<b>경사</b> 매개 변수에 의해 설정된 경사에 대한 곡선을 얻는 방법을 설정합니다.
* *선형*: 선형 곡선을 적용하여 직선 경사를 만듭니다.
* *매끄러운 단계*: 매끄러운 단계 곡선을 적용하여 매끄러운 경사를 만듭니다.
* *곡선 입력*: <b>곡선 입력</b> 입력 맵에서 설명하는 곡선을 적용합니다. [곡선](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/curve/curve.md) 노드를 사용하여 많은 양의 제어로 이 곡선을 설명할 수 있습니다.

## 예

![예 1](../../../../../../assets/quantizegrayscale.gif "예 1")

![예 2](../../../../../../assets/quantizegrayscale.png "예 2")
