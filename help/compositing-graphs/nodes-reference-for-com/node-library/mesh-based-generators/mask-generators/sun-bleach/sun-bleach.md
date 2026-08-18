---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/mask-generators/sun-bleach.html"
breadcrumb-title: ''
description: 태양 표백 노드를 사용하면 햇빛 노출을 기반으로 마스크를 생성하여 사실적인 태양 표백 및 빛바랜 효과를 만들 수 있습니다.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Mask Generators > Sun Bleach
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 선 블리치
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '164'
ht-degree: 1%

---


# 선 블리치

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/sun-bleach.png){width="128px"}

## 선 블리치

**내부:** *메시 기반 생성기**/마스크 생성기*

**단순**

</td>
<td style="border: 0;" valign="top">

## 설명

베이킹된 맵 및 사용자 설정을 기반으로 흑백 마스크를 생성합니다. [Painter](https://support.allegorithmic.com/documentation/display/SPDOC/Substance+Painter)의 [스마트 마스크](https://support.allegorithmic.com/documentation/display/SPDOC/Smart+Materials+and+Masks)와 비슷합니다.

이 마스크는 [빛](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/mesh-based-generators/mask-generators/light/light.md)과 비슷하지만 AO를 지원합니다. 이를 통해 효과 상단에 빛 표백 및 페이드를 나타내는 마스크가 만들어집니다.

## 입력

* **일반 월드 공간**: *색상 입력*
* **주변 오클루전**: *회색 음영 입력*\
  내부 효과 및 마스크에 사용되는 베이킹된 맵.
* **마스크(선택 사항)**: *회색 음영 입력*\
  노드의 효과를 마스킹하는 데 사용되는 마스크 슬롯입니다.

## 매개변수

* **수준**: *0.0 - 1.0*\
  전체 표백 양을 설정하고 효과를 아래로 이동합니다.
* **대비**: *0.0 - 1.0*\
  결과의 대비를 조정합니다.
* **오클루전**: *0.0 - 1.0*&#x200B;최종 결과에 대한 AO의 영향을 설정합니다.

## 예제 이미지

![](../../../../../../assets/sun-bleach-ex.gif)

</td>
</tr>
</table>
