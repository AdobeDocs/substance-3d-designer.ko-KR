---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/patterns/polygon-1.html"
breadcrumb-title: ''
description: 다각형 1 노드를 사용하여 기하학적 텍스처의 면 및 속성을 사용자 정의할 수 있는 기본 다각형 패턴을 생성합니다.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Patterns > Polygon 1
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 다각형 1
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '195'
ht-degree: 7%

---


# 다각형 1

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](polygon-1.resources/polygon-1-1.png){width="128px"}

<b>내부:</b> 텍스처 생성기 > 패턴

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 설명

다양한 조정 옵션을 사용하여 다각형 모양을 생성합니다. 더 간단한 버전은 [다각형 2](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/polygon-2/polygon-2.md)을 참조하세요.

</td>
</tr>
</table>

<a name="parameters"></a>

## 매개변수

|  |  |
|:---|:---|
| <b>면</b> <i>3 - 32</i> | 다각형이 가져야 하는 면의 양을 설정합니다. |
| <b>분해</b> <i>0.0 - 1.0</i> | 다각형 &quot;슬라이스&quot;를 따로 이동합니다. |
| <b>삼각형 크기</b> <i>0.0 - 1.0</i> | 분할 영역/삼각형의 크기를 조정합니다. 어떤 조정이든 모양을 분리할 수 있으며 이는 1,1개에 불과합니다. 이(가) 완벽하게 연결되었습니다! |
| <b>크기 조절</b> <i>0.0 - 1.0</i> | 전체 모양의 크기를 하나로 조절합니다. |
| <b>자동 크기 조정</b> <i>거짓/참</i> | 기본 매개 변수를 사용하여 전체 다각형이 보기에 맞도록 비율을 조정합니다. |
| <b>회전</b> <i>0.0 - 1.0</i> | 전체 모양을 회전합니다. |
| <b>그레이디언트</b> <i>거짓/참</i> | 단색 대신 그라디언트 분할 영역/삼각형을 생성합니다. 참고: 이 설정이 활성화된 경우 다각형 2와 비슷해집니다. |
| <b>그레이디언트 반전</b> <i>거짓/참</i> | &quot;그레이디언트&quot;가 활성화된 경우 그레이디언트 방향을 뒤집습니다. |
| <b>타일링</b> <i>1 - 16</i> | 결과가 바둑판식으로 표시될 횟수를 설정합니다. |
| <b>비정사각형 확장</b> <i>거짓/참</i> | 제곱이 아닌 비율로 스쿼시와 스트레치를 보정할 수 있습니다. |
| <b>정사각형이 아닌 타일링</b> <i>거짓/참</i> | 비정사각형 확장 를 활성화하면 모양을 강제로 병합하지 않고 타일링합니다. |

## 예

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="polygon-1.resources/polygon-1-ex.gif" />
        </td>
    </tr>
</table>
