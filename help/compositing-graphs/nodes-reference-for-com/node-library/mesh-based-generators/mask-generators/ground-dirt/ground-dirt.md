---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/mask-generators/ground-dirt.html"
breadcrumb-title: ''
description: 지표 Dirt 노드를 사용하여 지면에 대한 메시 위치와 방향을 기준으로 Dirt 누적 마스크를 생성합니다.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Mask Generators > Ground Dirt
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 바닥 Dirt
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '153'
ht-degree: 1%

---


# 바닥 Dirt

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/ground-dirt.png){width="128px"}

## 바닥 Dirt

**내부:** *메시 기반 생성기**/마스크 생성기*

**단순**

</td>
<td style="border: 0;" valign="top">

## 설명

베이킹된 맵 및 사용자 설정을 기반으로 흑백 마스크를 생성합니다. [Painter](https://support.allegorithmic.com/documentation/display/SPDOC/Substance+Painter)의 [스마트 마스크](https://support.allegorithmic.com/documentation/display/SPDOC/Smart+Materials+and+Masks)와 비슷합니다.

이 마스크는 [아래에서 위로](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/mesh-based-generators/mask-generators/bottom-to-top/bottom-to-top.md) 또는 [Dust](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/mesh-based-generators/mask-generators/dust/dust.md)의 반대인 처음부터 위쪽으로 누적된 Dirt을 나타냅니다. 사용자 정의 맵 재정의가 없습니다.

## 입력

* **위치**: *회색 음영 입력*\
  기준점에 위치 매핑 적용 필수!
* **마스크(선택 사항)**: *회색 음영 입력*\
  노드의 효과를 마스킹하는 데 사용되는 마스크 슬롯입니다.

## 매개변수

* **수준**: *0.0 - 1.0*\
  Dirt의 전체 모양 레벨을 설정합니다.
* **대비**: *0.0 - 1.0*\
  결과의 대비를 조정합니다.
* **Dirt Height**: *0.0 - 1.0* Dirt이 표시할 Height(비례적으로)를 설정합니다.

## 예제 이미지

![](../../../../../../assets/ground-dirt-ex.gif)

</td>
</tr>
</table>
