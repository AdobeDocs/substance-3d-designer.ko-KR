---
helpx_url: "https://helpx.adobe.com/kr/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/3d-view-library/hdri-tools/line-light.html"
breadcrumb-title: ''
description: HDRI 환경에서 형광 및 스트립 조명을 시뮬레이션하는 선형 광원을 생성하려면 라인 조명 노드를 사용합니다.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > 3D View (Library) > HDRI Tools > Line Light
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 라인 라이트
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '707'
ht-degree: 3%

---


# 라인 라이트

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](line-light.resources/line-light-01.png){width="200px"}

<b>내부:</b> 3D 보기 > HDRI 도구

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 설명

공간에서 두 점의 좌표를 기반으로 구형으로 투영된 선 모양을 생성합니다. [모양 조명](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/3d-view-library/hdri-tools/shape-light/shape-light.md)과 비교하여 모양의 방향을 조정하고 조명 모양에 반복 패턴을 적용하는 더 많은 옵션이 있습니다.

이 노드에 대한 포지셔닝 모드는 다른 HDRI 라이트 노드보다 약간 더 복잡하다. 몇 가지 다른 크기 모드를 시도하여 시나리오에 적합한 모드를 찾는 것이 좋습니다.

</td>
</tr>
</table>

<a name="inputs"></a>

## 입력

|  |  |
|:---|:---|
| <b>배경 이미지 입력</b> <i>색상 입력</i> | 생성된 빛을 구성할 선택적 배경입니다. |
| <b>모양 이미지 입력</b> <i>색상 입력</i> | 라인 조명에 매핑할 선택적 이미지입니다. [모양 색상 모드]가 [이미지 입력]으로 설정된 경우에만 사용됩니다. |
| <b>패턴 이미지 입력</b> <i>회색 음영 입력</i> | &quot;Pattern&quot; 매개 변수를 &quot;Image Input&quot;으로 설정한 경우 사용되는 사용자 정의 패턴 이미지입니다. |

<a name="parameters"></a>

## 매개변수

|  |  |
|:---|:---|
| <b>위치 모드</b> <i>지상/천장, 원점으로부터의 거리, 세계 위치</i> | 세 가지 배치 모드 중에서 선택합니다. 2D 보기에서 바닥/천장 및 원점으로부터의 거리 지원 조작, 세계 위치는 속성을 통해서만 변경할 수 있지만 더 정확한 배치를 지원합니다. |
| <b>지표 격자 표시</b> <i>거짓/참</i> | 디버그 그라운드 그리드를 그릴 수 있도록 하는 도우미 함수입니다. 공간에서 선의 위치를 추정하는 데 도움이 됩니다. |
| <b>위치 좌표</b> |  |
| <b>위쪽 벡터</b> <i>Z 위로, Y 위로</i> | 세계 위치 모드에서만 좌표계의 방향을 결정합니다. |
| <b>포인트 1 UV 위치</b> | 바닥 / 천장 및 원점으로부터의 거리가 있어야합니다. UV 공간에서 첫 번째 점 위치를 설정합니다. |
| <b>포인트 2 UV 위치</b> | 바닥 / 천장 및 원점으로부터의 거리가 있어야합니다. UV 공간에서 두 번째 점 위치를 설정합니다. |
| <b>포인트 1 세계 위치</b> <i>-2.0 - 2.0</i> | 월드 포지션 모드만 사용 가능. 월드 공간의 첫 번째 점을 설정합니다. 지원되는 2D 보기 상호 작용이 없습니다. |
| <b>포인트 2 세계 위치</b> <i>-2.0 - 2.0</i> | 월드 포지션 모드만 사용 가능. 월드 공간에서 두 번째 지점을 설정합니다. 지원되는 2D 보기 상호 작용이 없습니다. |
| <b>선 절대 Height</b> <i>0.0 - 1.0</i> | 지표/천장 위치 모드에서만 천장으로부터 절대 Height을 설정합니다. 위치를 더 잘 추정하려면 [지표 격자 표시]를 사용합니다. |
| <b>원점으로부터의 거리</b> <i>0.0 - 1.0</i> | 원점으로부터의 거리 위치 모드에서만 가능합니다. 두 점의 파노라마 중심으로부터의 거리를 설정합니다. |
| <b>모양 색상 모드</b> <i>RGB, 온도(켈빈), 이미지 입력</i> | 모양 색상을 설정하는 데 사용할 방법을 선택합니다. 이미지 입력(Image Input)은 두 번째 입력 슬롯을 사용할 수 있게 합니다. |
| <b>색상</b> <i>(색상 값)</i> | [모양 색상 모드]가 [RGB]로 설정된 경우에만 가능합니다. 모양의 색상을 선택합니다. |
| <b>온도</b> <i>800.0 - 20000.0</i> | [모양 색상 모드]가 [온도]로 설정된 경우에만 가능합니다. 모양 색상의 켈빈 값을 설정합니다. |
| <b>모양 이미지 UV 모드</b> <i>늘리다, 중간만 반복 + 1&rbrace;</i> | [모양 색상 모드]가 [이미지 입력]으로 설정된 경우에만 가능합니다. 선 모양에 이미지가 적용되는 방식을 설정하고 UV 반복 동작을 결정합니다. |
| <b>모양 이미지 반복 간격</b> <i>0.0 - 1.0</i> | [모양 색상 모드]가 [이미지 입력]으로 설정되고 [UV 모드]가 [반복 + 간격]으로 설정된 경우에만 가능합니다. 이미지가 선을 따라 반복될 때의 간격 값을 설정합니다. |
| <b>모양 이미지 감마</b> <i>sRGB, 선형</i> | [모양 색상 모드]가 [이미지 입력]으로 설정된 경우에만 가능합니다. 모양 이미지 입력을 해석하는 방법을 결정합니다. |
| <b>노출(EV)</b> <i>0.0 - 10.0</i> | 생성된 모양에 대한 노출 값 설정, 배경 이미지 노출 값과 이상적인 일치. |
| <b>선 회전</b> <i>0.0 - 1.0</i> | 해당 길이 축을 따라 선을 회전합니다. 회전 시 선은 플랫 카드로 처리됩니다. |
| <b>선 Thickness</b> <i>0.0 - 1.0</i> | 선 카드의 Thickness을 설정합니다. |
| <b>패턴</b> <i>부드러운 사각형, 날카로운 사각형, 원뿔, 반구, 이미지 입력</i> | 사용할 패턴 모양을 선택합니다. |
| <b>패턴 경도</b> <i>0.0 - 1.0</i> | 패턴의 경도/대비를 설정합니다. |
| <b>패턴 UV 모드</b> <i>늘리다, 중간만 반복 + 1&rbrace;</i> | [모양] 이미지 위에 적용된 보조 패턴 마스크를 사용하는 방법을 설정합니다. |
| <b>패턴 반복 간격</b> <i>0.0 - 1.0</i> | 패턴 UV 모드가 반복 + 간격으로 설정된 경우에만 가능합니다. 반복된 패턴 사이의 간격을 설정합니다. |
| <b>지표 클리핑 사용</b> <i>거짓/참</i> | 선 그리기의 클리핑을 활성화합니다. 지표/천장 배치 모드를 사용하는 경우 효과가 표시되지 않습니다. |
| <b>지표 Height</b> <i>-2.0 - 0.0</i> | 클리핑에 사용되는 둥근 평면의 상대 Height을 설정합니다. 그려진 지표 격자에 영향을 줍니다. |
| <b>배경 입력 사용</b> <i>거짓/참</i> | 선택적 배경 이미지 사용을 전환합니다. 합성 이미지에서 배경 상단에 조명이 생성되었습니다. |
| <b>배경색</b> <i>(색상 값)</i> | [배경 입력]을 사용하지 않는 경우에는 여기에서 단색 배경 값을 설정합니다. |
| <b>배경 감마</b> <i>sRGB, 선형</i> | [배경 입력]을 사용하는 경우 배경 입력을 해석하는 방법을 설정합니다. |

## 예

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="line-light.resources/line-light-02.gif" />
        </td>
    </tr>
</table>
