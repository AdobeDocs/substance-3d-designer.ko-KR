---
helpx_url: "https://helpx.adobe.com/kr/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/shape-drop-shadow.html"
breadcrumb-title: ''
description: '[모양 그림자] 노드를 사용하면 모양에 그림자 효과를 추가하여 텍스처에 깊이와 차원을 만들 수 있습니다.'
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Shape Drop Shadow
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 모양 그림자
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '208'
ht-degree: 6%

---


# 모양 그림자

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](shape-drop-shadow.resources/shape-drop-shadow-01.png){width="128px"}

![](shape-drop-shadow.resources/shape-drop-shadow-02.png){width="128px"}

<b>인:</b> 필터 > 효과

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 설명

다른 2D 이미지 처리 소프트웨어에서 잘 알려진 &quot;그림자 만들기&quot; 효과를 입력 흑백 마스크(회색 음영 버전) 또는 투명도가 있는 이미지(색상 버전)에 수행합니다.

[어두운 영역](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/shadows-filter-node/shadows-filter-node.md) 효과와는 달리 전체 투명도가 적용된 이미지를 반환하므로 다른 소프트웨어에서 기대하는 것과 유사한 효과를 더 완벽하게 얻을 수 있습니다.

</td>
</tr>
</table>

<a name="parameters"></a>

## 매개변수

|  |  |
|:---|:---|
| <b>각도</b> <i>0.0 - 1.0</i> | (가짜) 빛의 입사각입니다. |
| <b>거리</b> <i>-0.5 - 0.5</i> | 그림자를 모양에서 아래로/멀리 이동합니다. |
| <b>크기</b> <i>0.0 - 1.0</i> | 그림자의 흐림/흐림 효과를 제어합니다. |
| <b>스프레드</b> <i>0.0 - 1.0</i> | [흐림] 효과를 위한 [잘라내기/임계값]을 사용하면 그림자가 더 멀리 퍼집니다. |
| <b>불투명도</b> <i>0.0 - 1.0</i> | 그림자 효과에 대한 혼합 불투명도. |
| <b>(그림자) 색상</b> <i>(색상 값)</i> | 그림자에 적용할 색상 색조입니다. |
| <b>마스크 색상</b> <i>(색상 값)(회색 음영 버전만)</i> | 투명도 매핑 출력에 사용되는 단색입니다. |
| <b>미리 곱하기</b> <i>False/True(색상 버전만)</i> | 입력을 미리 곱하기로 가정해야 하는지 여부입니다. |
| <b>미리 곱하기 출력</b> <i>거짓/참</i> | 출력을 미리 곱해야 하는지 여부입니다. |

## 예

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="shape-drop-shadow.resources/shape-drop-shadow-03.png" />
        </td>
    </tr>
</table>
