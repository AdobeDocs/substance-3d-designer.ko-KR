---
helpx_url: "https://helpx.adobe.com/kr/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/weathering/leather-weathering.html"
breadcrumb-title: ''
description: 가죽 풍화 노드를 사용하여 메쉬 곡률을 기반으로 가죽 소재에 마모 패턴과 에이징 효과를 추가합니다.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Weathering > Leather Weathering
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 가죽 풍화
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '455'
ht-degree: 0%

---


# 가죽 풍화

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/leather-weathering.png){width="128px"}

## 가죽 풍화

**내부:** *메쉬 기반 생성기**/풍화*

**복합**

</td>
<td style="border: 0;" valign="top">

## 설명

여러 채널에서 한 번에 작동하는 전체 재질 효과입니다. 나이와 더러움을 조절할 수 있는 무작위 가죽 마모 효과를 추가합니다. [직물 풍화](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/mesh-based-generators/weathering/fabric-weathering/fabric-weathering.md)와 비슷하지만, 특히 가죽을 위해 조정되었습니다.\
이 효과는 제대로 된 구운 AO와 월드 스페이스 노르말맵이 연결되어 있지 않은 한 잘 작동하지 않습니다. 모든 것을 적절하게 계산하고 생성하기 위해서는 이러한 것이 필요하기 때문입니다.

전체 재질을 사용하여 작업할 때는 [링크 만들기 모드](https://support.allegorithmic.com/documentation/display/SD5/Link+Creation+Modes)를 완전히 이해해야 합니다.

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
  * **사용됨**: *0.0 - 1.0*&#x200B;전 세계에서 마모된 가죽 모양의 혼합.
  * **나이**: *0.0 - 1.0* AO를 기반으로 한 주름에서 마모된 가죽 모양의 혼합 효과. 배치는 Age Treshold의 영향을 많이 받습니다.
  * **나이 임계값**: *0.0 - 1.0*&#x200B;나이 효과에 대한 모양 임계값을 설정합니다.
  * **균열 비율**: *1.0 - 16.0*&#x200B;중고 및 연령 효과에서 닳은 가죽의 깊이를 설정합니다.
  * **균열 뒤틀기 강도**: *0.0 - 1.0*&#x200B;사용된 가죽 및 연령 효과의 마모된 가죽 강도를 설정합니다.
  * **선명한 가장자리 Scratches 크기**: *1.0 - 32.0*
  * **선명한 가장자리 Scratches 뒤틀기 강도**: *0.0 - 1.0*
  * **사용된 가죽 채도 감소**: *0.0 - 1.0*&#x200B;오래된 가죽 모양과 사용된 효과의 채도를 설정합니다.
  * **사용된 가죽 명도**: *0.0 - 1.0*&#x200B;오래된 가죽 모양과 사용된 효과의 명도를 설정합니다.
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

![](../../../../../../assets/leather-ex.gif)

![](../../../../../../assets/leather-ex2.png){width="233px"}

</td>
</tr>
</table>
