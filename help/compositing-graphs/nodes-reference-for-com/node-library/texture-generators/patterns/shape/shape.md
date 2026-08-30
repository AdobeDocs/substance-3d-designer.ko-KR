---
helpx_url: "https://helpx.adobe.com/kr/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/patterns/shape.html"
breadcrumb-title: ''
description: 모양 노드를 사용하여 Substance 3D Designer에서 패턴 및 텍스처를 만들기 위한 기본 기하학적 모양을 생성합니다.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Patterns > Shape
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 모양
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '217'
ht-degree: 6%

---


# 모양

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](shape.resources/shape-2.png){width="128px"}

<b>내부:</b> 텍스처 생성기 > 패턴

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 설명

기본 모양을 수정하는 옵션을 사용하여 다양한 절차 모양을 생성합니다. 모양은 항상 완벽하게 보간되고 고정밀입니다.

단순함에도 불구하고, 이것은 매우 유용한 노드입니다: 그것은 대부분의 절차적 하이트맵 생성의 기본 요소입니다! 기본 모양을 변형 노드와 결합하면 어떤 비트맵보다 훨씬 더 정확한 완벽한 절차의 Heightmap 모양을 만들 수 있습니다.

</td>
</tr>
</table>

<a name="parameters"></a>

## 매개변수

|  |  |
|:---|:---|
| <b>타일링</b> <i>1 - 16</i> | 결과가 바둑판식으로 표시될 횟수를 설정합니다. |
| <b>패턴</b> <i>정사각형, 디스크, 포물면, 벨, 가우스, 가시, 피라미드, 벽돌, 그라데이션, 파도, 하프 벨, 고정된 벨, 크레산트, 캡슐, 원뿔, 반구</i> | 사용할 패턴 모양을 선택합니다. |
| <b>패턴별</b> <i>0.0 - 1.0</i> | 선택한 패턴의 모양을 변경할 수 있습니다. 효과는 선택한 패턴에 따라 달라집니다. |
| <b>크기 조절</b> <i>0.0 - 1.0</i> | 전체 모양의 크기를 조절합니다. |
| <b>크기</b> <i>0.0 - 1.0</i> | X축 또는 Y축에 대해 균일하지 않은 배율 조정을 허용합니다. |
| <b>각도</b> <i>0.0 - 1.0</i> | 전체 모양을 회전합니다. |
| <b>회전 45°</b> <i>거짓/참</i> | 미리 설정된 45도로 회전합니다. |
| <b>비정사각형 확장</b> <i>거짓/참</i> | 제곱이 아닌 비율로 스쿼시와 스트레치를 보정할 수 있습니다. |
| <b>정사각형이 아닌 타일링</b> <i>거짓/참</i> | 비정사각형 확장 를 활성화하면 모양을 강제로 병합하지 않고 타일링합니다. |

## 예

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="shape.resources/shape-ex.gif" />
        </td>
    </tr>
</table>
