---
helpx_url: "https://helpx.adobe.com/kr/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/uber-emboss.html"
breadcrumb-title: ''
description: Uber 엠보스 노드를 사용하여 사용자 정의 가능한 깊이, 각도 및 조명 컨트롤로 고급 엠보스 효과를 만들 수 있습니다.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Uber Emboss
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 우버 엠보스
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '164'
ht-degree: 9%

---


# 우버 엠보스

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](uber-emboss.resources/uber-emboss.png){width="128px"}

<b>인:</b> 필터 > 효과

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 설명

[엠보스](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/emboss/emboss.md)의 기능이 풍부한 고급 버전입니다. Heightmap을 기반으로 정교한 2D 가짜 조명 효과를 수행합니다.

많은 제어가 필요한 경우 특정 텍스처링 스타일에 적합한 추가 조명을 만들 때 유용합니다.

</td>
</tr>
</table>

<a name="inputs"></a>

## 입력

|  |  |
|:---|:---|
| <b>색상</b> <i>색상 입력</i> | 수정할 기본 이미지 |
| <b>Height</b> <i>회색 음영 입력</i> | Heightmap이 효과의 드라이버로 사용됩니다. |

<a name="parameters"></a>

## 매개변수

|  |  |
|:---|:---|
| <b>주변 색상</b> <i>(색상 값)</i> | 어두운 영역에서 사용되는 색상입니다. |
| <b>확산 색상</b> <i>(색상 값)</i> | 조명 영역에서 사용되는 색상입니다. |
| <b>Specular 색상</b> <i>(색상 값)</i> | Specular 반사에 사용되는 색상 |
| <b>조명 강도</b> <i>0.0 - 1.0</i> | (위조된) 조명의 강도입니다. |
| <b>조명 각도</b> <i>0.0 - 1.0</i> | (가짜) 빛의 입사각 |
| <b>Specular 강도</b> <i>0.0 - 1.0</i> | Specular 반사의 강도입니다. |
| <b>Specular 광택도</b> <i>0.0 - 1.0</i> | Specular 밝은 영역의 크기입니다. |
| <b>확산 거칠음</b> <i>0.0 - 1.0</i> | 확산 조명을 계산하는 데 사용되는 거칠기입니다. |
| <b>그림자 불투명도</b> <i>0.0 - 1.0</i> | 그림자가 있는 영역의 불투명도를 혼합합니다. |

## 예

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="uber-emboss.resources/uberemboss-ex.png" />
        </td>
    </tr>
</table>
