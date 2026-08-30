---
helpx_url: "https://helpx.adobe.com/kr/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/noises/voronoi-fractal.html"
breadcrumb-title: ''
description: Voronoi 프랙탈 노드를 사용하여 유기적인 세포 텍스처를 만들기 위한 프랙탈 Voronoi 패턴을 생성합니다.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Noises > Voronoi Fractal
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 보로노이 프랙탈
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '807'
ht-degree: 0%

---


# 보로노이 프랙탈

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](voronoi-fractal.resources/voronoifractal.png){width="200px"}

<b>내부:</b> 텍스처 생성기 > 잡음

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 설명

**보로노이 프랙탈** 노드는 *Z-down 직교 투영*&#x200B;을 사용하여 2D 이미지에 매핑된 *프랙탈* 3D 보로노이 노이즈를 생성합니다.

이 베이킹된 맵은 실제 노드 대신 [큐브 GBuffers](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/cube-3d-gbuffers/cube-3d-gbuffers.md)을(를) 입력으로 사용하여 테스트할 수 있습니다(아래 예제 이미지 참조).

>[!WARNING]
>
> 이 노이즈는 *GPU 엔진*(예: **Direct** 또는 **OpenGL**)에만 사용됩니다. **도구 > 엔진 전환...**(으)로 이동하거나 **F9** 키를 눌러 원하는 엔진을 선택합니다.

</td>
</tr>
</table>

<a name="parameters"></a>

## 매개변수

|  |  |
|:---|:---|
| <b>반전</b> <i>부울</i> | 출력 이미지를 반전합니다. |
| <b>크기 조절</b> <i>부동</i> | 프랙탈 보로노이 노이즈의 크기를 제어합니다.<br><br>*참고*: *모든 축*&#x200B;에서 **타일링**&#x200B;을 사용하도록 설정한 경우 크기 조정이 *단계*&#x200B;입니다. 이것은 예상된 일입니다. |
| <b>크기</b> <i>Float3</i> | **X**, **Y** 및 **Z** 축의 프랙탈 보로노이 노이즈 크기를 제어합니다. 균일하지 않은 값으로 *균등 없는 값*&#x200B;이 발생합니다.<br><br>*참고*: **타일링**&#x200B;이 *모든 축*&#x200B;에서 활성화되면 크기 조정이 *단계*&#x200B;입니다. 이것은 예상된 일입니다. |
| <b>오프셋</b> <i>Float3</i> | **X**, **Y** 및 **Z** 축에서 프랙탈 보로노이 노이즈의 *위치*&#x200B;에 오프셋을 적용합니다. |
| <b>장애</b> <i>Float3</i> | **X**, **Y** 및 **Z** 축의 각 노이즈 지점에 적용된 *임의 오프셋*&#x200B;의 강도입니다. |
| <b>왜곡 강도</b> <i>부동</i> | 프랙탈 보로노이 노이즈에 적용된 *뒤틀기 효과*&#x200B;의 강도를 제어합니다. |
| <b>왜곡 배율 배율</b> <i>부동</i> | **왜곡 강도**&#x200B;로 제어되는 뒤틀기 효과에 사용되는 *변형 패턴*&#x200B;의 비율을 제어합니다. |
| <b>최소 수준</b> <i>정수</i> | 프랙탈 패턴에 사용된 최소 *반복 수준*&#x200B;입니다. 최소/최대 범위가 넓으면 더 많은 주파수 범위에서 변동이 있는 *더 풍부한 패턴*&#x200B;이 만들어집니다. |
| <b>최대 수준</b> <i>정수</i> | 프랙탈 패턴에 사용된 최대 *반복 수준*&#x200B;입니다. 최소/최대 범위가 넓으면 더 많은 주파수 범위에서 변동이 있는 *더 풍부한 패턴*&#x200B;이 만들어집니다. |
| <b>거칠음</b> <i>부동</i> | 프랙탈 패턴에서 낮음 및 높음 *반복 수준* 간의 *균형*&#x200B;을 제어합니다.<br><br>*참고*: **0** 값을 지정하면 *해당 줄 다음에 오는 다른 낮음 값이 있는*&#x200B;에 맞지 않는 출력이 생성됩니다. 이것은 예상된 일입니다.<br><br>*참고 2*: 이 매개 변수는 **혼합 모드** 매개 변수가 *추가*(으)로 설정된 경우에만 사용할 수 있습니다. |
| <b>라쿠나리티</b> <i>부동</i> | 적용된 프랙탈 패턴 *공간을 채우는 방법*&#x200B;을 제어합니다. *더 높은* 값을 사용하면 패턴에 *간격*&#x200B;이 줄어들고 *더 조밀해지는* 노이즈가 발생합니다. |
| <b>전체 불투명도</b> <i>부동</i> | 프랙탈 펄린 노이즈 값의 *범위*&#x200B;를 0부터 제어합니다. |
| <b>둥근 곡선</b> <i>부동</i> | *경사*&#x200B;을(를) 소음의 각 지점 주위에 반올림하여 *볼록*.<br><br>*참고*: 이 매개 변수는 **Style** 매개 변수가 *Edge*(으)로 설정된 경우 사용할 수 없습니다. |
| <b>거리 눈금</b> <i>부동</i> | 노이즈의 각 지점을 중심으로 *그레이디언트의 거리*&#x200B;를 조정합니다. |
| <b>거리 모드</b> <i>정수</i> | 노이즈의 각 지점을 중심으로 *거리 그레이디언트를 계산*&#x200B;하도록 메서드를 설정합니다.<br><br>- *유클리드*<br>- *맨해튼*<br>- *체비쇼프*<br>- *민코프스키* |
| <b>민코프스키 수</b> <i>부동</i> | Minkowski 거리의 순서 *p*&#x200B;입니다. 거리 그레이디언트를 사분면으로 나누면 이 숫자는 다음과 같이 사분면에 영향을 줍니다.<br><br>- p는 *정확하게* 1: 곧게<br>- p는 1보다 *더 낮음* 1: 오목하게<br>- p는 1보다 *더 크다* 1: 볼록하게<br><br>흥미로운 값:<br><br>- *1.0*: 맨해튼 거리<br>- *2.0*: 유클리드 거리<br>- *무한대*: 체비쇼프 거리&#x200B;<br><br>*참고*: 이 매개 변수는 **거리 모드** 매개 변수가 *로 설정된 경우에만 사용할 수 있습니다. minkowski*. |
| <b>혼합 모드</b> <i>정수</i> | <br><br>- *추가*: 값 추가<br>- *최대*: *가장 높은* 값 유지<br>- *최소*: *가장 낮은* 값 유지&#x200B;** |
| <b>스타일</b> <i>정수</i> | 잡음이 공간의 점 집합을 기반으로 한다는 점을 고려하여 프랙탈 보로노이 잡음의 *데이터 렌더링*&#x200B;을 설정합니다. <br><br>- *F1*: 공간에서 *가장 가까운 점*&#x200B;까지의 거리<br>- *F2*: 공간에서 *두 번째 가장 가까운 점*&#x200B;까지의 거리<br>- *F2-F1*<br>- *F1\* F2 *<br>-* F1/F2 *<br>-*&#x200B;가장자리&#x200B;*: 공간 잡음의 각 셀 사이의*&#x200B;가장자리&#x200B;**&#x200B;임의 색상&#x200B;*:*&#x200B;임의 플랫 색상*을 공간 노이즈의 각 셀에 할당합니다<br> |
| <b>Edge Thickness</b> <i>부동</i> | 프랙탈 보로노이 노이즈의 셀 사이에서 검출되는 가장자리의 Thickness을 조정합니다. 가장자리가 X, Y 및 Z축에서 검색되므로 일부 두께는 셀의 *깊이*&#x200B;에 따라 다른 것보다 빠르게 증가할 수 있습니다.<br><br>*참고*: 이 매개 변수는 **Style** 매개 변수가 *Edge*(으)로 설정된 경우에만 사용할 수 있습니다. |
| <b>임의 색상 시드 모드</b> <i>정수</i> | 셀당 색상 선택에 대한 *임의 시드 획득*&#x200B;의 방법 설정:<br><br>- *전역 임의 시드*: 노드에서 *상속* 시드 사용<br>- *수동 시드*: *이산* 시드 사용&#x200B;<br><br>*참고*: 이 매개 변수는 **스타일** 매개 변수가 *임의 색상*(으)로 설정된 경우에만 사용할 수 있습니다. |
| <b>임의 색상 시드</b> <i>정수</i> | 셀당 색상 선택에 사용해야 하는 이산 임의 시드.<br><br>*참고*: 이 매개 변수는 **Style** 매개 변수가 *임의 색상*(으)로 설정되고 **임의 색상 시드 모드** 매개 변수가 *수동 시드*(으)로 설정된 경우에만 사용할 수 있습니다. |
| <b>타일링 사용</b> <i>부울</i> | 프랙탈 보로노이 노이즈를 조정하여 결과 패턴이 X, Y 및 Z축에서 *반복*&#x200B;되도록 합니다. |

## 예

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="voronoi-fractal.resources/fractal-voronoi-sea.gif" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="voronoi-fractal.resources/fractal-voronoi-scifi-panel.gif" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="voronoi-fractal.resources/voronoifractal-variant.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="voronoi-fractal.resources/voronoifractal-variant2.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="voronoi-fractal.resources/voronoifractal-variant6.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="voronoi-fractal.resources/voronoifractal-variant3.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="voronoi-fractal.resources/voronoifractal-variant5.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="voronoi-fractal.resources/voronoifractal-variant4.jpg" />
        </td>
    </tr>
</table>
