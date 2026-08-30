---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/pbr-utilities/pbr-dielectric-f0.html"
breadcrumb-title: ''
description: PBR Dielectric F0 노드를 사용하여 물리적 기반 재료 워크플로우에 대한 유전체 F0 값을 계산합니다.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > PBR Utilities > PBR Dielectric F0
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: PBR 유전체 F0
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '112'
ht-degree: 5%

---


# PBR 유전체 F0

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](pbr-dielectric-f0.resources/pbr-dielectric-f0.png){width="128px"}

<b>내부:</b> 재질 필터 > PBR 유틸리티

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 설명

Specular PBR 모델을 사용할 때 Specular 값에 대한 유틸리티 &quot;사전 설정&quot; 노드.

정확한 값을 시작점으로 빠르게 가져와 차트에서 색상을 선택하지 않도록 하는 데 유용합니다.

</td>
</tr>
</table>

<a name="parameters"></a>

## 매개변수

|  |  |
|:---|:---|
| <b>Specular F0</b> <i>플라스틱, 나무, 돌, 벽돌, 모래, 콘크리트, 직물, 녹슨 금속, 물, 얼음, 유리, 맞춤 IOR</i> | 미리 정의된 Specular 범위를 선택합니다. |
| <b>Specular 범위</b> <i>0.01 - 1.0</i> | 선택한 사전 설정의 범위 내에서 Specular 값을 조정합니다. 약간의 수정이 허용됩니다. |
| <b>IOR</b> <i>1.0 - 5.0</i> | 사용자 정의 IOR로 설정된 경우에만 활성화됩니다. 자신의 가치를 선택합니다. |
