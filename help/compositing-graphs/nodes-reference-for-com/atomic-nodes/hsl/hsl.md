---
helpx_url: "https://helpx.adobe.com/kr/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/atomic-nodes/hsl.html"
breadcrumb-title: ""
description: HSL 노드를 사용하여 색상 조작 및 교정을 위한 텍스처의 색조, 채도 및 밝기를 조정합니다.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Atomic nodes > HSL
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: HSL
user-guide-description: ""
user-guide-title: ""
source-git-commit: 11ab41b58a2dfcb6dd048c55f7a6138a003a2833
workflow-type: tm+mt
source-wordcount: '152'
ht-degree: 9%
---

# HSL

<table>
<tr style="border: 0;">
<td style="border: 0; width:33.33%; vertical-align:top" width="33.33%" valign="top">

![Atomic node: HSL](hsl.resources/comp_hsl_1.png "Atomic node: HSL"){width="100%"}

<b>내부:</b> 원자 노드

</td>
<td style="border: 0; width:66.66%; vertical-align:top" width="66.66%" valign="top">

색상 이미지의 색조, 채도 및 밝기를 조정합니다.

색상 데이터를 사용하여 작업할 때 매우 유용한 기본적이고 사용하기 쉬운 노드입니다.

이미지의 톤을 편집하는 다른 방법을 찾고 있다면 [곡선](../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/curve/curve.md), [레벨](../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/levels/levels.md) 및 [대비/광도](../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/contrast-luminosity/contrast-luminosity.md)를 확인하십시오.

</td>
</tr>
</table>

<table>
<tr style="border: 0">
<td style="border: 0; width: 15%" width="15%"></td>
<td style="border: 0; text-align: center" align="center"><img src="hsl.resources/hsl-tooltip.gif" alt="hsl 툴팁" /></td>
<td style="border: 0; width: 15%" width="15%"></td>
</tr>
</table>



## 매개변수

|  |  |
| --- | --- |
| <b>색조</b> *부동* | 입력 이미지의 색상을 결정합니다.   0.5 미만의 값은 [색조]를 음수로 이동하고, 0.5 이상의 값은 색조를 양수로 이동합니다. |
| <b>채도</b> *부동* | 입력 이미지 색상의 채도를 결정합니다.   0.5 미만의 값은 채도를 낮추고 0.5 이상의 값은 채도를 높입니다. |
| <b>밝기</b> *부동* | 입력 이미지 값의 밝기를 0.5 미만으로 결정하고, 밝기를 0.5 이상으로 하면 값을 증가시킵니다. |

## 입력 커넥터

|  |  |
| --- | --- |
| <b>입력</b> 기본 *색상* | 처리할 이미지입니다. |


## 예

*곧 출시 예정*
