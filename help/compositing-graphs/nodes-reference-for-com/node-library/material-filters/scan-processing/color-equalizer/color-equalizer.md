---
helpx_url: "https://helpx.adobe.com/kr/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/scan-processing/color-equalizer.html"
breadcrumb-title: ''
description: 일관된 텍스처 모양을 위해 스캔한 재료의 색상 변화 균형을 맞추기 위해 Color Equalizer 노드를 사용합니다.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > Scan Processing > Color Equalizer
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Color Equalizer
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '354'
ht-degree: 1%

---


# Color Equalizer

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/color-equalizer.png){width="128px"}

## Color Equalizer

**내부:** *재질 필터/스캔 처리*

**복합**

</td>
<td style="border: 0;" valign="top">

## 설명

이 노드는 색상 차이에 대해 고품질 [하이패스](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/highpass/highpass.md)처럼 작동합니다. 일반 하이패스가 채도를 제거하고 원치 않는 선명도를 추가할 수 있는 경우, Color Equalizer을 통해 야간 색상 차이 및 사용자 선택 가능한 비율로 원치 않는 색조를 제거할 수 있습니다.

이는 사진 또는 스캔에 원치 않는 색상 차이가 있거나 제거하려는 색조가 있는 경우 매우 유용합니다. [하이패스](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/highpass/highpass.md)를 사용한 경우 이 노드는 친숙하게 느껴집니다.

마스크 옵션은 매우 특정한 색조를 제거하거나 특정 값 범위에서만 작업하기 위한 것입니다. 효과가 너무 광범위하다고 생각되면 사용하십시오.

## 매개변수

### 입력

* **입력**: *색상 입력*
* **마스크 입력**: *회색 음영 입력*\
  노드의 효과를 마스킹하는 데 사용되는 마스크 슬롯입니다. 마스크가 &#39;입력&#39;으로 설정된 경우에만 활성화됩니다.

### 매개변수

* **바둑판식 입력**: *False/True*&#x200B;선택적으로 가장자리에 바둑판식 배열을 유지합니다.
* **반경**: *0.0 - 50.0*&#x200B;균일화 반경을 설정합니다. 반경이 클수록 큰 색상 차이만 제거됩니다. 이를 위해서는 모든 이미지에 대한 수정이 필요합니다.
* **밝음/어두운 균형**: *0.0 - 1.0*&#x200B;더 어두운 색조를 남거나 제거하기 위한 편향 설정.
* **사용자 지정 색상 변형**: *False/True*&#x200B;사용자가 지정한 색상으로 효과를 변경할 수 있습니다.
* **색상 변형**\
  사용자 정의 색상 변형이 활성화된 경우에만 활성화됩니다. 설정을 사용하여 색조 오프셋을 선택하여 균일화할 수 있습니다.
  * **색조**: *0.0 - 360.0*
  * **크로마**: *0.0 - 1.0*
  * **루마**: *0.0 - 1.0*
* **마스크 소스**: *없음, 이미지 평균, 색상 매개 변수, 입력*&#x200B;어떤 종류의 마스크가 발생할지 설정합니다. [색상 매개 변수]를 사용하면 아래의 추가 설정을 사용할 수 있습니다. [입력]은 사용자 정의 마스크 입력으로 전환됩니다.
* **마스크**\
  이는 색상 매개 변수 마스크에서만 활성화됩니다. 이미지 자체를 기반으로 마스크를 결정하는 추가 마스크 매개 변수입니다. 아래 매개 변수를 사용하면 색조를 균일화가 적용되는 이진 마스크로 정확하게 변환할 수 있습니다. 이러한 설정을 사용하면 Radius 매개 변수의 효과가 훨씬 뚜렷하게 나타나지 않을 수 있습니다.
  * **색상**: *(색상 값)*
  * **색조 범위**: *0.0 - 360.0*
  * **크로마 범위**: *0.0 - 1.0*
  * **루마 범위**: *0.0 - 1.0*
  * **흐림 효과**: *0.0 - 2.0*
  * **Smoothness**: *0.0 - 2.0*

## 예제 이미지

|  |
| --- |
| 이 페이지에 첨부된 이미지가 없습니다. |

</td>
</tr>
</table>
