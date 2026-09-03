---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/rt-shadow.html"
breadcrumb-title: ''
description: RT 그림자 노드를 사용하여 동적 조명 효과를 생성하기 위해 형상에서 실시간 그림자 정보를 계산합니다.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > RT Shadows
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: RT 그림자
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '306'
ht-degree: 0%

---


# RT 그림자

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![RT 그림자 노드 아이콘](rt-shadow.resources/rt-shadow-01.png "RT 그림자 노드 아이콘")

<b>인:</b> 필터 > 효과

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 설명

Height 맵 입력에서 광선 추적형 그림자를 생성합니다.

이 노드는 계산 시간으로 인해 CPU(SSE) 엔진과 함께 사용하면 안 됩니다.

</td>
</tr>
</table>

<a name="parameters"></a>

## 매개변수

|  |  |
|:---|:---|
| <b>샘플</b> <i>정수</i> | 그림자를 계산하는 데 사용되는 광선 수입니다.<br>값이 높을수록 성능이 저하되므로 더 부드럽고 정확한 결과를 얻을 수 있습니다. |
| <b>모드</b> <i>정수</i> | 표면에 그림자를 그리는 방법입니다. |
| <b>Height 크기</b> <i>부동</i> | 입력 Height 맵의 강도에 대한 승수입니다. |
| <b>조명 위치</b> <i>Float2</i> | 표면을 둘러싸는 구의 광원 위치:<br><br>- <b>X</b>: 수평 위치, 회전 수;<br>- <b>Y</b>: 수직 위치. 여기서 0.5는 정점이고 0/1은 수평선입니다. |
| <b>조명 강도</b> <i>부동</i> | 광원의 강도입니다. |
| <b>조명 크기</b> <i>Float2</i> | (<b>모드</b>가 <i>음영</i>(으)로 설정된 경우 사용 가능) 광원의 크기가 사각형입니다. |
| <b>조명 비율(부드러운 그림자)</b> <i>부동</i> | 광선 방향에 대한 <b>조명 크기</b>의 기여도에 대한 승수입니다.<br>값이 높을수록 그림자가 더 매끄러워집니다. |
| <b>수평선 위에 빛 유지</b> <i>부울</i> | 수평선 아래에 조명을 배치하는 방식으로 <b>조명 위치</b>를 설정하면 이 매개 변수는 조명이 해당 임계값을 넘지 않도록 합니다. 즉, Y 값이 [0;1] 범위로 고정되어 있습니다. |
| <b>그림자 불투명도</b> <i>부동</i> | 표면에 그려진 그림자의 불투명도에 대한 승수입니다. |
| <b>그림자 감쇠</b> <i>부동</i> | 그림자 감쇠의 승수는 해당 캐스터와 멀리 떨어져 있습니다.<br>값이 0이면 부드러운 그림자가 계속 적용되어 균일한 그림자가 만들어집니다. |
| <b>최대 그림자 길이</b> <i>부동</i> | 캐스터로부터 그림자가 그려질 수 있는 최대 거리입니다.<br>값이 0이면 그림자가 보이지 않습니다. |

## 예

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="rt-shadow.resources/rt-shadow-02.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="rt-shadow.resources/rt-shadow-03.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="rt-shadow.resources/rt-shadow-04.jpg" />
        </td>
    </tr>
</table>
