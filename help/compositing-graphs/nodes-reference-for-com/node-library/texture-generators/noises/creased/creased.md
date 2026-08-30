---
helpx_url: "https://helpx.adobe.com/kr/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/noises/creased.html"
breadcrumb-title: ''
description: 주름진 노드를 사용하여 접힌 원단과 주름진 표면 텍스처 효과를 만들기 위한 주름 패턴을 생성합니다.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Noises > Creased
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 주름진
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '106'
ht-degree: 8%

---


# 주름진

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](creased.resources/creased.png){width="128px"}

<b>내부:</b> 텍스처 생성기 > 잡음

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 설명

이 노드는 천과 같은 노이즈를 생성합니다. Heightmap으로 해석할 수 있다

[주름진 모양]은 비율 변화가 큰 반방향 노이즈가 필요한 경우에 유용합니다.

</td>
</tr>
</table>

<a name="parameters"></a>

## 매개변수

|  |  |
|:---|:---|
| <b>크기 조절</b> <i>1 - 8</i> | 효과의 전체 배율을 설정합니다. |
| <b>뒤틀기 강도</b> <i>0.0 - 128.0</i> | 벤드/뒤틀기 효과의 강도를 설정합니다. |
| <b>장애</b> <i>0.0 - 100.0</i> | 노이즈를 생성하는 데 사용된 레이어를 약간 오프셋하여 변형을 추가합니다. |
| <b>비정사각형 확장</b> <i>거짓/참</i> | 제곱이 아닌 비율로 스쿼시와 스트레치를 보정할 수 있습니다. |

## 예

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="creased.resources/creased-ex.gif" />
        </td>
    </tr>
</table>
