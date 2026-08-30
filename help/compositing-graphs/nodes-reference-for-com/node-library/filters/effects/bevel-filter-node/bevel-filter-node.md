---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/bevel-filter-node.html"
breadcrumb-title: ''
description: 경사 필터 노드를 사용하면 깊이 및 치수를 추가하기 위해 모양과 패턴에 경사진 가장자리를 만들 수 있습니다.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Bevel (Filter Node)
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 경사(필터 노드)
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '204'
ht-degree: 4%

---


# 경사(필터 노드)

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](bevel-filter-node.resources/bevel.png){width="128px"}

<b>인:</b> 필터 > 효과

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 설명

입력 회색 음영 높이 맵에 가장자리 베벨링 효과를 적용합니다. 해당 Heightmap에 따라 경사진 Heightmap과 Normalmap을 모두 반환합니다.

이 노드는 이상적인 바이너리(높은 수축 흑백), 기본 Heightmap에 정확한 곡선 프로파일을 적용하는 데 유용합니다.

</td>
</tr>
</table>

<a name="inputs"></a>

## 입력

|  |  |
|:---|:---|
| <b>입력</b> <i>회색 음영 입력</i> | 변환할 Heightmap. |
| <b>사용자 지정 곡선</b> <i>회색 음영 입력</i> | 정확한 곡선/경사를 결정하는 그레이디언트입니다. [수준](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/levels/levels.md) 또는 [곡선](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/curve/curve.md)과 같은 모든 종류의 조정을 수행할 수 있는 [선형 그레이디언트] 노드입니다. &quot;사용자 정의 곡선 사용&quot;이 True인 경우에만 활성화됩니다. |

<a name="parameters"></a>

## 매개변수

|  |  |
|:---|:---|
| <b>거리</b> <i>-1.0 - 1.0</i> | 경사 효과의 도달 거리입니다. |
| <b>모퉁이 유형</b> <i>원형, Angular</i> | 경사 프로필을 둥글게 할지 직선 프로필로 할지 지정합니다. |
| <b>보정</b> <i>0.0 - 5.0</i> | 경사 후 수행할 추가 다듬기(흐림) 양입니다. |
| <b>비균일 흐림 효과 사용</b> <i>거짓/참</i> | 매끄럽게 하기 작업을 균일하지 않게 수행할지 여부를 지정합니다. |
| <b>사용자 지정 곡선 사용</b> <i>거짓/참</i> | 사용자 정의 Height 곡선 사용을 전환합니다. 자세한 내용은 위를 참조하십시오. |
| <b>표준 강도</b> <i>0.0 - 50.0</i> | 생성된 표준 맵의 강도입니다. |
| <b>표준 형식</b> <i>DirectX, OpenGL</i> | 다른 표준 맵 포맷 간에 전환합니다(녹색 채널을 반전합니다). |

## 예

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="bevel-filter-node.resources/bevel-example.png" />
        </td>
    </tr>
</table>
