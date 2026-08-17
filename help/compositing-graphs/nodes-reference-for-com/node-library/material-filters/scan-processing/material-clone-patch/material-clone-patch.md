---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/scan-processing/material-clone-patch.html"
breadcrumb-title: ''
description: '[재질 복제 패치] 노드를 사용하여 스캔한 재질의 가공물을 복구하기 위해 텍스처 영역을 복제하고 패치합니다.'
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > Scan Processing > Material Clone Patch
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 재질 복제 패치
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '334'
ht-degree: 1%

---


# 재질 복제 패치

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/clone-patch-material.png){width="128px"}

## 재질 복제 패치

**내부:** *재질 필터/스캔 처리*

**복합**

</td>
<td style="border: 0;" valign="top">

## 설명

[복제 패치](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/clone-patch/clone-patch.md)의 다중 채널, 전체 재질 버전입니다. 재질의 모든 채널에 대해 복제 패치를 수행합니다. [자세한 내용은 원래 버전을 참조하세요!](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/clone-patch/clone-patch.md)

재질의 모든 채널에서 세부 묘사를 제거하려는 경우 매우 유용합니다. 여러 채널에 대한 디버그 이미지를 출력하여 스마트 패치 영역의 모양을 정확하게 확인합니다.

## 매개변수

### 입력

* **마스크**: *회색 음영 입력*\
  노드의 효과를 마스킹하는 데 사용되는 마스크 슬롯입니다. &quot;마스크&quot; 매개 변수로 전환할 수 있습니다.

### 매개변수

* **채널**
  * 예를 들어 [금속]/[거칠음] 대신 [Specular/광택] 맵을 사용하는 경우 이 그룹에서 재질 채널을 켜거나 끌 수 있습니다.
* **모양**: *정사각형, 디스크*&#x200B;스탬프 모양을 설정합니다. 기본으로만 사용됩니다.
* **가장자리**
  * **임계값(여러 채널의 경우)**: *0.0 - 1.0*&#x200B;혼합 영역이 도달하는 정도를 설정합니다. 이는 대상 영역의 모양을 따라 단계적으로 성장하므로 균일한 배경으로는 효과가 거의 없습니다*.*시각적 차이가 발생할 수 있으므로 채널 간에 너무 많이 변경되도록 주의하십시오!
  * **흐림**: *0.0 - 2.0*&#x200B;더 부드러운 전환이 필요한 경우 스탬프 영역의 가장자리를 흐리게 합니다.
  * **Smoothness**: *0.0 - 2.0*&#x200B;스탬프 모양의 가장자리를 둥글게 하여 더 매끄럽게 흐르는 윤곽선을 만듭니다.
  * **격자 해상도**: *1 - 11*&#x200B;혼합 분석의 품질 해상도를 설정합니다. 값이 높을수록 더 정확한 혼합을 의미합니다.
* **변환**
  * **소스 행렬**: *(변환 행렬)*소스를 변환합니다(크기 조정 및 회전). 캔버스에서는 수행할 수 없으며 이러한 매개 변수만 변경하십시오.
  * **원본 오프셋**: *-0.5 - 0.5*&#x200B;원본 위치를 변환합니다. 캔버스에서는 수행할 수 없으며 이러한 매개 변수만 변경하십시오. *이 매개 변수는 아마도 변경할 기본 매개 변수입니다!*
  * **대상 행렬**: *(변환 행렬)*대상 위치를 변환합니다(크기 및 회전). 캔버스에서 gizmo를 통해 수행할 수도 있습니다.
  * **대상 오프셋**: *-0.5 - 0.5*&#x200B;대상 위치를 변환합니다. 캔버스에서 gizmo를 통해 수행할 수도 있습니다.

## 예제 이미지

|  |
| --- |
| 이 페이지에 첨부된 이미지가 없습니다. |

</td>
</tr>
</table>
