---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/transforms/symmetry-slice.html"
breadcrumb-title: ''
description: 대칭 슬라이스(Slide Slice) 노드를 사용하면 대칭복사된 패턴과 효과를 생성하기 위해 대칭 축을 따라 텍스처를 슬라이스할 수 있습니다.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Transforms > Symmetry Slice
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 대칭 슬라이스
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '143'
ht-degree: 6%

---


# 대칭 슬라이스

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](symmetry-slice.resources/mirror-2.png){width="128px"}

<b>필터</b>:

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 설명

복잡한 대칭/미러링 작업 노드입니다. 전체 제어를 통해 다양한 기하학적 연산을 수행할 수 있지만 몇 가지 실험적인 작업이 필요합니다.

[미러링](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/transforms/mirror-filter-node/mirror-filter-node.md) 및 [대칭](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/transforms/symmetry/symmetry.md)에 비해 이 노드에는 더 많은 옵션이 있습니다.

</td>
</tr>
</table>

<a name="parameters"></a>

## 매개변수

|  |  |
|:---|:---|
| <b>대칭 모드</b> <i>0 - 6</i> | 형상 대칭/선 대칭복사를 선택합니다. 옵션은 [가로], [세로], [왼쪽 대각선], [오른쪽 대각선], [세로 반전], [모퉁이] 및 [대각선 모퉁이]입니다. |
| <b>전송 모드</b> <i>0 - 6</i> | 혼합 모드. 옵션은 다음과 같습니다. |
| <b>혼합</b> <i>0.0 - 1.0</i> | 원본 이미지를 결과에 다시 혼합으로 맞춥니다. |
| <b>측면 뒤집기</b> <i>거짓/참</i> | 원점을 대칭 이동합니다. 즉, 작업의 원점 면이 반전됩니다. 예를 들어, 왼쪽에서 오른쪽 대칭은 오른쪽에서 왼쪽이 된다. |
| <b>측면 뒤집기2</b> <i>거짓/참</i> | 대칭 모드가 5 또는 6인 경우에만 사용됩니다. 모퉁이 원점을 뒤집습니다. |

## 예

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="symmetry-slice.resources/symslice.png" />
        </td>
    </tr>
</table>
