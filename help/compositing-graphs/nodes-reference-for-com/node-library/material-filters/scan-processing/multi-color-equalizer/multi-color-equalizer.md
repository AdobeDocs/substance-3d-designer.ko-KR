---
helpx_url: "https://helpx.adobe.com/kr/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/scan-processing/multi-color-equalizer.html"
breadcrumb-title: ''
description: 여러 Color Equalizer 채널에 걸쳐 색상을 균일화하여 일관된 스캔 재질 처리를 위해 [다중 텍스처] 노드를 사용합니다.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > Scan Processing > Multi Color Equalizer
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 다중 Color Equalizer
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '314'
ht-degree: 7%

---


# 다중 Color Equalizer

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](multi-color-equalizer.resources/color-equalizer-multi.png){width="128px"}

<b>내부:</b> 재질 필터 > 스캔 처리

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 설명

[Color Equalizer](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/color-equalizer/color-equalizer.md)의 다중 입력 버전입니다. 색상 차이를 완화하고 사용자가 선택할 수 있는 비율로 원치 않는 색조를 제거합니다. 주로 다각 사진에 사용하기 위한 것으로, 다각 사진은 [알베도에 대한 다각](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/multi-angle-to-albedo/multi-angle-to-albedo.md) 또는 [보통 사진에 대한 다각](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/multi-angle-to-normal/multi-angle-to-normal.md)과 결합됩니다.

>[!NOTE]
>
> 자세한 내용은 원본 [Color Equalizer](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/color-equalizer/color-equalizer.md)를 참조하세요.

</td>
</tr>
</table>

<a name="inputs"></a>

## 입력

|  |  |
|:---|:---|
| <b>입력 1-8</b> <i>색상 입력</i> | 처리할 다중 입력입니다. |
| <b>마스크 입력</b> <i>회색 음영 입력</i> | 노드의 효과를 마스킹하는 데 사용되는 마스크 슬롯입니다. |

<a name="parameters"></a>

## 매개변수

|  |  |
|:---|:---|
| <b>입력 수</b> <i>1 - 8</i> | 병렬로 처리할 입력 수를 설정합니다. |
| <b>바둑판식 입력</b> <i>거짓/참</i> | 원할 경우 가장자리의 타일링을 유지합니다. |
| <b>반경</b> <i>0.0 - 50.0</i> | 균일화 반경을 설정합니다. 반경이 클수록 큰 색상 차이만 제거됩니다. 이를 위해서는 모든 이미지에 대한 수정이 필요합니다. |
| <b>밝은/어두운 균형</b> <i>0.0 - 1.0</i> | 어두운 색조를 유지하거나 제거하기 위한 편향 설정. |
| <b>사용자 지정 색상 변형</b> <i>거짓/참</i> | 사용자가 지정한 색상으로 효과를 변경할 수 있습니다. |
| <b>색상 변형</b> | 사용자 정의 색상 변형이 활성화된 경우에만 활성화됩니다. 설정을 사용하여 색조 오프셋을 선택하여 균일화할 수 있습니다. |
| <b>색조</b> <i>0.0 - 360.0</i> |  |
| <b>크로마</b> <i>0.0 - 1.0</i> |  |
| <b>루마</b> <i>0.0 - 1.0</i> |  |
| <b>마스크 원본</b> <i>없음, 이미지 평균, 색상 매개 변수, 입력</i> | 마스크를 적용할지 여부를 설정합니다. [색상 매개 변수]를 사용하면 아래에서 추가 설정을 사용할 수 있으며 [입력]이 사용자 정의 마스크 입력으로 전환됩니다. |
| <b>마스크</b> | 색상 매개 변수 마스크가 있는 경우에만 활성화됩니다. 이미지 자체를 기반으로 마스크를 결정하는 추가 마스크 매개 변수를 포함합니다. 아래 매개 변수를 사용하면 색조를 균일화가 적용되는 이진 마스크로 정확하게 변환할 수 있습니다. 이러한 설정을 사용하면 Radius 매개 변수의 효과가 훨씬 뚜렷하게 나타나지 않을 수 있습니다. |
| <b>색상</b> <i>(색상 값)</i> |  |
| <b>색조 범위</b> <i>0.0 - 360.0</i> |  |
| <b>크로마 범위</b> <i>0.0 - 1.0</i> |  |
| <b>루마 범위</b> <i>0.0 - 1.0</i> |  |
| <b>흐림 효과</b> <i>0.0 - 2.0</i> |  |
| <b>Smoothness</b> <i>0.0 - 2.0</i> |  |
