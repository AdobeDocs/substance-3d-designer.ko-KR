---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/mask-generators/metal-edge-wear.html"
breadcrumb-title: ''
description: 금속 Edge Wear 노드를 사용하여 메쉬 곡률과 위치를 기반으로 금속 가장자리에 마모 마스크를 생성합니다.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Mask Generators > Metal Edge Wear
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 금속 Edge Wear
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '275'
ht-degree: 1%

---


# 금속 Edge Wear

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/metal-edge-wear.png){width="128px"}

## 금속 Edge Wear

**내부:** *메시 기반 생성기**/마스크 생성기*

**복합**

</td>
<td style="border: 0;" valign="top">

## 설명

베이킹된 맵 및 사용자 설정을 기반으로 흑백 마스크를 생성합니다. [Painter](https://support.allegorithmic.com/documentation/display/SPDOC/Substance+Painter)의 [스마트 마스크](https://support.allegorithmic.com/documentation/display/SPDOC/Smart+Materials+and+Masks)와 비슷합니다.

이 마스크는 금속 오브젝트의 가장자리 마모를 나타내며, 가장자리가 볼록하게 솟아오른 곳에 스크래치와 칩이 표시되어 구운 AO 어두운 영역으로 마스크될 수 있습니다.

## 매개변수

### 입력

* **곡률**: *회색 음영 입력*\
  내부 효과 및 마스크에 사용되는 베이킹된 맵.
* **주변 오클루전**: *회색 음영 입력*\
  내부 효과 및 마스크에 사용되는 베이킹된 맵.
* **그런지 입력**: *회색 음영 입력*
* **마스크(선택 사항)**: *회색 음영 입력*\
  노드의 효과를 마스킹하는 데 사용되는 마스크 슬롯입니다.
* **월드 스페이스 표준**: *색상 입력*
* **위치**: *색상 입력*

### 매개변수

* **마모 수준**: *0.0 - 1.0*&#x200B;마모의 총 양을 설정하고 점차적으로 드러냅니다.
* **마모 대비**: *0.0 - 1.0*&#x200B;최종 결과의 대비를 설정합니다.
* **가장자리 Smoothness**: *0.0 - 16.0*&#x200B;곡률의 가장자리에서 밝기 감소 Smoothness을 설정합니다.
* **그런지 양**: *0.0 - 1.0*&#x200B;가장자리 사이에서 혼합할 그런지 양을 설정합니다.
* **그런지 크기**: *1 - 16*&#x200B;그런지 크기를 설정합니다.
* **주변 오클루전 마스크**: *0.0 - 1.0* AO가 마스킹되는 어두운 영역에서 최종 효과에 미치는 영향의 양을 설정합니다.
* **곡률 두께**: *0.0 - 1.0*&#x200B;곡률에서 볼록한 가장자리가 최종 효과에 미치는 영향의 양을 설정합니다.
* **사용자 지정 그런지 사용**: *False/True*&#x200B;사용자 지정 그런지 맵 입력 슬롯을 사용합니다.
* **Triplanar 사용**: *False/True*&#x200B;이음새를 숨기려면 [Tri Planar](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/mesh-based-generators/utilities-mesh-based-gen/tri-planar/tri-planar.md) 프로젝션을 사용하도록 설정합니다.
* **삼각 평면 혼합 대비**: *0.0 - 1.0*&#x200B;삼각 평면 투영에 대한 혼합 대비를 설정합니다.

## 예제 이미지

![](../../../../../../assets/metal-edge-wear-ex.gif)

</td>
</tr>
</table>
