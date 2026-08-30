---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/3d-texture-surface-render.html"
breadcrumb-title: ''
description: 3D 텍스처 표면 렌더링 노드를 사용하여 3D 데이터에서 표면 텍스처를 렌더링하여 절차적 표면 효과를 만들 수 있습니다.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > 3D Texture Surface Render
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 3D 텍스처 표면 렌더링
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '475'
ht-degree: 0%

---


# 3D 텍스처 표면 렌더링

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](3d-texture-surface-render.resources/3dtexturesurfacerender.png){width="200px"}

<b>인:</b> 필터 > 효과

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 설명

**3D 텍스처 표면 렌더링** 노드는 **3D 거리 필드** 이미지 입력에서 해당 *거리 필드*&#x200B;를 사용하여 *3D 텍스처*&#x200B;로 설명된 모양의 표면을 렌더링합니다.

표면은 *단위 큐브*&#x200B;의 경계 내에 표시됩니다. 조명은 무한 구에 매핑된 **환경** 입력 이미지를 사용하여 계산됩니다.

>[!NOTE]
>
> 거리 필드는 256개의 슬라이스로 구성된 **16x16** 격자가 있는 모양을 설명하는 **4096x4096** 텍스처여야 합니다.\
> [3D 텍스처 SDF](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/3d-texture-sdf/3d-texture-sdf.md) 노드를 사용하여 256개 조각의 3D 텍스처에 대한 거리 필드를 계산할 수 있습니다.

</td>
</tr>
</table>

<a name="inputs"></a>

## 입력

|  |  |
|:---|:---|
| <b>3D 거리 필드</b> <i>회색 음영</i> | 모양의 <i>거리 필드</i>의 256 <i>슬라이스</i>를 나타내는 4096x4096 이미지는 16x16 격자로 정렬됩니다.<br>256개의 슬라이스로 구성된 3D 텍스처의 거리 필드를 계산하기 위해 [3D 텍스처 SDF](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/3d-texture-sdf/3d-texture-sdf.md) 노드를 사용할 수 있습니다. |
| <b>환경</b> <i>색상</i> | 렌더링에서 무한 구에 매핑해야 하는 <i>환경</i>을(를) 나타내는 이미지이며 <i>조명</i>을(를) 계산하는 데 사용됩니다.<br>이미지는 <b>배경 모드</b> 매개 변수가 <i>주변</i> 또는 <i>환경</i>(으)로 설정된 경우 장면 배경을 렌더링하는 데에도 사용됩니다. |

<a name="parameters"></a>

## 매개변수

|  |  |
|:---|:---|
| <b>출력 해상도</b> <i>정수2</i> | <b>X</b> 및 <b>Y</b>의 출력 이미지 해상도이며, <i>2의 제곱</i>으로 표시됩니다. |
| <b>카메라 위치</b> <i>Float2</i> | 모양 주위의 카메라 위치입니다.<br>노드를 선택하면 카메라의 <b>2D 보기</b>에서 <i>궤도</i>까지 위치 기즈모를 사용할 수 있습니다. |
| <b>카메라 거리</b> <i>부동</i> | 카메라에서 모양까지의 거리입니다. |
| <b>카메라 FOV</b> <i>부동</i> | <i>도</i>의 카메라 시야입니다. |
| <b>알베도</b> <i>Float3</i> | 모양 표면의 알베도 색상입니다. |
| <b>배경 모드</b> <i>정수</i> | 렌더링된 장면의 배경을 나타내는 방법:<br>- <i>지표 조도</i>: 지표 평면의 계산된 조도<br>- <i>주변</i>: <b>환경</b> 이미지 입력의 주변 색상이 이미지의 강하게 흐려진 버전과 유사한 무한 구형에 매핑됨<br>- <i>균일 색상</i>: 지정된 색상으로 배경을 균일하게 채우기<br>- <i>환경</i>: <b>환경</b> 이미지 입력이 무한 구형에 매핑됨 |
| <b>배경색</b> <i>Float4</i> | 렌더링된 장면의 배경을 균일하게 채우는 데 사용되는 색입니다.<br><i>참고</i>: 이 매개 변수는 <b>배경 모드</b> 매개 변수가 <i>균일 색상</i>(으)로 설정된 경우에만 사용할 수 있습니다. |
| <b>기준 평면 사용</b> <i>부울</i> | <i>True</i>일 때 기준 평면을 렌더링합니다. 모양을 둘러싸는 <i>단위 육면체</i>가 이 평면에 있습니다. |
| <b>무한 평면</b> <i>부울</i> | 지표 평면을 <i>수평선으로 무한히 확장</i>하도록 설정합니다.<br><i>참고</i>: 이 매개 변수는 <b>지표 평면 사용</b> 매개 변수가 <i>True</i>(으)로 설정된 경우에만 사용할 수 있습니다. |
| <b>지표 평면 크기</b> <i>Float2</i> | 지표 평면의 크기를 조정합니다.<br><i>참고</i>: 이 매개 변수는 <b>지표 평면 사용</b> 매개 변수가 <i>True</i>(으)로 설정되어 있고 <b>무한 평면</b> 매개 변수가 <i>False</i>(으)로 설정되어 있는 경우에만 사용할 수 있습니다. |

## 예

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="3d-texture-surface-render.resources/3dtexturesurfacerender-variant.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="3d-texture-surface-render.resources/3dtexturesurfacerender-variant2.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="3d-texture-surface-render.resources/3dtexturesurfacerender-variant3.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="3d-texture-surface-render.resources/3dtexturesurfacerender-variant4.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="3d-texture-surface-render.resources/3dtexturesurfacerender-node.png" />
        </td>
    </tr>
</table>
