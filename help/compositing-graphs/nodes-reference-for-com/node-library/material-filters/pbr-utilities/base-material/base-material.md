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
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '357'
ht-degree: 6%

---


# 기본 재질

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](base-material.resources/pbr-base-material.png){width="128px"}

<b>내부:</b> 재질 필터 > PBR 유틸리티

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 설명

[Adobe Substance 3D Designer](https://www.adobe.com/kr/products/substance3d-designer.html)에서 다중 채널 재질을 만드는 가장 빠르고 쉬운 방법입니다. 이 노드는 단순한 단색 설정 및 값을 기반으로 번들로 제공되는 전체 재질을 반환합니다. 자리 표시자로 사용하거나 복잡한 재질을 세밀하게 조정할 수 있습니다.

노드는 전체 소품을 텍스처링하고 여러 재질을 혼합할 때 매우 유용합니다. 사실 복잡한 물질 기반이 없어도 이 노드에서 모든 물질을 시작할 수 있습니다.

</td>
</tr>
</table>

<a name="inputs"></a>

## 입력

|  |  |
|:---|:---|
|  | &quot;사용자 정의 입력&quot;에서 스위치를 사용하여 전환할 수 있는 모든 채널에 대한 선택적 입력입니다. |

<a name="parameters"></a>

## 매개변수

|  |  |
|:---|:---|
| <b>PBR 워크플로</b> <i>금속 - 거칠음, Specular - 광택도</i> | 사용된 PBR 모델을 설정합니다. |
| <b>재질 사전 설정</b> <i>사용자 정의, 유전체, 금, 은, 알루미늄, 철, 구리, 티타늄, 니켈, 코발트, 백금</i> | 특정 금속을 만들기 위한 빠른 단축키. 관련 없는 옵션을 비활성화합니다. |
| <b>기본 색상</b> <i>(색상 값)</i> | 기본 색상에 사용되는 단색입니다. |
| <b>금속</b> <i>(회색 음영 값)</i> | 금속에 사용되는 실선 값입니다. |
| <b>확산 색상</b> <i>(색상 값)</i> | 확산에 사용되는 단색입니다. |
| <b>Specular</b> <i>(색상 값)</i> | Specular에 사용되는 단색입니다. |
| <b>Specular 사전 설정</b> <i>플라스틱, 나무, 돌, 벽돌, 모래, 콘크리트, 직물, 녹슨 금속, 물, 얼음, 유리</i> | 빠른 사전 설정(선택 사항)을 사용하여 PBR 교정 Specular 값을 설정합니다. |
| <b>Specular 범위</b> <i>0.0 - 1.0</i> | Specular 범위를 조정합니다. |
| <b>거칠음 - 광택도</b> |  |
| <b>거칠기 값</b> <i>(회색 음영 값)</i> | 채널이 활성화된 경우 기본 거칠기 값을 설정합니다. |
| <b>광택도 값</b> <i>(회색 음영 값)</i> | 채널이 활성화된 경우 광택도에 사용되는 단색입니다. |
| <b>그런지 양</b> <i>0.0 - 1.0</i> | 선택적 그런지 맵 입력을 [광택] 또는 [거칠음]에 혼합하는 정도입니다. |
| <b>그런지 타일링</b> <i>1 - 16</i> | 선택적 그런지 맵을 바둑판식으로 배열할 범위입니다. |
| <b>사용자 지정 그런지 입력</b> <i>거짓/참</i> | 선택적 사용자 정의 그런지 맵 을 활성화하거나 비활성화합니다. |
| <b>표준</b> |  |
| <b>Height 강도에서 표준</b> <i>0.0 - 16.0</i> | 선택적으로 사용자 정의 Heightmap을 normal로 변환하고 이를 재질 Normalmap으로 반환합니다. |
| <b>Height</b> |  |
| <b>Height 위치</b> <i>0.0 - 1.0</i> | Height 출력에 사용되는 단색 값입니다. |
| <b>Height 범위</b> <i>0.0 - 1.0</i> | 활성화된 경우 사용자 정의 Heightmap의 영향을 설정합니다. |
| <b>사용자 정의 맵</b> | 모든 사용자 정의 맵을 켜거나 끄고 실선 값 대신 표시합니다. |
