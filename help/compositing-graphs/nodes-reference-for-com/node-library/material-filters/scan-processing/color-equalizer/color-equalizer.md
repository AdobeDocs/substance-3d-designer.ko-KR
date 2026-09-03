---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/scan-processing/color-equalizer.html"
breadcrumb-title: ''
description: Color Equalizer 노드를 사용하여 스캔한 재질의 색상 변화를 균형 있게 조정하여 일관된 텍스처 모양을 만들 수 있습니다.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > Scan Processing > Color Equalizer
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Color Equalizer
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '345'
ht-degree: 6%

---


# Color Equalizer

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](color-equalizer.resources/color-equalizer-01.png){width="128px"}

<b>내부:</b> 재질 필터 > 스캔 처리

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 설명

이 노드는 색상 차이에 대해 고품질 [하이패스](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/highpass/highpass.md)처럼 작동합니다. 일반 하이패스가 채도를 제거하고 원치 않는 선명도를 추가할 수 있는 경우, Color Equalizer을 통해 야간 색상 차이 및 사용자 선택 가능한 비율로 원치 않는 색조를 제거할 수 있습니다.

이는 사진 또는 스캔에 원치 않는 색상 차이가 있거나 제거하려는 색조가 있는 경우 매우 유용합니다. [하이패스](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/highpass/highpass.md)를 사용한 경우 이 노드는 친숙하게 느껴집니다.

마스크 옵션은 매우 특정한 색조를 제거하거나 특정 값 범위에서만 작업하기 위한 것입니다. 효과가 너무 광범위하다고 생각되면 사용하십시오.

</td>
</tr>
</table>

<a name="inputs"></a>

## 입력

|  |  |
|:---|:---|
| <b>입력</b> <i>색상 입력</i> |  |
| <b>마스크 입력</b> <i>회색 음영 입력</i> | 노드의 효과를 마스킹하는 데 사용되는 마스크 슬롯입니다. 마스크가 &#39;입력&#39;으로 설정된 경우에만 활성화됩니다. |

<a name="parameters"></a>

## 매개변수

|  |  |
|:---|:---|
| <b>바둑판식 입력</b> <i>거짓/참</i> | 원할 경우 가장자리의 타일링을 유지합니다. |
| <b>반경</b> <i>0.0 - 50.0</i> | 균일화 반경을 설정합니다. 반경이 클수록 큰 색상 차이만 제거됩니다. 이를 위해서는 모든 이미지에 대한 수정이 필요합니다. |
| <b>밝은/어두운 균형</b> <i>0.0 - 1.0</i> | 어두운 색조를 유지하거나 제거하기 위한 편향 설정. |
| <b>사용자 지정 색상 변형</b> <i>거짓/참</i> | 사용자가 지정한 색상에 따라 효과를 변경할 수 있습니다. |
| <b>색상 변형</b> | 사용자 정의 색상 변형이 활성화된 경우에만 활성화됩니다. 설정을 사용하여 색조 오프셋을 선택하여 균일화할 수 있습니다. |
| <b>색조</b> <i>0.0 - 360.0</i> |  |
| <b>크로마</b> <i>0.0 - 1.0</i> |  |
| <b>루마</b> <i>0.0 - 1.0</i> |  |
| <b>마스크 원본</b> <i>없음, 이미지 평균, 색상 매개 변수, 입력</i> | 어떤 종류의 마스크가 발생하는지 설정합니다. [색상 매개 변수]를 사용하면 아래의 추가 설정을 사용할 수 있습니다. [입력]은 사용자 정의 마스크 입력으로 전환됩니다. |
| <b>마스크</b> | 이는 색상 매개 변수 마스크에서만 활성화됩니다. 이미지 자체를 기반으로 마스크를 결정하는 추가 마스크 매개 변수입니다. 아래 매개 변수를 사용하면 색조를 균일화가 적용되는 이진 마스크로 정확하게 변환할 수 있습니다. 이러한 설정을 사용하면 Radius 매개 변수의 효과가 훨씬 뚜렷하게 나타나지 않을 수 있습니다. |
| <b>색상</b> <i>(색상 값)</i> |  |
| <b>색조 범위</b> <i>0.0 - 360.0</i> |  |
| <b>크로마 범위</b> <i>0.0 - 1.0</i> |  |
| <b>루마 범위</b> <i>0.0 - 1.0</i> |  |
| <b>흐림 효과</b> <i>0.0 - 2.0</i> |  |
| <b>Smoothness</b> <i>0.0 - 2.0</i> |  |
