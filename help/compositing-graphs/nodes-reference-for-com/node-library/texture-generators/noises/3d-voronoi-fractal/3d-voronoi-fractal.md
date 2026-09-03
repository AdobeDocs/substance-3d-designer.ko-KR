---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/noises/3d-voronoi-fractal.html"
breadcrumb-title: ''
description: 3D Voronoi Fractal 노드를 사용하여 부피 텍스처에 대한 3D 위치를 기반으로 프랙탈 보로노이 패턴을 생성합니다.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Noises > 3D Voronoi Fractal
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 3D Voronoi Fractal
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '733'
ht-degree: 0%

---


# 3D Voronoi Fractal

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](3d-voronoi-fractal.resources/3d-voronoi-fractal-01.png){width="200px"}

<b>내부:</b> 텍스처 생성기 > 잡음

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 설명

<b>3D Voronoi Fractal</b> 노드는 <b>위치 맵</b> 입력을 기반으로 3D 공간에서 <i>프랙탈</i> 보로노이 노이즈를 생성합니다.

이 베이킹된 맵은 실제 노드 대신 [큐브 3D GBuffers](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/cube-3d-gbuffers/cube-3d-gbuffers.md)을(를) 입력으로 사용하여 테스트할 수 있습니다(아래 그림 참조).

</td>
</tr>
</table>

>[!WARNING]
>
> 이 노이즈는 <i>GPU 엔진</i>(예: <b>Direct3D</b> 또는 <b>OpenGL</b>)에만 사용됩니다. <b>도구 > 엔진 전환...</b>(으)로 이동하거나 <b>F9</b> 키를 눌러 원하는 엔진을 선택합니다.

<a name="parameters"></a>

## 매개변수

|  |  |
|:---|:---|
| <b>반전</b> <i>부울</i> | 출력 이미지를 반전합니다. |
| <b>크기 조절</b> <i>부동</i> | 프랙탈 3D 보로노이 노이즈의 크기를 제어합니다.<br><br><i>참고</i>: <i>모든 축</i>에서 <b>타일링</b>을 사용하도록 설정한 경우 크기 조정이 <i>단계</i>입니다. 이것은 예상된 일입니다. |
| <b>크기</b> <i>Float3</i> | 프랙탈 3D 보로노이 노이즈의 크기를 <b>X</b>, <b>Y</b> 및 <b>Z</b> 축으로 제어합니다. 균일하지 않은 값으로 <i>균등 없는 값</i>이 발생합니다.<br><br><i>참고</i>: <b>타일링</b>이 <i>모든 축</i>에서 활성화되면 크기 조정이 <i>단계</i>입니다. 이것은 예상된 일입니다. |
| <b>오프셋</b> <i>Float3</i> | <b>X</b>, <b>Y</b> 및 <b>Z</b> 축에서 프랙탈 3D 보로노이 노이즈의 <i>위치</i>에 오프셋을 적용합니다. |
| <b>장애</b> <i>Float3</i> | <b>X</b>, <b>Y</b> 및 <b>Z</b> 축의 각 노이즈 지점에 적용된 <i>임의 오프셋</i>의 강도입니다. |
| <b>왜곡 강도</b> <i>부동</i> | 프랙탈 3D 보로노이 노이즈에 적용된 <i>뒤틀기 효과</i>의 강도를 제어합니다. |
| <b>왜곡 배율 배율</b> <i>부동</i> | <b>왜곡 강도</b>로 제어되는 뒤틀기 효과에 사용되는 <i>변형 패턴</i>의 비율을 제어합니다. |
| <b>최소 수준</b> <i>정수</i> | 프랙탈 패턴에 사용된 최소 <i>반복 수준</i>입니다. 최소/최대 범위가 넓으면 더 많은 주파수 범위에서 변동이 있는 <i>더 풍부한 패턴</i>이 만들어집니다. |
| <b>최대 수준</b> <i>정수</i> | 프랙탈 패턴에 사용된 최대 <i>반복 수준</i>입니다. 최소/최대 범위가 넓으면 더 많은 주파수 범위에서 변동이 있는 <i>더 풍부한 패턴</i>이 만들어집니다. |
| <b>거칠음</b> <i>부동</i> | 프랙탈 패턴에서 낮음 및 높음 <i>반복 수준</i> 간의 <i>균형</i>을 제어합니다.<br><br><i>참고</i>: <b>0</b> 값을 지정하면 <i>해당 줄 다음에 오는 다른 낮음 값이 있는 </i>에 맞지 않는 출력이 생성됩니다. 이것은 예상된 일입니다.<br><br><i>참고 2</i>: 이 매개 변수는 <b>혼합 모드</b> 매개 변수가 <i>추가</i>(으)로 설정된 경우에만 사용할 수 있습니다. |
| <b>라쿠나리티</b> <i>부동</i> | 적용된 프랙탈 패턴 <i>공간을 채우는 방법</i>을 제어합니다. <i>더 높은</i> 값을 사용하면 패턴에 <i>간격</i>이 줄어들고 <i>더 조밀해지는</i> 노이즈가 발생합니다. |
| <b>전체 불투명도</b> <i>부동</i> | 프랙탈 3D Perlin 노이즈 값의 <i>범위</i>를 0에서 제어합니다. |
| <b>둥근 곡선</b> <i>부동</i> | <i>경사</i>을(를) 소음의 각 지점 주위에 반올림하여 <i>볼록</i>.<br><br><i>참고</i>: 이 매개 변수는 <b>Style</b> 매개 변수가 <i>Edge</i>(으)로 설정된 경우 사용할 수 없습니다. |
| <b>거리 눈금</b> <i>부동</i> | 노이즈의 각 지점을 중심으로 <i>그레이디언트의 거리</i>를 조정합니다. |
| <b>거리 모드</b> <i>정수</i> | 노이즈의 각 지점을 중심으로 <i>거리 그레이디언트를 계산</i>하도록 메서드를 설정합니다.<br><br>- <i>유클리드</i><br>- <i>맨해튼</i><br>- <i>체비쇼프</i><br>- <i>민코프스키</i> |
| <b>민코프스키 수</b> <i>부동</i> | Minkowski 거리의 순서 <i>p</i>입니다. 거리 그레이디언트를 사분면으로 나누면 이 숫자는 다음과 같이 사분면에 영향을 줍니다.<br><br>- p는 <i>정확하게</i> 1: 곧게<br>- p는 1보다 <i>더 낮음</i> 1: 오목하게<br>- p는 1보다 <i>더 크다</i> 1: 볼록하게<br><br>흥미로운 값:<br>- <i>1.0</i>: 맨해튼 거리<br>- <i>2.0</i>: 유클리드 거리<br>- <i>무한대</i>: 체비쇼프 거리<br><br><i>참고</i>: 이 매개 변수는 <b>거리 모드</b> 매개 변수가 <i>로 설정된 경우에만 사용할 수 있습니다. minkowski</i>. |
| <b>혼합 모드</b> <i>정수</i> | 3D 공간에서 <i>겹치는 셀</i>의 값을 함께 혼합하는 방법을 설정합니다.<br><br>- <i>추가</i>: 값 추가<br>- <i>최대</i>: <i>가장 높은</i> 값 유지<br>- <i>최소</i>: <i>가장 낮은</i> 값 유지 |
| <b>스타일</b> <i>정수</i> | 잡음이 3D 공간의 점 집합을 기반으로 하는 것을 고려하여 프랙탈 3D 보로노이 잡음의 <i>데이터 렌더링</i>을 설정합니다. <br><br>- <i>F1</i>: 3D 공간에서 <i>가장 가까운 점</i>까지의 거리<br>- <i>F2</i>: 3D 공간에서 <i>두 번째 가장 가까운 점</i>까지의 거리<br>- <i>F2-F1</i><br>- <i>F1\*F2</i><br>- <i>F1/F2</i><br>- <i>가장자리</i>: 각 셀</i>의 <i>가장자리 3D 공간 노이즈<br>- <i>임의 색상</i>: 3D 공간 노이즈의 각 셀에 <i>임의 플랫 색상</i>을 할당합니다 |
| <b>Edge Thickness</b> <i>부동</i> | 프랙탈 3D 보로노이 노이즈의 셀 사이에서 검출되는 가장자리의 Thickness을 조정합니다. 가장자리가 X, Y 및 Z축에서 검색되므로 일부 두께는 셀의 <i>깊이</i>에 따라 다른 것보다 빠르게 증가할 수 있습니다.<br><br><i>참고</i>: 이 매개 변수는 <b>Style</b> 매개 변수가 <i>Edge</i>(으)로 설정된 경우에만 사용할 수 있습니다. |
| <b>타일링 사용</b> <i>부울</i> | 프랙탈 3D 보로노이 노이즈를 조정하여 결과 패턴이 X, Y 및 Z축에서 <i>반복</i>되도록 합니다. |

## 예

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="3d-voronoi-fractal.resources/3d-voronoi-fractal-02.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="3d-voronoi-fractal.resources/3d-voronoi-fractal-03.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="3d-voronoi-fractal.resources/3d-voronoi-fractal-04.jpg" />
        </td>
    </tr>
    <tr style="border: 0; background: transparent">
        <td style="border: 0; background: transparent">
            <img src="3d-voronoi-fractal.resources/3d-voronoi-fractal-05.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="3d-voronoi-fractal.resources/3d-voronoi-fractal-06.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="3d-voronoi-fractal.resources/3d-voronoi-fractal-07.jpg" />
        </td>
    </tr>
</table>
