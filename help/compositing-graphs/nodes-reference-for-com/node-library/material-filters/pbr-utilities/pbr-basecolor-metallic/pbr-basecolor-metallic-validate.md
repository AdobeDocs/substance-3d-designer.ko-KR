---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/pbr-utilities/pbr-basecolor-metallic-validate.html"
breadcrumb-title: ''
description: PBR BaseColor Metallic Validate 노드를 사용하여 PBR 재질에 대한 기본 색상 및 금속성 값을 검증하고 수정합니다.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > PBR Utilities > PBR BaseColor  Metallic Validate
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: PBR 기본 색상 금속 유효성 검사
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '210'
ht-degree: 0%

---


# PBR BaseColor/Metallic Validate

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/pbr-basecolor-metallic-validate.png){width="128px"}

## PBR BaseColor/Metallic Validate

**내부:** *재질 필터/PBR 유틸리티*

**단순**

</td>
<td style="border: 0;" valign="top">

## 설명

PBR 표준에 따라 값이 정확하거나 잘못된 양호 &quot;히트맵&quot;을 생성하는 유틸리티 노드입니다.

실수가 무엇인지, 어디에서 찾을 수 있는지 매우 명확한 시각적 피드백을 제공하기 때문에 PBR의 학습 도구로 매우 유용합니다.

이를 모든 것을 다 갖춘 도구로 사용하지 말고, 이 도구로 강조할 수 있는 규칙을 어기는 이유에 대해 항상 명확하게 이해하도록 하십시오.

## 매개변수

* **유효성 검사 모드**: *알베도 , Metal, 결합됨*&#x200B;알베도, Metal 또는 둘 다 개요 모드로 확인할지 여부를 설정합니다.
* **알베도 어두운 범위 임계값**: *50 sRGB, 30 sRGB*&#x200B;낮은 알베도 제한을 50 또는 30 sRGB로 설정합니다. 빨간색 영역의 허용치를 높이거나 낮출 수 있습니다.
* **금속 반사율 범위**: *70-100% 반사, 60-100% 반사*&#x200B;금속 범위가 올바른 것으로 변경됩니다. 빨간색 영역의 허용치를 높이거나 낮출 수 있습니다.
* **오버레이 맵**: *False/True*&#x200B;빠른 디버그 모드로 입력 맵을 오버레이하면 문제 영역을 더 빠르게 추적할 수 있습니다.

## 예제 이미지

|  |
| --- |
| 이 페이지에 첨부된 이미지가 없습니다. |

</td>
</tr>
</table>
