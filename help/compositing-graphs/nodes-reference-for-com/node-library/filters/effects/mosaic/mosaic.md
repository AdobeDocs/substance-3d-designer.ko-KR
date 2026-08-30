---
helpx_url: "https://helpx.adobe.com/kr/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/mosaic.html"
breadcrumb-title: ''
description: '[모자이크] 노드를 사용하면 텍스처를 픽셀화된 블록과 패턴으로 분할하여 모자이크 타일 효과를 만들 수 있습니다.'
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Mosaic
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 모자이크
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '110'
ht-degree: 7%

---


# 모자이크

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](mosaic.resources/mosaic-1.png){width="128px"}

![](mosaic.resources/mosaic-grayscale.png){width="128px"}

<b>인:</b> 필터 > 효과

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 설명

멀티패스 [뒤틀기](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/warp/warp.md) 효과를 수행하여 기존의 매끄럽고 경사진 그레이디언트 맵을 &quot;페이스티스&quot;합니다. 두 입력에 동일한 맵을 사용하면 기본적으로 가장 밝은 영역이 커지고 강조됩니다.

이 기능은 모양에 더 많은 정의를 적용할 수 있으므로 Heightmap과 같은 회색 음영 맵에 더 많은 정의를 추가하는 데 유용합니다.

</td>
</tr>
</table>

<a name="inputs"></a>

## 입력

|  |  |
|:---|:---|
| <b>색상</b> <i>색상/회색 음영 입력</i> |  |
| <b>모자이크 지도</b> <i>회색 음영 입력</i> | 드라이버 맵을 뒤틀었습니다. 첫 번째 입력과 같을 수 있습니다. |

<a name="parameters"></a>

## 매개변수

|  |  |
|:---|:---|
| <b>샘플</b> <i>0 - 16</i> | 다중 샘플 품질을 결정합니다. |
| <b>강도</b> <i>0.0 - 1.0</i> | 효과의 강도입니다. |

## 예

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="mosaic.resources/mosaci-ex.png" />
        </td>
    </tr>
</table>
