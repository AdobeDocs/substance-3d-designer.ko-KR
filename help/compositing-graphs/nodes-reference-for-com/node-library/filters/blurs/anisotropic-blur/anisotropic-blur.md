---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/blurs/anisotropic-blur.html"
breadcrumb-title: ''
description: 비등방성 흐림 효과 노드를 사용하면 동작 흐림 효과와 줄무늬 효과를 만들기 위한 방향성 흐림 효과를 적용할 수 있습니다.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Blurs > Anisotropic Blur
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 비등방성 흐림
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '133'
ht-degree: 8%

---


# 비등방성 흐림

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](anisotropic-blur.resources/anisotropic-blur-grayscale.png){width="128px"}

![](anisotropic-blur.resources/anisotropic-blur.png){width="128px"}

<b>인:</b> 필터 > 흐림 효과

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 설명

모양을 사용자 지정하는 몇 가지 설정으로 고품질의 [방향 흐림 효과](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/directional-blur/directional-blur.md)를 수행합니다. &quot;동작 흐림 효과&quot;라고도 합니다.

중요: 입력에 적합한 버전을 사용해야 합니다. [색상] 입력에는 [이방성 흐림 효과]를 사용하고, [회색 음영] 입력에는 [이방성 흐림 효과]를 사용합니다.

</td>
</tr>
</table>

<a name="parameters"></a>

## 매개변수

|  |  |
|:---|:---|
| <b>강도</b> <i>0.0 - 16.0</i> | 흐림 효과의 강도(반경)입니다. 이 값이 높을수록 흐림 효과가 더 적용됩니다. |
| <b>비등방성</b> <i>0.0 - 1.0</i> | 흐림 효과의 방향성입니다. 이 값을 0.0으로 설정하는 것은 일반 흐림 효과를 적용하는 것과 같습니다. |
| <b>각도</b> <i>0.0 - 1.0</i> | 흐림 방향의 각도를 설정합니다. |
| <b>품질</b> <i>0 - 1</i> | 내부적으로 [상자 흐림 효과](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/blur/blur.md)와 HQ 흐림 효과 사이를 전환합니다. 품질에 대한 빠른 거래. |

## 예

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="anisotropic-blur.resources/aniso-blur-example.gif" />
        </td>
    </tr>
</table>
