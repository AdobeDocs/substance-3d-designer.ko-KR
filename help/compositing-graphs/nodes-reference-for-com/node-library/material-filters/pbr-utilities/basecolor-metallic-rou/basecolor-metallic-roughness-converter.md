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
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '139'
ht-degree: 1%

---


# BaseColor/Metallic/Roughness 변환기

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](basecolor-metallic-roughness-converter.resources/pbr-convert.png){width="128px"}

<b>내부:</b> 재질 필터 > PBR 유틸리티

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 설명

이 노드는 [기준 색상], [금속 색상] 및 [거칠기] 맵을 Specular/광택 모델과 같은 다른 PBR 모델 출력으로 변환합니다. 포함된 출력 대상 중 일부는 Vray, Corona, Redshift, Renderman 및 Arnold와 같은 잘 알려진 렌더링 엔진입니다.

이 기능은 대상에 다른 모델이 필요하지만 하나의 PBR 모델로 만들어진 그래프나 재질이 있는 경우 유용합니다.

</td>
</tr>
</table>

<a name="parameters"></a>

## 매개변수

|  |  |
|:---|:---|
| <b>반사 수준 입력 사용</b> <i>거짓/참</i> | 추가 입력 슬롯을 SpecularLevel 입력에 노출합니다. 변환 과정에서 이 점도 고려됩니다. |
| <b>대상</b> <i>PBR 확산/Specular/광택, Vray(GGX), Corona, Corona 1.6+, Redshift 1.x, Arnold 4(AiStandard), Arnold 4(AlSurface), RenderMan(PxrSurface)</i> | 변환 대상 모델을 설정합니다. |
