---
helpx_url: "https://helpx.adobe.com/kr/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/mask-generators/edge-speckle.html"
breadcrumb-title: ''
description: 가장자리 반점 노드를 사용하여 메시 가장자리에 반점 마모 패턴을 생성하여 사실적인 가장자리 손상 효과를 생성합니다.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Mask Generators > Edge Speckle
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 가장자리 반점
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '183'
ht-degree: 2%

---


# 가장자리 반점

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/edge-speckle.png){width="128px"}

## 가장자리 반점

**내부:** *메시 기반 생성기**/마스크 생성기*

**중간**

</td>
<td style="border: 0;" valign="top">

## 설명

베이킹된 맵 및 사용자 설정을 기반으로 흑백 마스크를 생성합니다. [Painter](https://support.allegorithmic.com/documentation/display/SPDOC/Substance+Painter)의 [스마트 마스크](https://support.allegorithmic.com/documentation/display/SPDOC/Smart+Materials+and+Masks)와 비슷합니다.

이 마스크는 가장자리를 나타내는 약간의 스펙클을 추가해 분리합니다. [Edge Dirt](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/mesh-based-generators/mask-generators/edge-dirt/edge-dirt.md)도 참조하십시오.

## 매개변수

### 입력

* **곡률**: *회색 음영 입력*\
  가장자리 강조 표시에 사용되는 베이킹된 맵. 필수!
* **변형 마스크**: *회색 음영 입력*\
  노드의 효과를 마스킹하는 데 사용되는 선택적 마스크 슬롯입니다. &quot;변형 마스크 재정의&quot;를 사용하여 활성화합니다.
* **마스크(선택 사항)**: *회색 음영 입력*\
  노드의 효과를 마스킹하는 데 사용되는 마스크 슬롯입니다.

### 매개변수

* **수준**: *0.0 - 1.0*\
  가장자리 강조 표시의 총 양을 설정합니다.
* **대비**: *0.0 - 1.0*\
  결과의 대비를 조정합니다.
* **가장자리 선택**: *0.0 - 1.0*&#x200B;볼록한 가장자리의 영향을 설정합니다.
* **변형**: *0.0 - 1.0*&#x200B;변형 마스크가 효과를 중단하는 정도를 설정합니다.
* **변형 마스크 재정의**: *False/True*&#x200B;기본 제공 마스크를 사용자 지정 입력 슬롯으로 재정의합니다.

## 예제 이미지

![](../../../../../../assets/edge-speckle-ex.gif)

</td>
</tr>
</table>
