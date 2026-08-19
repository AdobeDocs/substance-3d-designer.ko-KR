---
helpx_url: "https://helpx.adobe.com/kr/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/pbr-utilities/basecolor-metallic-roughness-converter.html"
breadcrumb-title: ''
description: BaseColor 금속 거칠음 변환기 노드를 사용하여 다양한 PBR 재질 형식과 작업 과정 간에 변환할 수 있습니다.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > PBR Utilities > BaseColor  Metallic  Roughness converter
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: BaseColor 금속 거칠음 변환기
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '153'
ht-degree: 1%

---


# BaseColor/Metallic/Roughness 변환기

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/pbr-convert.png){width="128px"}

## BaseColor/Metallic/Roughness 변환기

**내부:** *재질 필터/PBR 유틸리티*

**단순**

</td>
<td style="border: 0;" valign="top">

## 설명

이 노드는 [기준 색상], [금속 색상] 및 [거칠기] 맵을 Specular/광택 모델과 같은 다른 PBR 모델 출력으로 변환합니다. 포함된 출력 대상 중 일부는 Vray, Corona, Redshift, Renderman 및 Arnold와 같은 잘 알려진 렌더링 엔진입니다.

이 기능은 대상에 다른 모델이 필요하지만 하나의 PBR 모델로 만들어진 그래프나 재질이 있는 경우 유용합니다.

## 매개변수

* **SpecularLevel 입력 사용**: *False/True* SpecularLevel 입력에 추가 입력 슬롯을 노출합니다. 변환 과정에서 이 점도 고려됩니다.
* ***대상**: *PBR 확산/Specular/광택, Vray(GGX), 코로나, 코로나 1.6+, Redshift 1.x, Arnold 4(AiStandard), Arnold 4(AlSurface), RenderMan(PxrSurface)**변환 대상 모델을 설정합니다.

## 예제 이미지

|  |
| --- |
| 이 페이지에 첨부된 이미지가 없습니다. |

</td>
</tr>
</table>
