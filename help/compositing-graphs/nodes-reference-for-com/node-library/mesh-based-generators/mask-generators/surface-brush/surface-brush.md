---
helpx_url: "https://helpx.adobe.com/kr/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/mask-generators/surface-brush.html"
breadcrumb-title: ''
description: '[표면 브러시] 노드를 사용하면 표면 방향을 기반으로 방향 풍화 및 마모 효과를 만들기 위한 마스크를 생성할 수 있습니다.'
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Mask Generators > Surface Brush
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 표면 브러시
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '224'
ht-degree: 1%

---


# 표면 브러시

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/surface-brush.png){width="128px"}

## 표면 브러시

**내부:** *메시 기반 생성기**/마스크 생성기*

**중간**

</td>
<td style="border: 0;" valign="top">

## 설명

베이킹된 맵 및 사용자 설정을 기반으로 흑백 마스크를 생성합니다. [Painter](https://support.allegorithmic.com/documentation/display/SPDOC/Substance+Painter)의 [스마트 마스크](https://support.allegorithmic.com/documentation/display/SPDOC/Smart+Materials+and+Masks)와 비슷합니다.

이 마스크는 오브젝트 지오메트리 및 AO에 의해 가려진 오브젝트 표면에서의 금속 브러싱의 흥미로운 효과를 나타낸다.

## 매개변수

### 입력

* **월드 스페이스 표준**: *색상 입력*
* **곡률**: *회색 음영 입력*\
  내부 효과 및 마스크에 사용되는 베이킹된 맵.
* **주변 오클루전**: *회색 음영 입력*\
  내부 효과 및 마스크에 사용되는 베이킹된 맵.
* **위치**: *회색 음영 입력*
* **마스크(선택 사항)**: *회색 음영 입력*\
  노드의 효과를 마스킹하는 데 사용되는 마스크 슬롯입니다.

### 매개변수

* **수준**: *0.0 - 1.0*\
  전체 효과 레벨을 점진적으로 표시하도록 설정합니다.
* **대비**: *0.0 - 1.0*\
  결과의 대비를 조정합니다.
* **Scratches 길이**: *0.0 - 8.0*&#x200B;스크래치 길이를 설정합니다. 값이 작을수록 점과 비슷하고, 값이 클수록 긴 줄무늬가 나타납니다.
* **축**: 스크래치를 받아야 하는 개체의 *X, Y, Z, 없음*&#x200B;축. 스크래치 방향을 바꾸지 않습니다.
* **폐색 축 강도**: *0.0 - 1.0*&#x200B;축 오클루전 효과의 강도.
* **오클루전**: *0.0 - 1.0*&#x200B;스크래치 폐색 시 AO의 강도.
* **선명 효과 강도**: *0.0 - 1.0*&#x200B;스크래치에 적용할 선명 효과 후 양을 설정합니다.

## 예제 이미지

![](../../../../../../assets/surface-brush-ex.gif)

</td>
</tr>
</table>
