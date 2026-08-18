---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/effects-material/season-filter.html"
breadcrumb-title: ''
description: '[시즌 필터] 노드를 사용하여 봄, 여름, 가을, 겨울 변형을 만드는 재질에 계절별 효과를 적용합니다.'
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > Effects (Material) > Season Filter
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 계절 필터
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '428'
ht-degree: 0%

---


# 계절 필터

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/default-icon.png){width="128px"}

## 계절 필터

**내부:** *재질 필터/효과*

**복합**

</td>
<td style="border: 0;" valign="top">

## 설명

이 노드는 애니메이션 수위, 눈, 얼음 및/또는 이끼와 같은 효과를 추가합니다.

이 필터는 PBR 교정이 불가능한 이전 버전이라는 점을 명심하십시오. 일부 경우에는 여전히 유용할 수 있지만 대부분 레거시/호환성의 이유로 보관됩니다. [Snow 표지](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/effects-material/snow-cover/snow-cover.md) 및 [수위](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/effects-material/water-level/water-level.md)에서 최신 PBR 수정 버전을 확인할 수 있습니다.

노드는 적절한 재료 투입의 집합을 요구하는데, 주로 세밀한 Heightmap 또는 Normalmap과 함께한다.

## 매개변수

### 입력

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
  * **조명 강도**: *0.0 - 1.0*\
    (위조된) 조명의 강도입니다.
  * **조명 각도**: *0.0 - 1.0*\
    (가짜) 빛의 입사각
* **효과**
  * **Height 또는 표준으로 효과**: *Height, 표준*&#x200B;효과를 구동하는 입력 맵을 선택합니다.
  * **수위**: *0.0 - 1.0* Height/일반 정보에 따라 수위를 높이거나 낮춥니다.
  * **물 세부 정보**: *0.0 - 1.0*&#x200B;물의 세부 정보 양을 설정합니다.
  * **굴절**: *0.0 - 1.0*&#x200B;효과의 거짓 굴절 양을 설정합니다.
  * **반사**: *0.0 - 1.0*&#x200B;효과에 대한 거짓 반사의 양을 설정합니다.
  * **반사 거리**: *0.0 - 1.0*&#x200B;반사 비주얼을 제어합니다.
  * **반사 각도**: *0.0 - 1.0*&#x200B;반사 비주얼을 제어합니다.
  * **흐름 방향**: *0.0 - 1.0*&#x200B;애니메이션 흐름을 제어합니다(Substance Player을 사용하여 시각화).
  * **얼음**: *0.0 - 1.0*&#x200B;물이 얼는 정도를 설정합니다.
  * **얼음 세부 사항**: *0.0 - 1.0*&#x200B;얼음의 세부 사항을 설정합니다.
  * **Snow**: *0.0 - 1.0*&#x200B;적설 범위를 설정합니다.
  * **이끼**: *0.0 - 1.0*&#x200B;이끼 검사 양을 설정합니다.
  * **이끼 비율**: *1 - 4*&#x200B;생성된 이끼 텍스처의 비율을 설정합니다.
  * **이끼 색상**: *(색상 값)*이끼 색상을 설정합니다.
  * **물 색상**: *(색상 값)*알파/불투명도를 포함한 물의 색상을 설정합니다.
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

|  |
| --- |
| 이 페이지에 첨부된 이미지가 없습니다. |

</td>
</tr>
</table>
