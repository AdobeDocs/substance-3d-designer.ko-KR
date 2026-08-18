---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/patterns/shape.html"
breadcrumb-title: ''
description: 모양 노드를 사용하여 Substance 3D Designer에서 패턴 및 텍스처를 만들기 위한 기본 기하학적 모양을 생성합니다.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Patterns > Shape
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 모양
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '215'
ht-degree: 2%

---


# 모양

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/shape-2.png){width="128px"}

## 모양

**인:** *텍스처 생성기**/패턴*

**중간**

</td>
<td style="border: 0;" valign="top">

## 설명

기본 모양을 수정하는 옵션을 사용하여 다양한 절차 모양을 생성합니다. 모양은 항상 완벽하게 보간되고 고정밀입니다.

단순함에도 불구하고, 이것은 매우 유용한 노드입니다: 그것은 대부분의 절차적 하이트맵 생성의 기본 요소입니다! 기본 모양을 변형 노드와 결합하면 어떤 비트맵보다 훨씬 더 정확한 완벽한 절차의 Heightmap 모양을 만들 수 있습니다.

## 매개변수

* **타일링**: *1 - 16*\
  결과가 바둑판식으로 표시될 횟수를 설정합니다.
* **패턴**: *정사각형, 디스크, 포물선, 벨, 가우스, 가시, 피라미드, 벽돌, 그라데이션, 파도, 하프 벨, 리지 벨, 크레스칸트, 캡슐, 원뿔*, 반구**\
  사용할 패턴 모양을 선택합니다.
* **패턴별**: *0.0 - 1.0*\
  선택한 패턴의 모양을 변경할 수 있습니다. 효과는 선택한 패턴에 따라 달라집니다.
* **크기 조절**: *0.0 - 1.0*&#x200B;전체 모양의 크기를 조절합니다.
* **크기**: *0.0 - 1.0* X축 또는 Y축에 대해 균일하지 않은 크기 조절을 허용합니다.
* **각도**: *0.0 - 1.0*&#x200B;전체 모양을 회전합니다.
* **회전 45°**: *False/True*&#x200B;미리 설정된 45도로 회전합니다.
* **비정사각형 확장**: *False/True*\
  제곱이 아닌 비율로 스쿼시와 스트레치를 보정할 수 있습니다.
* **정사각형이 아닌 타일링****:** *False/True*비정사각형 확장을 사용하도록 설정하면 모양이 찌그러지지 않고 타일링됩니다.

## 예제 이미지

![](../../../../../../assets/shape-ex.gif)

</td>
</tr>
</table>
