---
helpx_url: "https://helpx.adobe.com/kr/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/pbr-utilities/base-material.html"
breadcrumb-title: ''
description: 기본 재질 노드를 사용하여 처음부터 물리적 기반 재질을 구축하기 위한 기본 재질 속성을 만듭니다.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > PBR Utilities > Base Material
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 기본 재질
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '361'
ht-degree: 4%

---


# 기본 재질

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/pbr-base-material.png){width="128px"}

## 기본 재질

**내부:** *재질 필터/PBR 유틸리티*

**중간**

</td>
<td style="border: 0;" valign="top">

## 설명

[Adobe Substance 3D Designer](https://www.adobe.com/kr/products/substance3d-designer.html)에서 다중 채널 재질을 만드는 가장 빠르고 쉬운 방법입니다. 이 노드는 단순한 단색 설정 및 값을 기반으로 번들로 제공되는 전체 재질을 반환합니다. 자리 표시자로 사용하거나 복잡한 재질을 세밀하게 조정할 수 있습니다.

노드는 전체 소품을 텍스처링하고 여러 재질을 혼합할 때 매우 유용합니다. 사실 복잡한 물질 기반이 없어도 이 노드에서 모든 물질을 시작할 수 있습니다.

## 매개변수

### 입력

* &quot;사용자 정의 입력&quot;에서 스위치를 사용하여 전환할 수 있는 모든 채널에 대한 선택적 입력입니다.

### 매개변수

* **PBR 워크플로**: *금속 - 거칠기, Specular - 광택*&#x200B;사용되는 PBR 모델을 설정합니다.
* **재질 사전 설정**: *사용자 정의, 유전체, 금, 은, 알루미늄, 철, 구리, 티타늄, 니켈, 코발트, 백금*&#x200B;특정 금속을 만드는 빠른 단축키. 관련 없는 옵션을 비활성화합니다.
* **기본 색상**: *(색상 값)*기본 색상에 사용된 단색.
* **금속**: *(회색 음영 값)*금속에 사용되는 단색 값.
* **확산 색상**: *(색상 값)*확산에 사용되는 단색.
* **Specular**: *(색상 값)*단색을 Specular에 사용했습니다.
* **Specular 사전 설정**: *플라스틱, 나무, 돌, 벽돌, 모래, 콘크리트, 직물, 녹슨 금속, 물, 얼음, 유리* PBR 교정 Specular 값을 설정하는 빠른 사전 설정(옵션).
* **Specular 범위**: *0.0 - 1.0* Specular 범위를 조정합니다.
* **거칠음 - 광택**
  * **거칠기 값**: *(회색 음영 값)*채널이 활성화되어 있는 경우 기본 거칠기 값을 설정합니다.
  * **광도 값**: *(회색 음영 값)*채널이 활성화된 경우 광도에 단색을 사용합니다.
  * **그런지 양**: *0.0 - 1.0*&#x200B;선택적 그런지 맵 입력을 광택 또는 거칠기에 혼합하는 범위입니다.
  * **그런지 타일링**: *1 - 16*&#x200B;선택적 그런지 맵을 타일링할 범위입니다.
  * **사용자 지정 그런지 입력**: *False/True*&#x200B;선택적 사용자 지정 그런지 맵을 사용하거나 사용하지 않도록 설정합니다.
* **표준**
  * **Height 강도에서 표준**: *0.0 - 16.0*&#x200B;선택적으로 사용자 지정 Heightmap을 표준으로 변환하고 재질 Normalmap으로 반환합니다.
* **Height**
  * **Height 위치**: *0.0 - 1.0* Height 출력에 사용되는 실선 값.
  * **Height 범위**: *0.0 - 1.0*&#x200B;활성화된 경우 사용자 정의 Heightmap의 영향을 설정합니다.
* **사용자 정의 맵**
  * 모든 사용자 정의 맵을 켜거나 끄고 실선 값 대신 표시합니다.

## 예제 이미지

|  |
| --- |
| 이 페이지에 첨부된 이미지가 없습니다. |

</td>
</tr>
</table>
