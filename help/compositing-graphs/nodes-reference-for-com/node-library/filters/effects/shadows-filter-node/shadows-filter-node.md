---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/shadows-filter-node.html"
breadcrumb-title: ''
description: 그림자 필터 노드를 사용하여 입력 텍스처에서 그림자 효과를 생성하여 깊이와 사실감을 재질에 추가합니다.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Shadows (Filter Node)
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 어두운 영역(필터 노드)
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '134'
ht-degree: 8%

---


# 어두운 영역(필터 노드)

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](shadows-filter-node.resources/shadows-1.png){width="128px"}

<b>인:</b> 필터 > 효과

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 설명

Raw, 회색 음영 전용 버전의 [모양 그림자](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/shape-drop-shadow/shape-drop-shadow.md) 노드입니다. 검정색과 흰색의 이진 모양만 입력으로 사용하고 그림자만 반환합니다.

그림자 바로 뒤에 있으며 자신의 재질을 만들거나 조명을 구운 경우와 같이 더 완전한 노드로 작업하고 싶지 않을 때 유용할 수 있습니다.

</td>
</tr>
</table>

<a name="parameters"></a>

## 매개변수

|  |  |
|:---|:---|
| <b>그림자 거리</b> <i>0.0 - 1.0</i> | 그림자가 떨어질 거리를 제어합니다. |
| <b>조명 각도</b> <i>0.0 - 1.0</i> | 빛의 입사각을 제어합니다. |
| <b>가장자리 부드러움</b> <i>0.0 - 1.0</i> | 어두운 영역의 가장자리가 얼마나 단단한지 또는 부드러운지를 결정합니다. |
| <b>샘플</b> <i>1 - 16</i> | [가장자리 부드러움] 설정의 품질을 설정합니다. |

## 예

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="shadows-filter-node.resources/shadow-ex.png" />
        </td>
    </tr>
</table>
