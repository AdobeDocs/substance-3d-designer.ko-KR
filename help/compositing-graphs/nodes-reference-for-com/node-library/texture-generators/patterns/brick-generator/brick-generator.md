---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/patterns/brick-generator.html"
breadcrumb-title: ''
description: '[벽돌 생성기] 노드를 사용하여 사용자 정의 가능한 크기, 오프셋 및 모르타르 속성을 가진 프로시저 벽돌 패턴을 만듭니다.'
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Patterns > Brick Generator
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 벽돌 생성기
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '211'
ht-degree: 8%

---


# 벽돌 생성기

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](brick-generator.resources/brick-generator-01.png){width="128px"}

<b>내부:</b> 텍스처 생성기 > 패턴

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 설명

고급 브릭 패턴 생성기. 특별히 인공 벽돌 패턴을 생성하기 위한 많은 옵션이 있습니다.

추가 옵션은 [Tile Generator](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/tile-generator/tile-generator.md)을 참조하세요.

</td>
</tr>
</table>

<a name="parameters"></a>

## 매개변수

|  |  |
|:---|:---|
| <b>벽돌</b> <i>1 - 64</i> | X축과 Y축 모두에서 벽돌의 양을 설정합니다. |
| <b>경사</b> <i>0.0 - 1.0</i> | 벽돌의 경사 프로파일을 변경하여 두 방향으로 변경할 수 있고 밝기 감소 프로파일 및 모퉁이 둥글게 설정할 수 있습니다. |
| <b>비율 유지</b> <i>거짓/참</i> | [경사] 프로파일을 벽돌 크기에 연결하거나 연결하지 않습니다. |
| <b>간격</b> <i>0.0 - 1.0</i> | 벽돌 사이에 남겨 둘 간격. [경사]에는 간격이 추가된다는 점에 유의하십시오. 따라서 경사를 설정해도 이 매개 변수로 보정해야 합니다. |
| <b>중간 크기</b> <i>0.0 - 1.0</i> | 벽돌 패턴 오프셋은 다른 모든 열 또는 행의 크기를 변경합니다. |
| <b>Height</b> <i>-1.0 - 1.0</i> | Height 프로필을 수정합니다. 광도 변형 및 모든 종류의 임의화를 사용할 수 있습니다. |
| <b>경사</b> <i>-1.0 - 1.0</i> | 특정 벽돌이 비스듬히 누워있는 것처럼 벽돌마다 경사를 도입합니다. |
| <b>오프셋</b> <i>0.0 - 1.0</i> | 행 기준으로 벽돌을 오프셋하고 행별 간격에 영향을 줍니다. |
| <b>비정사각형 확장</b> <i>거짓/참</i> | 사각형이 아닌 비율로 squash 및 squash를 보정할 수 있습니다. |

## 예

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="brick-generator.resources/brick-generator-02.gif" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="brick-generator.resources/brick-generator-03.gif" />
        </td>
    </tr>
</table>
