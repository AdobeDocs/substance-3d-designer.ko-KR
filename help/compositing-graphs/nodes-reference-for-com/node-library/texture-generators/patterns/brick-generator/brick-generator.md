---
helpx_url: "https://helpx.adobe.com/kr/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/patterns/brick-generator.html"
breadcrumb-title: ''
description: '[브릭 생성기] 노드를 사용하여 사용자 정의 가능한 크기, 오프셋 및 모르타르 속성을 가진 절차적 브릭 패턴을 만듭니다.'
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Patterns > Brick Generator
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 벽돌 생성기
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '208'
ht-degree: 0%

---


# 벽돌 생성기

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/brick-generator.png){width="128px"}

## 벽돌 생성기

**인:** *텍스처 생성기**/패턴*

**중간**

</td>
<td style="border: 0;" valign="top">

## 설명

고급 브릭 패턴 생성기. 특별히 인공 벽돌 패턴을 생성하기 위한 많은 옵션이 있습니다.

추가 옵션은 [Tile Generator](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/tile-generator/tile-generator.md)을 참조하세요.

## 매개변수

* **벽돌**: *1 - 64* X축과 Y축 모두의 벽돌 양을 설정합니다.
* **경사**: *0.0 - 1.0*&#x200B;벽돌의 경사 프로필을 변경하고 두 방향으로 변경할 수 있으며 밝기 감소 프로필과 모퉁이 라운딩을 설정할 수 있습니다.
* **비율 유지**: *거짓/참*&#x200B;경사 프로필을 벽돌 크기에 연결하거나 연결하지 않도록 설정합니다.
* **간격**: *0.0 - 1.0*&#x200B;벽돌 사이에 둘 간격. [경사]에는 간격이 추가된다는 점에 유의하십시오. 따라서 경사를 설정해도 이 매개 변수로 보정해야 합니다.
* **중간 크기**: *0.0 - 1.0*&#x200B;브릭 패턴 오프셋으로, 다른 모든 열 또는 행의 크기를 변경합니다.
* **Height**: *-1.0 - 1.0* Height 프로필을 수정합니다. 광도 변형 및 모든 종류의 임의화를 사용할 수 있습니다.
* **경사**: *-1.0 - 1.0*&#x200B;특정 벽돌이 비스듬히 누워있는 것처럼 벽돌마다 경사를 도입합니다.
* **오프셋**: *0.0 - 1.0*\
  행 기준으로 벽돌을 오프셋하고 행별 간격에 영향을 줍니다.
* **비정사각형 확장**: *False/True*\
  제곱이 아닌 비율로 스쿼시와 스트레치를 보정할 수 있습니다.

## 예제 이미지

![](../../../../../../assets/brick-generator-ex-01.gif)

![](../../../../../../assets/brick-generator-ex-02.gif)

</td>
</tr>
</table>
