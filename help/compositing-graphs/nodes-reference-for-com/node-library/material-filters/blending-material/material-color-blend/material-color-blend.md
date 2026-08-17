---
helpx_url: "https://helpx.adobe.com/kr/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/blending-material/material-color-blend.html"
breadcrumb-title: ''
description: 재질 색상 혼합 노드를 사용하여 복합 재질 효과를 만들기 위해 재질 간에 색상 채널을 혼합합니다.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > Blending (Material) > Material Color Blend
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 재질 색상 혼합
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '466'
ht-degree: 0%

---


# 재질 색상 혼합

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/material-color-blend.png){width="128px"}

## 재질 색상 혼합

**내부:** *재질 필터/혼합*

**중간**

</td>
<td style="border: 0;" valign="top">

## 설명

이 노드를 사용하면 맨 위에 단색을 혼합하여 다중 채널 전체 재질을 조정할 수 있습니다. 이는 [재질 조정 블렌드](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/blending-material/material-adjustment-blend/material-adjustment-blend.md)와의 주요 차이점으로, 채널에는 [레벨](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/levels/levels.md) 유형의 조정만 허용되며, 이 노드에서는 단색과 함께 [블렌드](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/blend/blend.md) 유형의 조정을 사용합니다.

이 노드는 [확산] 또는 [기본 색상]에 플랫 색상 힌트를 도입하거나 설정된 단색 값을 사용하여 다른 채널을 &quot;병합&quot;하려는 경우 가장 유용합니다.

## 매개변수

### 입력

* **ColorID**: *색상 입력*\
  노드의 효과를 마스킹하는 데 사용되는 마스크 슬롯입니다.
* **회색 음영 마스크**: *회색 음영 입력*\
  노드의 효과를 마스킹하는 데 사용되는 마스크 슬롯입니다.

### 매개변수

* **채널**
  * 예를 들어 [금속/거칠음] 대신 [Specular/광택] 맵을 사용하는 경우 이 그룹에서 재질 채널을 켜거나 끌 수 있습니다.
* **확산**
  * **색상**: *(색상 값)*확산 채널 위에서 혼합할 색상 값입니다.
  * **불투명도**: *0.0 - 1.0*\
    전경과 배경 간 불투명도 혼합.
  * **혼합 모드**: *표준, 추가, 빼기, 곱하기, 추가/하위, 최대, 최소, 전환*&#x200B;연산에 사용할 혼합 모드.
* **기본 색상**
  * [확산] 그룹에서와 같은 옵션을 사용하여 이 채널 위에 단색을 혼합합니다.
* **표준**
  * **원본**: *Height, 마스크*
  * **혼합 모드**: *결합, 혼합*
  * **Height 강도**: *0.0 - 1.0*
  * **Height 불투명도**: *0.0 - 1.0*
  * **형식**: *DirectX, OpenGL*
* **Specular**
  * [확산] 그룹에서와 같은 옵션을 사용하여 이 채널 위에 단색을 혼합합니다.
* **발광**
  * [확산] 그룹에서와 같은 옵션을 사용하여 이 채널 위에 단색을 혼합합니다.
* **광택**
  * [확산] 그룹에서와 같은 옵션을 사용하여 이 채널 위에 단색을 혼합합니다.
* **거칠음**
  * [확산] 그룹에서와 같은 옵션을 사용하여 이 채널 위에 단색을 혼합합니다.
* **금속**
  * [확산] 그룹에서와 같은 옵션을 사용하여 이 채널 위에 단색을 혼합합니다.
* **Specular level**
  * [확산] 그룹에서와 같은 옵션을 사용하여 이 채널 위에 단색을 혼합합니다.
* **주변 오클루전**
  * [확산] 그룹에서와 같은 옵션을 사용하여 이 채널 위에 단색을 혼합합니다.
* **Height**
  * [확산] 그룹에서와 같은 옵션을 사용하여 이 채널 위에 단색을 혼합합니다.
* **불투명도**
  * [확산] 그룹에서와 같은 옵션을 사용하여 이 채널 위에 단색을 혼합합니다.
* **색상 ID 마스크**: *False/True*&#x200B;회색 음영 마스크 대신 색상 ID 마스크를 사용합니다. 이 색상은 한 가지 색상에만 적용된다는 점을 기억하십시오!\
  아래 옵션을 모두 활성화합니다.
* **색상**: *(색상 값)*선택하고 흰색으로 변환할 색상입니다.
* **허용량**: *0.01 - 1.0*&#x200B;선택한 색상이 주변과 혼합되는 정도입니다.
* **패딩**: *0.0 - 1.0*&#x200B;선택한 색상의 전환 대비.

## 예제 이미지

|  |
| --- |
| 이 페이지에 첨부된 이미지가 없습니다. |

</td>
</tr>
</table>
