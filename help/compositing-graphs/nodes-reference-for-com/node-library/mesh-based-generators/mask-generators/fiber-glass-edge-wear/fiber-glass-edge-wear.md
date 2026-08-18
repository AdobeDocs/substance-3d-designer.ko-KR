---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/mask-generators/fiber-glass-edge-wear.html"
breadcrumb-title: ''
description: 섬유 유리 Edge Wear 노드를 사용하여 메쉬 곡률을 기반으로 섬유 유리 가장자리에 마모 마스크를 생성합니다.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Mask Generators > Fiber Glass Edge Wear
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 섬유 유리 Edge Wear
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '288'
ht-degree: 1%

---


# 섬유 유리 Edge Wear

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/fiber-glass-edge-wear.png){width="128px"}

## 섬유 유리 Edge Wear

**내부:** *메시 기반 생성기**/마스크 생성기*

**중간**

</td>
<td style="border: 0;" valign="top">

## 설명

베이킹된 맵 및 사용자 설정을 기반으로 흑백 마스크를 생성합니다. [Painter](https://support.allegorithmic.com/documentation/display/SPDOC/Substance+Painter)의 [스마트 마스크](https://support.allegorithmic.com/documentation/display/SPDOC/Smart+Materials+and+Masks)와 비슷합니다.

섬유유리 유형의 착용을 위해 특별히 의도된 마스크를 나타내며, 아마도 천에 사용될 수 있다. 섬유의 매우 타일링되고, 반복적인 특성으로 인해, 삼평면 블렌딩이 임의로 인에이블될 수 있다.

## 매개변수

### 입력

* **곡률**: *회색 음영 입력*\
  가장자리 강조 표시에 사용되는 베이킹된 맵 필수!
* **주변 오클루전**: *회색 음영 입력*\
  베이킹된 맵은 가려진 영역을 마스크하는 데 사용됩니다. 필수는 아니지만 반드시 권장됩니다.
* **그런지 입력**: *회색 음영 입력*\
  파이버 패턴을 재정의하는 사용자 지정 슬롯(옵션).
* **마스크(선택 사항)**: *회색 음영 입력*\
  노드의 효과를 마스킹하는 데 사용되는 마스크 슬롯입니다.
* **월드 스페이스 표준**: *색상 입력*\
  Triplanar에만 사용됩니다.
* **위치**: *색상 입력*\
  Triplanar에만 사용됩니다.

### 매개변수

* **마모 수준**: *0.0 - 1.0*[막대 그래프 스캔](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/histogram-scan/histogram-scan.md)과 같이 점진적으로 마모가 드러납니다.
* **마모 대비**: *0.0 - 1.0*&#x200B;총 효과 대비를 설정합니다.
* **가장자리 Smoothness**: *0.0 - 16.0*&#x200B;강조 표시된 가장자리에서 도련/흐림 효과를 설정합니다.
* **그런지 양**: *0.0 - 1.0*&#x200B;가장자리 사이에서 혼합할 섬유 효과의 양을 설정합니다. 마모 수준과 함께 조정하여 최대한의 제어를 얻을 수 있습니다.
* **주변 오클루전 마스크**: *0.0 - 1.0* AO가 효과를 숨기는 데 미치는 영향의 양을 설정합니다.
* **곡률 두께**: *0.0 - 1.0*&#x200B;곡률에서 볼록 가장자리의 영향을 설정합니다.
* **사용자 지정 그런지 사용**: *False/True*&#x200B;기본 제공 섬유를 사용자 지정 맵으로 재정의합니다.
* **Triplanar 사용**: *False/True*&#x200B;은(는) [Tri Planar](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/mesh-based-generators/utilities-mesh-based-gen/tri-planar/tri-planar.md)을(를) 통해 이음새를 숨길 수 있도록 합니다.
* **삼각 혼합 대비**: *0.0 - 1.0*&#x200B;삼각 효과의 대비를 제어합니다.

## 예제 이미지

![](../../../../../../assets/fiber-glass-edge-wear-ex.gif)

</td>
</tr>
</table>
