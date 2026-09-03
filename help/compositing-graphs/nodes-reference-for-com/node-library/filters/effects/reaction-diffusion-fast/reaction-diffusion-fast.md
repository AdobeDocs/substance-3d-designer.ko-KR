---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/reaction-diffusion-fast.html"
breadcrumb-title: ''
description: 절차 텍스처에 대한 빠른 반응 확산 알고리즘을 사용하여 유기 패턴을 생성하려면 반응 확산 빠른 노드를 사용합니다.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Reaction Diffusion Fast
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 빠른 반응 확산
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '164'
ht-degree: 3%

---


# 빠른 반응 확산

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![반응 확산 노드 아이콘](reaction-diffusion-fast.resources/reaction-diffusion-fast-01.png "반응 확산 노드 아이콘")

<b>인:</b> 필터 > 효과

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 설명

이 노드는 입력 회색 음영 이미지에 반응-확산 효과를 수행합니다.

반응-확산은 물질이 퍼져(확산) 다른 물질과 상호 작용(반응)하는 과정이다. 예를 들어 동물의 피부에 특정 패턴이 형성되면 자연에서 일어나는 일을 시뮬레이션한 수학적 모델이다.

이 노드는 성능에 최적화되어 있고 속도를 위해 일부 정확성 절충을 합니다.

</td>
</tr>
</table>

<a name="inputs"></a>

## 입력

|  |  |
|:---|:---|
| <b>입력</b> <i>회색 음영</i> | [반응 확산] 효과를 적용해야 하는 회색 음영 이미지입니다. |

<a name="outputs"></a>

## 출력

|  |  |
|:---|:---|
| <b>출력</b> <i>회색 음영</i> | 입력 이미지에 적용된 반응-확산 효과를 나타내는 회색 음영 이미지 |

<a name="parameters"></a>

## 매개변수

|  |  |
|:---|:---|
| <b>반경</b> *부동* | 효과가 확산되는 거리입니다. |
| <b>대비</b> *부동* | 입력의 대비를 조정하며, 일종의 임계값 역할을 합니다. |

## 예

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![예 1](reaction-diffusion-fast.resources/reaction-diffusion-fast-02.png "예 1")

</td>
<td style="border: 0;" valign="top">

![예 2](reaction-diffusion-fast.resources/reaction-diffusion-fast-03.png "예 2")

</td>
<td style="border: 0;" valign="top">

![예 3](reaction-diffusion-fast.resources/reaction-diffusion-fast-04.gif "예 3")

</td>
</tr>
</table>
