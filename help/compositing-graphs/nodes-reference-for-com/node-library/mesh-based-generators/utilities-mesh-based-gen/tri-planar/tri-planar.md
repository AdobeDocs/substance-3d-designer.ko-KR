---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/utilities-mesh-based-generators/tri-planar.html"
breadcrumb-title: ''
description: 3개의 평면 노드를 사용하면 복잡한 형상에 대한 원활한 텍스처 매핑을 위해 3개의 직교 평면에서 텍스처를 투영할 수 있습니다.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Utilities (Mesh Based Generators) > Tri Planar
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 삼중 평면
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '439'
ht-degree: 0%

---


# 삼중 평면

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/triplanar-1.png){width="128px"}

![](../../../../../../assets/triplanar-grayscale.png){width="128px"}

## 삼각 평면(회색 음영)

**내부:** *메시 기반 생성기**/유틸리티*

**복합**

</td>
<td style="border: 0;" valign="top">

## 설명

이 고급 노드는 베이킹된 위치 및 월드 스페이스 표준 데이터를 기반으로 2D에서 삼평면 투영 매핑을 수행합니다. 이는 메쉬 자체를 기반으로 UV 좌표를 (대부분) 이음새가 없는 매핑으로 완전히 변환하는 것을 의미합니다.

이것은 매번 다시 구울 필요 없이 솔기를 피하기 위한 좋은 방법입니다 (제빵사와 유사한 것을 달성 할 수 있습니다). 단점은 이 노드가 상당히 무겁기 때문에 빠르지 않다는 점이다.

베이크는 고정밀이어야 한다는 점을 염두에 두십시오. 8비트 베이크는 매우 좋은 결과로 이어지지 않습니다.

## 매개변수

### 입력

* **위치**: *색상 입력*\
  위치 맵을 구웠습니다. 16비트 이상의 정밀도를 사용하는 것이 좋습니다.
* **월드 스페이스 표준**: *색상 입력*\
  Baked World Space Normal 지도, 이상적으로 16비트 이상의 정밀도.
* **입력 X**: *색상 입력(회색 음영 입력)*3면 투영을 통해 UV에서 월드 공간으로 다시 매핑할 맵을 입력합니다. [이미지 입력]을 1로 설정한 경우 모든 축에 사용되고, [X 축]을 3으로 설정한 경우 모든 축에 사용됩니다.
* **입력 Y**: *색상 입력(회색 음영 입력)*이미지 입력이 3으로 설정된 경우에만 가능합니다. Y축의 UV에서 월드 공간으로 다시 매핑할 맵을 입력합니다.
* **입력 Z**: *색상 입력(회색 음영 입력)*이미지 입력이 3으로 설정된 경우에만 가능합니다. Z축의 UV에서 월드 공간으로 다시 매핑할 맵을 입력합니다.

### 매개변수

* **투영**: *모든 축, X만, Y만, Z만*&#x200B;혼합할 축을 설정합니다.
* **이미지 입력**: *1개 입력, 3개 입력*\
  모든 축에 하나의 맵을 사용할지, 아니면 축당 특정 맵을 사용할지 설정합니다.
* **혼합 모드**: *선형, 고급*&#x200B;정확도 및 정밀도를 높입니다.
* **혼합 대비**: *0.001 - 1.0*&#x200B;전환 대비, 매끄러운 전환 또는 거친 전환을 혼합합니다.
* **정규화 요소**: *0.0 - 1.0*\
  혼합 영역에서 대비의 손실을 복원하여 투영 혼합을 개선합니다.
* **텍스처 타일링**: *0.0 - 10.0*&#x200B;입력 텍스처를 타일링한 횟수
* **전역 회전**: *0.0 - 1.0*\
  모든 축에 대한 전역 회전입니다.
* **미러된 투영 수정**: *False/True*&#x200B;미러된 투영을 처리하는 방법을 설정합니다.
* **회전 X**: *0.0 - 1.0*&#x200B;투영 X축을 통한 개별 회전.
* **회전 Y**: *0.0 - 1.0*&#x200B;투영 Y축을 통한 개별 회전.
* **회전 Z**: *0.0 - 1.0*&#x200B;투영 Z축을 통한 개별 회전.
* **오프셋 X**: *0.0 - 1.0*&#x200B;프로젝션 X축에 대한 오프셋.
* **임의 오프셋 X**: *0.0 - 1.0*\
  X축 오프셋의 임의화를 허용합니다.
* **오프셋 Y**: *0.0 - 1.0*&#x200B;프로젝션 Y축에 대한 오프셋.
* **임의 오프셋 Y**: *0.0 - 1.0*\
  Y축 오프셋의 임의화를 허용합니다.
* **오프셋 Z**: *0.0 - 1.0*&#x200B;프로젝션 Z축에 대한 오프셋.
* **임의 오프셋 Z**: *0.0 - 1.0*\
  Z축 오프셋의 임의화를 허용합니다.

## 예제 이미지

</td>
</tr>
</table>
