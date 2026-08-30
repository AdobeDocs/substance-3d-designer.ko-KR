---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/3d-view-library/hdri-tools/sphere-light.html"
breadcrumb-title: ''
description: 구 광원 노드를 사용하여 HDRI 환경에 구 광원을 추가하여 조명 제어를 향상시킵니다.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > 3D View (Library) > HDRI Tools > Sphere Light
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 구 라이트
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '518'
ht-degree: 4%

---


# 구 라이트

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](sphere-light.resources/panorama-sphere-light.png){width="200px"}

<b>내부:</b> 3D 보기 > HDRI 도구

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 설명

구형으로 투영된 구 모양을 생성합니다. 구 변환은 변환 기즈모에 의해 제어됩니다.

구 조명은 다재다능하며 단순한 둥근 조명을 생성할 뿐만 아니라 행성 또는 다른 천체를 생성할 수 있는 옵션이 있습니다. 고급 조명 및 회전 옵션이 필요하지 않은 경우 대신 [조명 모양](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/3d-view-library/hdri-tools/shape-light/shape-light.md)을 확인하십시오.

</td>
</tr>
</table>

<a name="inputs"></a>

## 입력

|  |  |
|:---|:---|
| <b>배경 이미지 입력</b> <i>색상 입력</i> | 생성된 빛을 구성할 선택적 배경입니다. |
| <b>모양 이미지 입력</b> <i>색상 입력</i> | 구체 조명에 매핑할 선택적 이미지입니다. [모양 색상 모드]가 [이미지 입력]으로 설정된 경우에만 사용됩니다. |

<a name="parameters"></a>

## 매개변수

|  |  |
|:---|:---|
| <b>위치 모드</b> <i>원점으로부터의 거리, 세계 위치</i> | 두 배치 모드 중 하나를 선택합니다. 원점으로부터의 거리는 극 좌표와 비슷하고, 구는 파노라마의 중심을 기준으로 설정되며, 세계 위치는 표준 3D 좌표처럼 작동합니다. |
| <b>위치 좌표</b> |  |
| <b>위쪽 벡터</b> <i>Z 위로, Y 위로</i> | 세계 위치 모드에서만 좌표계의 방향을 결정합니다. |
| <b>구 세계 위치</b> <i>-2.0 - 2.0</i> | [세계 위치] 모드를 사용하는 경우에만 세계 공간에서 구 위치를 설정합니다. |
| <b>위치</b> | 원점으로부터의 거리 모드에서만 가능합니다. 중심을 기준으로 위치를 설정합니다. 2D 보기에서 조작 가능 |
| <b>원점으로부터의 거리</b> <i>0.0 - 20.0</i> | 원점으로부터의 거리 모드에서만 가능합니다. 원점까지의 거리를 설정하고 구의 표시 크기에 영향을 줍니다. |
| <b>모양 색상 모드</b> <i>RGB, 온도(켈빈), 이미지 입력</i> | 모양 색상을 설정하는 데 사용할 방법을 선택합니다. 이미지 입력(Image Input)은 두 번째 입력 슬롯을 사용할 수 있게 합니다. |
| <b>색상</b> <i>(색상 값)</i> | [모양 색상 모드]가 [RGB]로 설정된 경우에만 가능합니다. 모양의 색상을 선택합니다. |
| <b>모양 온도</b> <i>800.0 - 20000.0</i> | [모양 색상 모드]가 [온도]로 설정된 경우에만 가능합니다. 모양 색상의 켈빈 값을 설정합니다. |
| <b>구 이미지 입력 감마</b> <i>sRGB, 선형</i> | [모양 색상 모드]가 [이미지 입력]으로 설정된 경우에만 가능합니다. 모양 이미지 입력을 해석하는 방법을 결정합니다. |
| <b>구 회전</b> <i>0.0 - 1.0</i> | [모양 색상 모드]가 [이미지 입력]으로 설정된 경우에만 가능합니다. 가운데를 중심으로 구를 회전시켜 매핑된 이미지의 방향을 지정합니다. |
| <b>노출(EV)</b> <i>0.0 - 10.0</i> | 생성된 모양에 대한 노출 값 설정, 배경 이미지 노출 값과 이상적인 일치. |
| <b>구 반경</b> <i>0.0 - 1.0</i> | 구의 반지름/크기를 설정합니다. |
| <b>구 경도</b> <i>0.0 - 1.0</i> | 구의 경도/밝기 감소를 설정합니다. |
| <b>음영</b> <i>없음, 팔다리 어둡게 하기, 음영 조명</i> | 구에 음영을 적용할지 여부를 설정합니다. 구를 단색의 비조명 오브젝트로 표시하지 않도록 허용합니다. 팔다리 어둡게 하기는 가장자리에 약간의 어두움이 나타나는 것을 의미하며, 음영 표시등은 구형에 선택적 음영 표시등이 켜지는 것을 의미합니다. |
| <b>조명 음영 위치</b> <i>-1.0 - 1.0</i> | [음영]를 [빛 음영]로 설정하면 구체에 대한 빛의 위치가 여기에서 제어됩니다. |
| <b>Penombra 투명도</b> <i>0.0 - 1.0</i> | [음영]가 [음영 라이트]로 설정되어 있으면 음영의 밝기 감소를 제어합니다. |
| <b>배경 입력 사용</b> <i>거짓/참</i> | 선택적 배경 이미지 사용을 전환합니다. 합성 이미지에서 배경 상단에 조명이 생성되었습니다. |
| <b>배경색</b> <i>(색상 값)</i> | [배경 입력]을 사용하지 않는 경우에는 여기에서 단색 배경 값을 설정합니다. |
| <b>배경 감마</b> <i>sRGB, 선형</i> | [배경 입력]을 사용하는 경우 배경 입력을 해석하는 방법을 설정합니다. |

## 예

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="sphere-light.resources/sphere-light-ex.gif" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="sphere-light.resources/spherelight-ex1.png" />
        </td>
    </tr>
</table>
