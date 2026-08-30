---
helpx_url: "https://helpx.adobe.com/kr/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/transforms/clone-filter-node.html"
breadcrumb-title: ''
description: 복제 필터 노드를 사용하면 매끄러운 패턴 및 타일링 효과를 내기 위해 텍스처 영역을 복제하고 오프셋할 수 있습니다.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Transforms > Clone (Filter Node)
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 복제(필터 노드)
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '179'
ht-degree: 4%

---


# 복제(필터 노드)

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](clone-filter-node.resources/clone-4.png)

<b>필터</b>:

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 설명

복제 입력 이미지를 지정한 위치로 한 번 이동합니다. 조잡한 &quot;복제 도장&quot; 도구로 작동할 수 있습니다.

원하는 결과를 얻기 위해 약간의 주의가 필요합니다.

* 블렌드는 직선 복사본이므로 입력 이미지에는 데칼과 같은 알파 채널이 있는 것이 좋습니다.
* 마스크는 기본적으로 검은색으로 설정되므로 결과를 보려면 균일한 흰색 회색 음영 값을 적어도 플러깅해야 합니다.
* [오프셋]은 이미지 바깥쪽을 쉽게 클리핑하므로 작은 값을 사용합니다.

</td>
</tr>
</table>

<a name="inputs"></a>

## 입력

|  |  |
|:---|:---|
| <b>원본</b> <i>색상 입력</i> | 복제할 이미지입니다. 중요: 이미지에 알파 채널이 있는 것이 이상적입니다! |
| <b>마스크</b> <i>회색 음영 입력</i> | 노드의 효과를 마스킹하는 데 사용되는 마스크 슬롯입니다. 기본적으로 검정으로 설정됩니다! |

<a name="parameters"></a>

## 매개변수

|  |  |
|:---|:---|
| <b>오프셋</b> <i>-</i> | 결과를 이동하거나 변환합니다. 양성은 왼쪽 위, 음성은 오른쪽 아래 작은 값을 사용하면 1.0 이상으로 설정하면 이미지 밖으로 이동합니다! |
| <b>흐림 효과 마스크</b> <i>0.0 - 10.0</i> | 마스크에 흐림 효과 필터를 적용하여 가장자리를 부드럽게 합니다. |

## 예

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="clone-filter-node.resources/clone-example.png" />
        </td>
    </tr>
</table>
