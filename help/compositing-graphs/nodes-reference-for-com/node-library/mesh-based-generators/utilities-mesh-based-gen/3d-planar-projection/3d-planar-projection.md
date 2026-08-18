---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/utilities-mesh-based-generators/3d-planar-projection.html"
breadcrumb-title: ''
description: 3D 평면 투영 노드를 사용하여 텍스처 매핑의 평면 투영을 사용하여 메시 표면에 텍스처를 투영합니다.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Utilities (Mesh Based Generators) > 3D Planar Projection
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 3D 평면 투영
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '251'
ht-degree: 1%

---


# 3D 평면 투영

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/3d-planar-gray.png)![](../../../../../../assets/3d-planar.png)

## 3D 평면 투영(색상)

**내부:** *메시 기반 생성기**/유틸리티*

**복합**

</td>
<td style="border: 0;" valign="top">

## 설명

구워진 메시 데이터(위치 및 세계 표준 맵)를 기반으로 평면 투영을 수행합니다. 원래 UV 매핑과 관계없이 이음새 간에 데칼을 투영하고 배치할 수 있습니다.

## 매개변수

### 입력

* **위치 맵**: *색상 입력*&#x200B;위치 맵을 구했습니다.
* **월드 스페이스 표준**: *색상 입력*&#x200B;구워진 월드 스페이스 표준 맵
* **예상된 텍스처**: *색상 입력*&#x200B;대상에 투영할 텍스처 입력

### 매개변수

* **위치**
  * **프로젝트 입력**: *UV 위치, 세계 공간 위치*&#x200B;투영 위치를 2D/UV로 설정할지, 3D/세계 공간으로 설정할지 선택합니다.
  * **대상 UV 위치**:\
    UV 위치 입력에서만 [위치] 맵의 2D 보기에서 점을 선택하는 데 가장 적합합니다.
  * **대상 위치**: *(색상 값)*World Space Position 입력만 사용하면 정확한 3D 좌표를 정의할 수 있습니다.
  * **대상 표준**: *(색상 값)*
  * **회전**: *0.0 - 1.0\
    투영된 텍스처를 수직 축을 따라 회전합니다.*
  * **비율**: *0.0 - 1.0*\
    투영된 텍스처의 전체 배율을 설정합니다.
  * **크기**: *0.0 - 2.0*&#x200B;투영된 텍스처에 대해 균일하지 않은 크기 조절을 수행합니다.
* **마스킹**
  * **최대 깊이**: *0.0 - 1.0*&#x200B;텍스처가 잘릴 때 표시되는 깊이를 제어합니다.
  * **깊이 페이드**: *0.0 - 1.0*&#x200B;컷오프 깊이의 전환을 갑자기 설정하거나 희미하게 설정합니다.
  * **보통 임계값**: *-1.0 - 1.0*&#x200B;정사각형과 정확히 정렬되지 않은 표면에 대한 임계값 설정.
  * **표준 페이드**: *0.0 - 1.0*&#x200B;정렬되지 않은 표면에 대한 전환을 갑작스럽게 또는 페이드로 설정합니다.

## 예제 이미지

![](../../../../../../assets/3d-planar-projection-ex.gif)

</td>
</tr>
</table>
