---
helpx_url: "https://helpx.adobe.com/kr/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/mask-generators/grease.html"
breadcrumb-title: ''
description: 메시 형상 및 접촉 영역을 기반으로 그리스 누적 마스크를 생성하려면 그리스 노드를 사용합니다.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Mask Generators > Grease
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 그리스
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '186'
ht-degree: 2%

---


# 그리스

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/grease.png){width="128px"}

## 그리스

**내부:** *메시 기반 생성기**/마스크 생성기*

**단순**

</td>
<td style="border: 0;" valign="top">

## 설명

베이킹된 맵 및 사용자 설정을 기반으로 흑백 마스크를 생성합니다. [Painter](https://support.allegorithmic.com/documentation/display/SPDOC/Substance+Painter)의 [스마트 마스크](https://support.allegorithmic.com/documentation/display/SPDOC/Smart+Materials+and+Masks)와 비슷합니다.

이 마스크는 특히 캐릭터 얼굴 및 기타 특정 영역을 위한 것입니다. Thickness이 낮은 영역에 스킨 그리스 유형의 마스크를 생성합니다.

## 매개변수

### 입력

* **Thickness**: *회색 음영 입력*\
  전체 효과의 기초가 되는 Thickness 맵을 구웠습니다. 필수!
* **노이즈**: *회색 음영 입력*\
  그리스 그런지를 재정의할 선택적 노이즈 맵
* **마스크(선택 사항)**: *회색 음영 입력*\
  노드의 효과를 마스킹하는 데 사용되는 마스크 슬롯입니다.

### 매개변수

* **수준**: *0.0 - 1.0*\
  표시할 효과의 총 양을 설정합니다.
* **대비**: *0.0 - 1.0*\
  결과의 대비를 조정합니다.
* **Thickness 임계값**: *0.0 - 1.0*&#x200B;효과가 나타나는 최소 Thickness을 설정합니다. [레벨]로도 중요합니다. Thickness 맵에 맞게 조정합니다.
* **노이즈 재정의**: *False/True*&#x200B;내부 그리스 그런지 맵을 사용자 지정 입력 슬롯으로 재정의하도록 설정합니다.

## 예제 이미지

![](../../../../../../assets/grease-ex.gif)

</td>
</tr>
</table>
