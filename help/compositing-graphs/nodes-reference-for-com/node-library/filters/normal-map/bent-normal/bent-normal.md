---
helpx_url: "https://helpx.adobe.com/kr/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/normal-map/bent-normal.html"
breadcrumb-title: ''
description: 표준 구부리기 노드를 사용하면 주변 오클루전 및 간접 조명을 설명하는 표준 구부리기 맵을 생성할 수 있습니다.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Normal Map > Bent Normal
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 노멀 구부리기
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '249'
ht-degree: 2%

---


# 노멀 구부리기

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![구부러진 표준 노드 아이콘](bent-normal.resources/bent-normal-01.png "구부러진 표준 노드 아이콘")

<b>내부:</b> 필터 > 노멀 맵

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 설명

Height 맵 입력을 기반으로 [구부러진 표준 맵]을 생성합니다. 구부러진 표준 맵은 [표준](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/normal/normal.md) 및 [주변 오클루전(RTAO)](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/ambient-occlusion-rtao/ambient-occlusion-rtao.md)의 특수 버전으로, 포함된 주변 오클루전으로 표준 맵을 생성합니다.\
이는 실시간 엔진에 사용되어 앰비언트 오클루전이 일반 지도에 적용되도록 할 수 있습니다. 예를 들어 금속에 대한 오클루전 반사가 더 정확해지도록 할 수 있습니다.

이 노드는 계산 시간으로 인해 CPU(SSE) 엔진과 함께 사용하면 안 됩니다.

</td>
</tr>
</table>

<a name="parameters"></a>

## 매개변수

|  |  |
|:---|:---|
| <b>물리적 크기 사용</b> <i>부울</i> | 물리적 크기 설정을 사용하여 Height 비율을 결정하려면 전환합니다. |
| <b>물리적 크기</b> <i>Float3</i> | (<b>물리적 크기 사용</b>이(가) <i>True</i>(으)로 설정된 경우 사용 가능) 표면의 실제 물리적 크기를 기준으로 Height 비율을 조정합니다. |
| <b>샘플</b> <i>정수</i> | 구부러진 법선을 계산하는 데 사용되는 광선 수입니다.<br>높을수록 성능이 저하되는 대신 더 부드럽고 정확한 결과를 얻을 수 있습니다. |
| <b>Height 크기</b> <i>부동</i> | (물리적 크기 사용 이 False 로 설정된 경우 사용 가능) 높이 맵 입력 강도에 대한 승수입니다. |
| <b>배포</b> <i>정수</i> | 배포 방법을 설정합니다. 어두운 영역 쪽으로 감소되는 영향이 있습니다. |
| <b>최대 거리</b> <i>부동</i> | 폐색될 수 있는 최대 거리 광선을 설정합니다. |
| <b>스프레드 각도</b> <i>부동</i> | 주사할 광선의 확산 각도를 설정합니다. 1의 값은 완전한 반구입니다. |
| <b>표준 형식</b> <i>정수</i> | 출력의 녹색 채널을 반전합니다. |

## 예

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="bent-normal.resources/bent-normal-02.jpg" />
        </td>
    </tr>
</table>
