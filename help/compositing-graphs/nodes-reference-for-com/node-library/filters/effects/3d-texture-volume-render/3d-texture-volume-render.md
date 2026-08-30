---
helpx_url: "https://helpx.adobe.com/kr/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/3d-texture-volume-render.html"
breadcrumb-title: ''
description: 3D 텍스처 볼륨 렌더링 노드를 사용하여 3D 데이터에서 텍스처 및 안개 효과를 만들기 위한 볼륨 노드를 렌더링합니다.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > 3D Texture Volume Render
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 3D 텍스처 볼륨 렌더링
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '709'
ht-degree: 0%

---


# 3D 텍스처 볼륨 렌더링

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](3d-texture-volume-render.resources/3dtexturevolumerender.png){width="200px"}

<b>인:</b> 필터 > 효과

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 설명

**3D 텍스처 볼륨 렌더링** 노드는 **3D 텍스처** 이미지 입력에서 해당하는 *부호 있는 거리 필드*&#x200B;를 사용하여 *3D 부호 거리 필드*&#x200B;에서 설명하는 모양의 볼륨을 렌더링합니다.

볼륨이 *단위 큐브*&#x200B;의 경계 내에 표시됩니다. 조명은 *직접 조명*&#x200B;과 *반구형 스카이라이트*&#x200B;를 사용하여 계산됩니다.

>[!NOTE]
>
> 서명된 거리 필드는 256개의 조각으로 된 **16x16** 격자가 있는 모양을 설명하는 **4096x4096** 텍스처가 되어야 합니다.\
> [3D 텍스처 SDF](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/3d-texture-sdf/3d-texture-sdf.md) 노드를 사용하여 256개 슬라이스의 3D 텍스처에 대한 부호 있는 거리 필드를 계산할 수 있습니다.

</td>
</tr>
</table>

<a name="inputs"></a>

## 입력

|  |  |
|:---|:---|
| <b>3D 부호 거리 필드</b> <i>회색 음영</i> | 모양의 <i>부호 있는 거리 필드</i>의 256 <i>분할 영역</i>을 나타내는 4096x4096 이미지는 16x16 격자로 정렬됩니다.<br>256개의 슬라이스가 있는 3D 텍스처에 대한 부호 있는 거리 필드를 계산하기 위해 [3D 텍스처 SDF](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/3d-texture-sdf/3d-texture-sdf.md) 노드를 사용할 수 있습니다. |
| <b>밀도</b> <i>회색 음영</i> | 모양의 <i>밀도</i>의 256 <i>분할 영역</i>을 나타내는 4096x4096 이미지는 16x16 격자로 정렬됩니다. 밀도는 0(완전 투명)에서 1(완전 불투명)까지의 회색 음영 값을 사용하여 매핑됩니다.<br>위치 입력으로 [3D 텍스처 위치](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/3d-texture-position/3d-texture-position.md) 노드와 결합된 [3D 볼륨 마스크](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/3d-volume-mask/3d-volume-mask.md) 또는 3D 노이즈 노드([3D Perlin 노이즈](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/3d-perlin-noise/3d-perlin-noise.md), [3D 보로노이](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/3d-voronoi/3d-voronoi.md), [3D Ridged 노이즈 프랙탈](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/3d-ridged-noise-fractal/3d-ridged-noise-fractal.md) 등)를 사용하여 볼륨 마스크를 256개의 슬라이스로 구성된 3D 텍스처로 생성할 수 있습니다. |

<a name="parameters"></a>

## 매개변수

|  |  |
|:---|:---|
| <b>출력 해상도</b> <i>정수2</i> | <b>X</b> 및 <b>Y</b>의 출력 이미지 해상도이며, <i>2의 제곱</i>으로 표시됩니다. |
| <b>카메라 위치</b> <i>Float2</i> | 모양 주위의 카메라 위치입니다.<br>노드를 선택하면 카메라의 <b>2D 보기</b>에서 <i>궤도</i>까지 위치 기즈모를 사용할 수 있습니다. |
| <b>조명 위치</b> <i>Float2</i> | 모양 주위의 <i>방향 조명</i>의 위치입니다.<br>노드를 선택하면 광원의 <b>2D 보기</b>에서 <i>궤도</i>까지 위치 기즈모를 사용할 수 있습니다. |
| <b>카메라 거리</b> <i>부동</i> | 카메라에서 모양까지의 거리입니다. |
| <b>카메라 FOV</b> <i>부동</i> | <i>도</i>의 카메라 시야입니다. |
| <b>흡수</b> <i>부동</i> | 볼륨이 <i>을(를) 통과하면서 빛이 흡수되는 정도를 조정합니다</i>. |
| <b>페더</b> <i>부동</i> | <b>밀도</b> 입력에 의해 제공된 값과 <i>내부</i> 거리 필드 값을 곱합니다.<br>이는 볼륨의 외부 한계에서 안쪽으로 <i>페이딩 그레이디언트</i>의 너비를 효과적으로 조정합니다. |
| <b>밝은 색상 모드</b> <i>정수</i> | 직접 조명의 색상을 얻는 방법을 설정합니다.<br>- <i>온도(켈빈)</i>: 색상은 빛의 온도로부터 발생하며, 여기서 <i>더 낮음</i> 값은 <i>더 따뜻함</i> 색상<br>- <i>RGB 색상</i>: RGB 값을 사용하여 색상을 정의합니다. |
| <b>빛 온도(켈빈)</b> <i>부동</i> | <i>색상</i>에 영향을 주는 직접 조명의 온도입니다. <i>더 낮음</i> 값을 사용하면 <i>더 따뜻한</i> 색상이 됩니다.<br>유용한 값:<br>1800K - 촛불<br>2800K - 백열등<br>5500K - 일광<br>6200K - 자연색<br>7000K - 흐린 하늘<br><i>참고</i>: 이 매개 변수는 <b>조명 색상 모드</b> 매개 변수가 <i>온도(켈빈)</i>로 설정된 경우에만 사용할 수 있습니다. |
| <b>밝은 색상</b> <i>Float3</i> | 직접 조명의 색상입니다.<br><i>참고</i>: 이 매개 변수는 <b>조명 색상 모드</b> 매개 변수가 <i>RGB 색상</i>(으)로 설정된 경우에만 사용할 수 있습니다. |
| <b>조명 강도</b> <i>부동</i> | 직접 조명의 강도입니다. |
| <b>주변 색상</b> <i>Float3</i> | 주변 스카이라이트의 색상입니다. |
| <b>주변 강도</b> <i>부동</i> | 주변 스카이라이트의 강도입니다. |
| <b>알베도</b> <i>Float3</i> | 볼륨의 알베도 색상입니다. |
| <b>배경 모드</b> <i>정수</i> | <b>배경색</b>:<br>- <i>음영</i>에 따라 렌더링된 장면의 배경 음영 방법: 색상은 직접 조명의 <i>색상</i> 및 <i>강도</i><br>- <i>일정한 색상</i>에 영향을 받습니다. 색상은 직접 조명의 <i>에 관계없이</i> 균일하게 적용됩니다. |
| <b>배경색</b> <i>Float4</i> | 렌더링된 장면의 배경을 채우는 데 사용되는 색상입니다. |
| <b>디더링</b> <i>부동</i> | 음영을 매끄럽게 하는 데 사용되는 <i>파랑 노이즈 디더링</i>의 강도를 조정합니다. |
| <b>기준 평면 사용</b> <i>부울</i> | <i>True</i>일 때 <i>무한</i> 기준 평면을 렌더링합니다. 모양을 둘러싸는 <i>단위 육면체</i>가 이 평면에 있습니다. |
| <b>무한 평면</b> <i>부울</i> | 지표 평면을 <i>수평선으로 무한히 확장</i>하도록 설정합니다.<br><i>참고</i>: 이 매개 변수는 <b>지표 평면 사용</b> 매개 변수가 <i>True</i>(으)로 설정된 경우에만 사용할 수 있습니다. |
| <b>지표 평면 크기</b> <i>Float2</i> | 지표 평면의 크기를 조정합니다.<br><i>참고</i>: 이 매개 변수는 <b>지표 평면 사용</b> 매개 변수가 <i>True</i>(으)로 설정되어 있고 <b>무한 평면</b> 매개 변수가 <i>False</i>(으)로 설정되어 있는 경우에만 사용할 수 있습니다. |

## 예

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="3d-texture-volume-render.resources/3dtexturevolumerender-variant2.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="3d-texture-volume-render.resources/3dtexturevolumerender-variant5.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="3d-texture-volume-render.resources/3dtexturevolumerender-variant3.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="3d-texture-volume-render.resources/3dtexturevolumerender-variant.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="3d-texture-volume-render.resources/3dtexturevolumerender-variant4.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="3d-texture-volume-render.resources/3dtexturevolumerender-node.png" />
        </td>
    </tr>
</table>
