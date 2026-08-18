---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/pbr-utilities/pbr-albedo-safe-color.html"
breadcrumb-title: ''
description: PBR 알베도 안전 색상 노드를 사용하여 알베도 색상이 PBR 재질에 대해 물리적으로 적합한 범위 내에 있는지 확인합니다.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > PBR Utilities > PBR Albedo Safe Color
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: PBR 알베도 안전 색상
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '153'
ht-degree: 1%

---


# PBR 알베도 안전 색상

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/pbr-albedo-safe-color.png){width="128px"}

## PBR 알베도 안전 색상

**내부:** *재질 필터/PBR 유틸리티*

**단순**

</td>
<td style="border: 0;" valign="top">

## 설명

[기본 색상] 또는 [확산] 값이 적합한 PBR-교정 범위를 벗어난 경우 교정하는 유틸리티 노드입니다. 이 값을 Metallic으로 설정하면 노드에서는 Metallic 강도를 기준으로 Basecolor 값을 수정하려고 합니다.

또한 잘못된 영역에 대한 시각적 피드백은 [PBR BaseColor/Metallic Validate](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/pbr-utilities/pbr-basecolor-metallic/pbr-basecolor-metallic-validate.md)을 참조하십시오.

이는 빠른 교정 도구로 유용하며, 특히 PBR을 아직 학습하고 있지만 항상 정확해야 하는 절대 측정값으로 의도되지 않을 때 유용합니다.

## 매개변수

* **PBR 워크플로**: *기본 색상 - 금속, 확산 - Specular*&#x200B;두 개의 다른 PBR 워크플로 사이를 전환합니다.
* **허용치**: *0.0 - 1.0*&#x200B;범위를 벗어난 값의 허용치 양.

## 예제 이미지

|  |
| --- |
| 이 페이지에 첨부된 이미지가 없습니다. |

</td>
</tr>
</table>
