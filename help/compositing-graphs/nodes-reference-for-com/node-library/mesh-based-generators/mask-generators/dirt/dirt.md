---
helpx_url: "https://helpx.adobe.com/kr/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/mask-generators/dirt.html"
breadcrumb-title: ''
description: Dirt 노드를 사용하여 메쉬 곡률, 위치, 오클루전을 기반으로 Dirt 누적 마스크를 생성합니다.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Mask Generators > Dirt
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 흙
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '248'
ht-degree: 2%

---


# 흙

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/dirt.png){width="128px"}

## 흙

**내부:** *메시 기반 생성기**/마스크 생성기*

**중간**

</td>
<td style="border: 0;" valign="top">

## 설명

베이킹된 맵 및 사용자 설정을 기반으로 흑백 마스크를 생성합니다. [Painter](https://support.allegorithmic.com/documentation/display/SPDOC/Substance+Painter)의 [스마트 마스크](https://support.allegorithmic.com/documentation/display/SPDOC/Smart+Materials+and+Masks)와 비슷합니다.

이 마스크는 적용된 AO 및 곡률을 기반으로, 오목하고 함몰된 가장자리 및 모퉁이의 Dirt을 나타냅니다.

## 매개변수

### 입력

* **곡률**: *회색 음영 입력*\
  내부 효과 및 마스크에 사용되는 베이킹된 맵. 필수!
* **주변 오클루전**: *회색 음영 입력*\
  내부 효과 및 마스크에 사용되는 베이킹된 맵. 필수!
* **그런지 입력**: *회색 음영 입력*\
  사용자 정의 그런지 맵 입력(선택 사항), 매개 변수에 의해 활성화됨
* **마스크(선택 사항)**: *회색 음영 입력*\
  노드의 효과를 마스킹하는 데 사용되는 마스크 슬롯입니다.
* **월드 스페이스 표준**: *색상 입력*\
  Triplanar에만 사용됩니다.
* **위치**: *색상 입력*\
  Triplanar에만 사용됩니다.

### 매개변수

* **Dirt 수준**: *0.0 - 1.0* Dirt 양에 대한 기본 제어.
* **Dirt 대비**: *0.0 - 1.0*&#x200B;마스크에 있는 Dirt의 기본 대비를 제어합니다.
* **그런지 양**: *0.0 - 1.0* Dirt이 얼마나 거칠은지 설정합니다. 완벽한 Dirt을 위해 0으로 설정합니다.
* **가장자리 마스크**: *0.0 - 1.0*&#x200B;높아진 가장자리에서 제거할 Dirt의 양(곡률 맵에 따라 다름)입니다.
* **사용자 지정 그런지 사용**: *False/True*&#x200B;기본 제공 그런지 대신 사용자 지정 그런지 맵 입력을 사용하도록 설정합니다.
* **그런지 크기**: *1 - 16*&#x200B;그런지 세부 사항의 타일링 크기를 설정합니다.
* **Triplanar 사용**: *False/True*&#x200B;그런지 매핑에 [Triplanar 투영](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/mesh-based-generators/utilities-mesh-based-gen/tri-planar/tri-planar.md)을 사용하고 이음새를 제거합니다.
* **삼각 혼합 대비**: *0.001 - 1.0*&#x200B;삼각 투영의 대비를 설정합니다.

## 예제 이미지

![](../../../../../../assets/dirt-ex.gif)

</td>
</tr>
</table>
