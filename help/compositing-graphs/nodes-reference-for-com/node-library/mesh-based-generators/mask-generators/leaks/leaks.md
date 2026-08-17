---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/mask-generators/leaks.html"
breadcrumb-title: ''
description: 누수 노드를 사용하여 메시 형상을 기반으로 물 얼룩과 유체 효과를 생성하는 누수 패턴을 생성합니다.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Mask Generators > Leaks
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 누출
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '333'
ht-degree: 1%

---


# 누출

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/leaks.png){width="128px"}

## 누출

**내부:** *메시 기반 생성기**/마스크 생성기*

**중간**

</td>
<td style="border: 0;" valign="top">

## 설명

베이킹된 맵 및 사용자 설정을 기반으로 흑백 마스크를 생성합니다. [Painter](https://support.allegorithmic.com/documentation/display/SPDOC/Substance+Painter)의 [스마트 마스크](https://support.allegorithmic.com/documentation/display/SPDOC/Smart+Materials+and+Masks)와 비슷합니다.

이 마디는 날카로운 모서리에서 나오는 Dirt 줄무늬와 그림이 새어 나오는 것을 나타냅니다. 구운 위치에서 줄무늬가 생성되므로 항상 아래쪽으로 이동합니다.

변형 마스크를 변경해 보십시오. 변형 마스크는 줄무늬의 배치를 구동하므로 다른 [마스크 생성기]에 비해 훨씬 더 큰 영향을 미칠 수 있습니다.

## 매개변수

### 입력

* **위치**: *회색 음영 입력*\
  줄무늬 방향에 사용되는 구워진 위치 맵입니다. 필수!
* **곡률**: *회색 음영 입력*\
  줄무늬 배치에 사용되는 베이킹된 맵. 필수!
* **주변 오클루전**: *회색 음영 입력*\
  내부 효과 및 마스크에 사용되는 베이킹된 맵. 권장되지만 대신 플랫 화이트를 사용할 수 있습니다.
* **일반 월드 공간**: *색상 입력*\
  Baked World Space Normalmap, 줄무늬 연출에 사용됨. 필수!
* **변형 마스크**: *회색 음영 입력*\
  변형 마스크(선택 사항)는 재정의를 True로 설정하여 활성화합니다.
* **마스크(선택 사항)**: *회색 음영 입력*\
  노드의 효과를 마스킹하는 데 사용되는 마스크 슬롯입니다.

### 매개변수

* **수준**: *0.0 - 1.0*\
  결과의 총 레벨입니다. 점진적으로 효과를 표시하고 길이에도 영향을 줍니다. 긴 물방울을 얻기 위해서는 꽤 높게 설정되어야 한다.
* **대비**: *0.0 - 1.0*\
  결과의 대비를 조정합니다.
* **변형**: *0.0 - 1.0*&#x200B;줄무늬를 마스킹하는 데 사용되는 대규모 변형의 양을 설정합니다. 이 값을 0으로 설정하면 완전히 균일한 줄무늬가 나타나므로 이 방법은 사용하지 마세요.
* **길이**: *0.0 - 8.0*&#x200B;줄무늬의 길이 이 값을 너무 높게 설정하면 단계별로 표시됩니다. 레벨도 사용해 보세요.
* **폐색**: *X, Y, Z, 없음* AO가 영향을 미치는 방향을 설정합니다.
* **변형 마스크 재정의**: *False/True*&#x200B;사용자 지정 입력 슬롯으로 변형 마스크를 재정의할 수 있습니다. 더 희미하거나 더 조밀한 마스크를 사용하는 것은 흥미로울 수 있으며, 물방울을 제어하는 좋은 방법입니다.

## 예제 이미지

![](../../../../../../assets/leaks-ex.gif)

</td>
</tr>
</table>
