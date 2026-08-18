---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/patterns/shape-splatter.html"
breadcrumb-title: ''
description: 모양 스플래터 노드를 사용하여 절차 패턴과 세부 사항을 만들기 위해 텍스처 간에 모양을 산란 합니다.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Patterns > Shape Splatter
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 모양 튀김
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '921'
ht-degree: 0%

---


# 모양 튀김

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/shape-splatter.png){width="128px"}

## 모양 튀김

**인:** *텍스처 생성기**/패턴*

**복합**

</td>
<td style="border: 0;" valign="top">

## 설명

함께 제공되는 노드 [모양 튄 혼합](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/shape-splatter-blend/shape-splatter-blend.md), [모양 튄 마스크](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/shape-splatter-to-mask/shape-splatter-to-mask.md) 및 [모양 튄 데이터 추출](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/shape-splatter-data-ext/shape-splatter-data-extract.md)과 함께 사용하도록 설계된 매우 복잡한 노드입니다. [Flood Fill](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/flood-fill/flood-fill.md)와 유사한 다단계 시스템을 통해 [타일 Sampler](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/tile-sampler/tile-sampler.md) 또는 [생성기](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/tile-generator/tile-generator.md)와 유사한 방식으로, 그러나 모든 단계를 제어할 수 있는 동적이고 비파괴적인 프로세스를 통해 모양을 튀기는 데 사용됩니다. Flood Fill이 외부 소스에서 기본 입력 맵을 가져오는 반면, 모양 스플래터는 [Flood Fill](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/flood-fill/flood-fill.md)의 고급 버전처럼 맵과 후속 데이터를 한 번에 생성합니다.

주요 목적은 Height 맵에 모양을 배치할 수 있도록 하고 그 위에 있는 모양을 배치한 다음 스플래터 데이터에서 다양한 맵을 생성하는 것입니다. 예를 들어 풍경에 바위, 잔가지, 나뭇잎 등을 배치합니다. 그런 다음 서로 다른 맵을 Height, 표준, 기본 색상, 거칠기 및 기타 채널에 사용할 수 있으며 모든 맵은 여전히 동일한 공유 스플래터 데이터를 기반으로 합니다.

## 매개변수

### 입력

* **배경 Height**: *회색 음영 입력*&#x200B;타일을 배치하고 다양한 효과를 구동하는 배경 Height.
* **패턴 1-8**: *회색 음영 입력**선택적 패턴*
* **패턴 분포**: *회색 음영 입력*&#x200B;회색 음영 매핑
* **모양 크기 조절**: *회색 음영 입력*&#x200B;타일 크기 조절을 구동하는 회색 음영 맵
* **모양 회전**: *회색 음영 입력*&#x200B;회색 음영 맵을 사용하여 타일 회전을 유도합니다.
* **Height 오프셋**: 타일 Height의 오프셋으로 사용할 *회색 음영 입력*&#x200B;회색 음영 맵
* **Height 크기**: 타일 Height의 오프셋으로 사용할 *회색 음영 입력*&#x200B;회색 음영 맵
* **무작위 마스크**: *회색 음영 입력*\
  노드의 효과를 마스킹하는 데 사용되는 마스크 슬롯입니다.
* **벡터 맵**: *색상 입력*&#x200B;타일 위치 지정 및 회전을 구동하는 색상 벡터 맵

### 매개변수

* **X 양**: *1 - 64*\
  패턴의 X 반복 정도.
* **Y 양**: *1 - 64*\
  패턴의 Y 반복의 양입니다.
* **패턴**
  * **패턴 입력 번호**: *1 - 8*&#x200B;사용할 다른 패턴의 양을 설정합니다. 새 패턴 입력 슬롯을 잠금 해제합니다.
  * **패턴 분포 모드**: *임의, 패턴 색인, 선 색인, 열 색인*&#x200B;사용할 패턴을 결정하는 방법을 설정합니다. 무작위로 또는 패턴, 선 또는 열별로 지정합니다.
  * **패턴 분포 맵 승수**: *0.0 - 1.0*&#x200B;패턴 배치에 대한 선택적 분포 맵의 영향을 설정합니다.
  * **패턴 회전**: *0, 90, 180, 270*&#x200B;패턴의 사전 설정, 90도 회전을 설정합니다.
  * **패턴 회전 무작위**: *0.0 - 1.0*&#x200B;패턴에 대한 무작위 90도 단계 회전 양을 설정합니다.
* **크기**
  * **비율**: *0.0 - 5.0*\
    모든 타일에 대해 균일한 크기를 설정합니다.
  * **무작위 크기 조정**: *0.0 - 1.0*&#x200B;모든 타일에 대해 균일 크기를 임의화합니다.
  * **겹치지 않게 크기 조정**: *0.0 - 1.0*&#x200B;타일이 겹치지 않게 무작위 크기를 균일하게 조정하되 축소합니다. 이전의 두 매개 변수와 함께 사용하면 안 됩니다.
  * **비율 맵 승수**: *0.0 - 1.0*&#x200B;비율 맵의 영향을 설정합니다.
  * **크기**: *0.0 - 1.0*&#x200B;타일의 균일하지 않은 크기 조정을 허용합니다.
  * **Bg 경사의 크기 비율**: *0.0 - 1.0*&#x200B;균일하지 않은 크기 타일에 배경 맵 경사(계산된 표준)을 사용합니다. 원근 뒤틀기를 시뮬레이션합니다.
  * **X/Y 양 비율별 크기**: *0.0 - 1.0* X 및 Y 양의 다른 비율을 보정하기 위한 균일하지 않은 비율.
* **위치**
  * **위치 무작위**: 모든 타일에 대해 *0.0 - 2.0*&#x200B;무작위 오프셋 위치.
  * **임의 분포**: *가우시안, 균일*&#x200B;이전 매개 변수에 사용할 계산을 설정합니다. 큰 차이를 만들지 않고, 숫자가 높을수록 더 두드러집니다. [가우스]은 퍼짐이 더 균일해지는 경향이 있습니다.
  * **벡터 맵 멀티플라이어**: *0.0 - 1.0*&#x200B;오프셋에 대한 벡터 입력 맵의 영향.
  * **오프셋 가로**: *-2.0 - 2.0*&#x200B;전역 가로 오프셋.
  * **오프셋 세로**: *-2.0 - 2.0*&#x200B;전역 세로 오프셋.
  * **범위를 벗어남 옵션**: *모양 크기 조절, 타일이 범위를 벗어난 경우 수행할 위치 제한*&#x200B;작업
* **회전**
  * **회전**: *0.0 - 1.0*&#x200B;모든 타일을 전역적으로 회전합니다.
  * **회전 무작위**: *0.0 - 1.0*&#x200B;타일당 무작위 회전.
  * **배경 경사에서 회전**: *0.0 - 1.0*&#x200B;배경 맵 경사(계산된 표준)를 사용하여 타일을 회전합니다. 경사 위나 아래를 가리키는 모양을 만드는 데 사용할 수 있습니다.
  * **회전 맵 배율**: *0.0 - 1.0*&#x200B;타일별 회전에 대한 회전 맵 효과의 혼합입니다.
  * **벡터 맵 멀티플라이어**: *0.0 - 1.0*&#x200B;타일 단위 회전에 대한 회전 맵의 영향에 대한 혼합.
* **Height**
  * **Height 크기 자동 조정**: *거짓/참*&#x200B;절대 범위를 정의하는 대신 배경에 상대적으로 Height 범위를 자동으로 조정합니다. 제어를 줄이거나 늘릴 수 있습니다.
  * **Height 오프셋**: *-1.0 - 1.0* Height 범위를 통해 모든 타일을 균일하게 오프셋하거나 이동하는 수정자.
  * **Height 오프셋 무작위**: *0.0 - 1.0*&#x200B;타일별로 Height 오프셋을 임의로 변경합니다.
  * **Height 오프셋 맵 변환기**: *0.0 - 1.0*&#x200B;오프셋 맵의 영향을 설정하는 수정자입니다.
  * **Height 크기**: *0.0 - 1.0* Height 범위에 걸쳐 모든 타일의 크기를 균일하게 조정하거나 확장하는 수정자. 오프셋과 반대로 하면 대비와 같이 값이 더 멀어집니다.
  * **Height 크기 무작위**: *0.0 - 1.0*&#x200B;타일별로 Height 크기를 무작위로 변경합니다.
  * **Height 비율 맵 승수**: *0.0 - 1.0*&#x200B;비율 맵의 영향을 설정하는 수정자입니다.
  * **배경 일치**: *0.0 - 1.0*&#x200B;타일과 배경의 혼합에 영향을 줍니다. 순응은 하이맵을 엄격하게 유지하고 순응은 배경 모양을 따르는 것을 의미합니다. 예를 들어 나뭇잎과 스틱에 적합합니다.
  * **일치된 배경 매끄럽게**: *0.0 - 2.0*&#x200B;이전 효과의 매끄러움 값으로, 잘못되거나 극단적인 변형을 방지합니다.
  * **배경 경사에서 기울이기**: *0.0 - 1.0*&#x200B;배경 경사로 구동되는 조정/경사 타일 Height(계산된 표준).
  * **배경 경사 Smoothness**: *0.0 - 2.0*&#x200B;이전 효과의 매끄러움 값으로, 잘못되거나 극단적인 변형을 방지합니다.
  * **검정 픽셀 오려내기**: *False/True*&#x200B;타일 기준 모양에서 전체 검정(0) 픽셀을 무시하도록 전환합니다.
  * **패턴 기준 병합**: *False/True*&#x200B;배경과 타일 혼합 동작을 조정합니다. 타일은 배경과 교차하거나(False) 아래쪽으로 이동하면 배경을 재정의합니다.
* **마스킹**
  * **무작위 마스크**: *0.0 - 1.0*&#x200B;타일을 임의로 숨깁니다. 이 값이 높을수록 타일이 더 많이 사라집니다.
  * **마스크 임의 맵 승수**: *0.0 - 1.0*&#x200B;타일 숨기기를 시작할 때 마스크 맵의 트레숄드를 설정합니다.
  * **배경 경사에서 마스크**: *-1.0 - 1.0*&#x200B;배경 맵 경사(계산된 표준)를 사용하여 타일을 숨깁니다.

## 예제 이미지

</td>
</tr>
</table>
