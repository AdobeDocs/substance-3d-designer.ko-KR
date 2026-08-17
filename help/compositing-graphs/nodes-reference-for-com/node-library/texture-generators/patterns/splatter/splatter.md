---
helpx_url: "https://helpx.adobe.com/kr/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/patterns/splatter.html"
breadcrumb-title: ''
description: 스플래터 노드를 사용하여 텍스처 간에 모양을 산란 하여 무작위 패턴과 유기적인 텍스처 세부 사항을 만들 수 있습니다.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Patterns > Splatter
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 스플래터
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '329'
ht-degree: 0%

---


# 스플래터

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/splatter.png)

![](../../../../../../assets/splatter-color.png)

## 스플래터(색상)

**인:** *텍스처 생성기**/패턴*

**복합**

</td>
<td style="border: 0;" valign="top">

## 설명

스플래터 는 지도 입력을 무작위로 배치하기 위한 패턴 생성기입니다. 기하학적 패턴 배치를 위한 많은 컨트롤이 있으며 [Tile Generator](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/tile-generator/tile-generator.md)보다 사용이 간단합니다. 후자도 비슷한 결과를 얻을 수 있지만 훨씬 복잡하다.

스플래터는 모양을 너무 수정하지 않고도 빠르게 찍어낼 수 있는 작업에 적합합니다.

기본 스플래터 매개 변수는 전혀 무작위로 보이지 않는다는 점을 기억하십시오. 임의화를 위해서는 이러한 매개 변수 중 일부를 수정해야 합니다(주로 장애 매개 변수). 또한 스플래터가 작동하려면 지도 입력이 필요합니다.

## 매개변수

* **패턴 크기 너비**: *0.0 - 1000.0* X축에 사용할 패턴 수입니다.
* **패턴 크기 Height**: *0.0 - 1000.0* Y축에 사용할 패턴 수.
* **회전**: *-360.0 - 360.0*&#x200B;설정된 양만큼 모든 패턴을 회전합니다.
* **회전 변형**: *0.0 - 360.0*&#x200B;모든 개별 모양에 대해 임의 회전을 도입합니다.
* **확대/축소**: *100.0 - 10000.0*&#x200B;최종 결과의 크기를 조정합니다. 이렇게 하면 타일링이 풀린다는 것을 명심해라!
* **게인**: *0.0 - 10.0*&#x200B;모든 패턴의 혼합 게인을 조정합니다. 더 돋보이게 합니다.
* **팬 X**: *-100.0 - 100.0* X축에서 전체 결과를 팬합니다.
* **Y 이동**: *-100.0 - 100.0* Y축에서 전체 결과를 팬합니다.
* **장애**: *0.0 - 100.0*\
  모양을 임의로 이동합니다.
* **격자 번호**: *0 - 8*&#x200B;결과 배율을 조정하기 위해 다른 격자 크기로 이동합니다. 타일링을 유지합니다.
* **장애 각도**: *0.0 - 360.0*&#x200B;장애 각도 이동을 제어합니다.
* **무질서 무작위**: *거짓/참*&#x200B;무질서 각도를 무작위화하여 훨씬 더 많은 혼란을 추가합니다.
* **패턴 크기**: *5 - 12*
* **크기 변형**: *0.0 - 100.0*&#x200B;모든 모양에 대해 무작위 크기 조정을 도입합니다.
* **이미지 입력 필터링(엔진 > v4만 해당)**: *쌍선형 + 밉맵, 쌍선형, 최단값*&#x200B;입력 이미지에 적용할 필터링입니다.
* **출력 레벨 최소**: *0.0 - 1.0*&#x200B;출력 최소 레벨 조정.
* **출력 수준 최대**: *0.0 - 1.0*&#x200B;최대 수준 조정 초과.
* **배경색**: *(회색 음영 값)*단색 배경색을 설정합니다.
* **광도 변형**: *0.0 - 1.0(회색 음영 버전만)*광도 변형을 도입합니다.
* **색상 변형**: *0.0 - 1.0(색상 버전만)*색상 변형을 도입합니다.

## 예제 이미지

![](../../../../../../assets/splatter-ex.gif)

</td>
</tr>
</table>
