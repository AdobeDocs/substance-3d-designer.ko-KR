---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/weathering/fabric-weathering.html"
breadcrumb-title: ''
description: Fabric Weathering 노드를 사용하여 메쉬 형상 및 곡률을 기반으로 패브릭 재질에 마모 및 에이징 효과를 추가합니다.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Weathering > Fabric Weathering
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 섬유 풍화
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '477'
ht-degree: 0%

---


# 섬유 풍화

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/fabric-weathering.png){width="128px"}

## 섬유 풍화

**내부:** *메쉬 기반 생성기**/풍화*

**복합**

</td>
<td style="border: 0;" valign="top">

## 설명

여러 채널에서 한 번에 작동하는 전체 재질 효과입니다. 그것은 나이와 더러운 것에 대한 제어와 함께 무작위 직물 마모 효과를 추가합니다.\
이 효과는 제대로 된 구운 AO와 월드 스페이스 노르말맵이 연결되어 있지 않으면 제대로 계산되고 생성되기 때문에 잘 작동하지 않습니다.

전체 재질을 사용하여 작업할 때는 [링크 만들기 모드](../../../../../../interface/the-graph-view/link-creation-modes/link-creation-modes.md)를 완전히 이해해야 합니다.

## 매개변수

### 입력

* **주변 오클루전**: *회색 음영 입력*\
  내부 효과 및 마스크에 사용되는 베이킹된 맵.
* **일반 월드 공간**: *색상 입력*
* **마스크** : *회색 음영 입력*\
  노드의 효과를 마스킹하는 데 사용되는 마스크 슬롯입니다. &quot;마스크&quot; 매개 변수로 전환할 수 있습니다.

### 매개변수

* **채널**
  * 예를 들어 [금속]/[거칠음] 대신 [Specular/광택] 맵을 사용하는 경우 이 그룹에서 재질 채널을 켜거나 끌 수 있습니다.
* **고급**
  * **표준 형식**: *DirectX, OpenGL*\
    서로 다른 표준 맵 포맷 사이를 전환합니다(녹색 채널을 반전합니다).
  * **마스크**: *False/True*\
    마스크 맵 사용을 설정하거나 해제합니다.
* **효과**
  * **Dust**: *0.0 - 1.0*&#x200B;월드 스페이스 표준 지도에서 위를 향하는 영역을 기준으로 어두운 Dust 효과를 혼합합니다.
  * **더러움**: *0.0 - 1.0* AO에서 대부분 가려진(어두운) 영역을 기반으로 하는 전역 Dirt/손가락 효과에 혼합됩니다.
  * **가장자리 착용**: *0.0 - 1.0*&#x200B;재질 표준을 기반으로 가장자리에 선명/심화 효과를 추가합니다.
  * **사용됨**: *0.0 - 1.0* AO를 기준으로 매우 어둡게 누적된 Dirt의 혼합입니다. 최대값 및 최소값은 극단적인 경향이 있으므로 주의해서 사용하십시오.
  * **나이**: *0.0 - 1.0*&#x200B;전역 타일링 마모 패턴 위에 혼합됩니다. 아래의 Treshold 컨트롤은 AO 영향을 제어합니다. 최댓값과 최솟값은 극단적인 경향이 있습니다.
  * **연령 임계값**: *0.0 - 1.0* AO가 연령 매개 변수에 영향을 주는 정도를 설정합니다.
  * **연령 감소**: *0.0 - 1.0*&#x200B;연령 효과의 미세한 추가 주름의 혼합을 제어합니다.
  * **날카로운 가장자리 Scratches 크기**: *1.0 - 32.0*&#x200B;작은 스크래치 크기를 설정하며, 주로 사용된 스크래치 및 노화 효과를 긁어냅니다.
  * **날카로운 가장자리 Scratches 뒤틀기 강도**: *0.0 - 1.0*&#x200B;위의 작은 스크래치에 대한 뒤틀기 강도를 설정합니다.
  * **이전 패브릭 채도 감소**: *0.0 - 1.0*&#x200B;연령 효과의 채도 감소를 제어합니다.
  * **이전 섬유 밝기**: *0.0 - 1.0*&#x200B;연령 효과의 밝기를 제어합니다. *이것은 원하는 모양을 얻기 위해 변경하는 데 매우 중요한 매개 변수입니다. 하지만 극단적인 결과를 얻을 수 있습니다. 하위 변경 내용에 사용하십시오.*
* **혼합**
  * **확산 강도**: *0.0 - 1.0*\
    확산 영역의 혼합 강도입니다.
  * **기본 색상 강도**: *0.0 - 1.0*\
    기본 색상의 혼합 강도입니다.
  * **표준 강도**: *0.0 - 1.0*\
    표준의 혼합 강도입니다.
  * **Specular 강도**: *0.0 - 1.0*\
    Specular의 혼합 강도입니다.
  * **광택 강도**: *0.0 - 1.0*\
    광택의 혼합 강도입니다.
  * **거칠음 강도**: *0.0 - 1.0*\
    거칠기의 혼합 강도입니다.
  * **주변 오클루전 강도**: *0.0 - 1.0*\
    주변 오클루전의 혼합 강도입니다.
  * **Height 강도**: *0.0 - 1.0*\
    Height의 혼합 강도입니다.

## 예제 이미지

![](../../../../../../assets/fabric-ex.gif)

</td>
</tr>
</table>
