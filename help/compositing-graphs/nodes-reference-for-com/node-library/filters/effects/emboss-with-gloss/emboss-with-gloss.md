---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/emboss-with-gloss.html"
breadcrumb-title: ''
description: '[광택 효과 엠보스] 노드를 사용하여 텍스처에 깊이와 광택을 추가하기 위해 광택 맵이 있는 엠보싱 효과를 만들 수 있습니다.'
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Emboss With Gloss
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 광택 있는 엠보스
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '136'
ht-degree: 6%

---


# 광택 있는 엠보스

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](emboss-with-gloss.resources/emboss-with-gloss.png){width="128px"}

<b>인:</b> 필터 > 효과

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 설명

색상 및 Height 입력에 광택(Specular 반사)이 추가된 엠보싱 효과를 수행합니다. 기본적으로 Height 정보를 기반으로 이미지에 가짜 조명을 추가합니다. 텍스처에 구운 조명이 필요한 일부 텍스처링 스타일에 유용합니다.

더 많은 옵션이 있는 버전을 보려면 [Uber 엠보스](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/uber-emboss/uber-emboss.md)을 참조하세요. [엠보스](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/emboss/emboss.md)의 간단한 원자 버전도 있습니다.

</td>
</tr>
</table>

<a name="inputs"></a>

## 입력

|  |  |
|:---|:---|
| <b>색상</b> <i>색상 입력</i> |  |
| <b>Height</b> <i>회색 음영 입력</i> |  |

<a name="parameters"></a>

## 매개변수

|  |  |
|:---|:---|
| <b>강조 색상</b> <i>(색상 값)</i> | Specular 강조 표시의 색상입니다. |
| <b>그림자 색상</b> <i>(색상 값)</i> | 어두운 영역/밝지 않은 영역에서 사용되는 색상입니다. |
| <b>광택</b> <i>0.0 - 0.5</i> | 광택도 강조 크기. |
| <b>강도</b> <i>0.0 - 10.0</i> | 밝은 영역의 강도입니다. |
| <b>조명 각도</b> <i>0.0 - 1.0</i> | (가짜) 빛의 입사각입니다. |
