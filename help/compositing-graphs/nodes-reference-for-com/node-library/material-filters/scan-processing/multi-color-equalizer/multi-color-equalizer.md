---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/scan-processing/multi-color-equalizer.html"
breadcrumb-title: ''
description: 다중 Color Equalizer 노드를 사용하여 여러 텍스처 채널에서 색상을 균일화하여 일관된 스캔 재질 처리를 수행할 수 있습니다.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > Scan Processing > Multi Color Equalizer
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 다중 Color Equalizer
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '322'
ht-degree: 1%

---


# 다중 Color Equalizer

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/color-equalizer-multi.png){width="128px"}

## 다중 Color Equalizer

**내부:** *재질 필터/스캔 처리*

**복합**

</td>
<td style="border: 0;" valign="top">

## 설명

[Color Equalizer](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/color-equalizer/color-equalizer.md)의 다중 입력 버전입니다. 색상 차이를 완화하고 사용자가 선택할 수 있는 비율로 원치 않는 색조를 제거합니다. 주로 다각 사진에 사용하기 위한 것으로, 다각 사진은 [알베도에 대한 다각](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/multi-angle-to-albedo/multi-angle-to-albedo.md) 또는 [보통 사진에 대한 다각](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/multi-angle-to-normal/multi-angle-to-normal.md)과 결합됩니다.

>[!NOTE]
>
> 자세한 내용은 원본 [Color Equalizer](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/color-equalizer/color-equalizer.md)를 참조하세요.

## 매개변수

### 입력

* **입력 1-8**: *색상 입력*&#x200B;처리할 여러 입력.
* **마스크 입력**: *회색 음영 입력*\
  노드의 효과를 마스킹하는 데 사용되는 마스크 슬롯입니다.

### 매개변수

* **입력 수**: *1 - 8*&#x200B;병렬로 처리할 입력 수를 설정합니다.
* **바둑판식 입력**: *False/True*&#x200B;선택적으로 가장자리에 바둑판식 배열을 유지합니다.
* **반경**: *0.0 - 50.0*&#x200B;균일화 반경을 설정합니다. 반경이 클수록 큰 색상 차이만 제거됩니다. 이를 위해서는 모든 이미지에 대한 수정이 필요합니다.
* **밝음/어두운 균형**: *0.0 - 1.0*&#x200B;더 어두운 색조를 남거나 제거하기 위한 편향 설정.
* **사용자 지정 색상 변형**: *False/True*&#x200B;사용자가 지정한 색상으로 효과를 변경할 수 있습니다.
* **색상 변형**\
  사용자 정의 색상 변형이 활성화된 경우에만 활성화됩니다. 설정을 사용하여 색조 오프셋을 선택하여 균일화할 수 있습니다.
  * **색조**: *0.0 - 360.0*
  * **크로마**: *0.0 - 1.0*
  * **루마**: *0.0 - 1.0*
* **마스크 소스**: *없음, 이미지 평균, 색상 매개 변수, 입력*&#x200B;마스크를 적용할지 여부를 설정합니다. [색상 매개 변수]를 사용하면 아래에서 추가 설정을 사용할 수 있으며 [입력]이 사용자 정의 마스크 입력으로 전환됩니다.
* **마스크**\
  색상 매개 변수 마스크가 있는 경우에만 활성화됩니다. 이미지 자체를 기반으로 마스크를 결정하는 추가 마스크 매개 변수를 포함합니다. 아래 매개 변수를 사용하면 색조를 균일화가 적용되는 이진 마스크로 정확하게 변환할 수 있습니다. 이러한 설정을 사용하면 Radius 매개 변수의 효과가 훨씬 뚜렷하게 나타나지 않을 수 있습니다.
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
