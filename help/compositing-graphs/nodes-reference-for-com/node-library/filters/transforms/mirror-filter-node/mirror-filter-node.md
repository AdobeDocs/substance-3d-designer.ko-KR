---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/transforms/mirror-filter-node.html"
breadcrumb-title: ''
description: 대칭 패턴 및 효과를 만들기 위해 텍스처를 수평 또는 수직으로 대칭복사하려면 대칭복사 필터 노드를 사용합니다.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Transforms > Mirror (Filter Node)
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 미러(필터 노드)
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '148'
ht-degree: 4%

---


# 미러(필터 노드)

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](mirror-filter-node.resources/mirror-2.png){width="128px"}

![](mirror-filter-node.resources/mirror-grayscale.png){width="128px"}

<b>필터</b>:

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 설명

선택한 측면에서 선택한 축을 기준으로 입력 이미지를 미러링합니다. 대칭 효과를 얻을 수 있는 매우 유용하고 빠른 방법입니다.

</td>
</tr>
</table>

<a name="parameters"></a>

## 매개변수

|  |  |
|:---|:---|
| <b>모드</b> <i>미러링 축 X, 미러링 축 Y, 미러 모퉁이</i> | 왼쪽-오른쪽, 위쪽-아래쪽 또는 양쪽 모두를 미러링하도록 선택합니다. |
| <b>축 X 오프셋</b> <i>0.0 - 1.0</i> | 축 X를 선택한 경우에만 오프셋을 정의합니다. |
| <b>축 Y 오프셋</b> <i>0.0 - 1.0</i> | 축 Y를 선택한 경우에만 오프셋을 정의합니다. |
| <b>축 X 반전</b> <i>거짓/참</i> | 축 X를 선택한 경우에만 방향 대칭 이동 |
| <b>축 반전</b> <i>거짓/참</i> | 축 Y를 선택한 경우에만 방향 대칭 이동 |
| <b>모퉁이 유형</b> <i>왼쪽 위, 오른쪽 위, 왼쪽 아래, 오른쪽 아래</i> | 코너 유형을 선택한 경우에만 사용할 코너 유형을 정의합니다. |

## 예

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="mirror-filter-node.resources/mirror-example.png" />
        </td>
    </tr>
</table>
