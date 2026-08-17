---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/noises/3d-voronoi-fractal.html"
breadcrumb-title: ''
description: 3D Voronoi Fractal 노드를 사용하여 체적 텍스처에 대한 3D 위치를 기반으로 프랙탈 보로노이 패턴을 생성합니다.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Noises > 3D Voronoi Fractal
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 3D Voronoi Fractal
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '740'
ht-degree: 0%

---


# 3D Voronoi Fractal

<table>
<tr style="border: 0;">
<td width="41.60%" style="border: 0;" valign="top">

![](../../../../../../assets/3dvoronoifractal.png){width="200px"}

**내부:** *텍스처 생성기* */노이즈*

**중간**

</td>
<td width="58.30%" style="border: 0;" valign="top">

## 설명

**3D Voronoi Fractal** 노드는 **위치 맵** 입력을 기반으로 3D 공간에서 *프랙탈* 보로노이 노이즈를 생성합니다.

이 베이킹된 맵은 실제 노드 대신 [큐브 3D GBuffers](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/cube-3d-gbuffers/cube-3d-gbuffers.md)을(를) 입력으로 사용하여 테스트할 수 있습니다(아래 그림 참조).

>[!WARNING]
>
> 이 노이즈는 *GPU 엔진*(예: **Direct3D** 또는 **OpenGL**)에만 사용됩니다. **도구 > 엔진 전환...**(으)로 이동하거나 **F9** 키를 눌러 원하는 엔진을 선택합니다.

</td>
</tr>
</table>

## 매개변수

* **반전** *부울*\
  출력 이미지를 반전합니다.
* **비율** *부동*\
  프랙탈 3D 보로노이 노이즈의 크기를 제어합니다.\
  *참고*: *모든 축*&#x200B;에서 **타일링**&#x200B;을 사용하도록 설정하면 크기 조정이 *단계*&#x200B;입니다. 이것은 예상된 일입니다.
* **크기** *부동 소수점3*\
  프랙탈 3D 보로노이 노이즈의 크기를 **X**, **Y** 및 **Z** 축으로 제어합니다. 균일하지 않은 값을 사용하면 *스트레치 또는 스쿼싱* 효과가 발생합니다.\
  *참고*: *모든 축*&#x200B;에서 **타일링**&#x200B;을 사용할 수 있는 경우 크기 조정은 *단계*&#x200B;입니다. 이것은 예상된 일입니다.
* **오프셋** *부동 소수점3*\
  **X**, **Y** 및 **Z** 축에서 프랙탈 3D 보로노이 노이즈의 *위치*&#x200B;에 오프셋을 적용합니다.
* **장애** *부동 소수점3*\
  **X**, **Y** 및 **Z** 축의 각 노이즈 지점에 적용된 *임의 오프셋*&#x200B;의 강도입니다.
* **왜곡 강도** *부동*\
  프랙탈 3D 보로노이 노이즈에 적용된 *뒤틀기 효과*&#x200B;의 강도를 제어합니다.
* **왜곡 배율 배율** *부동*\
  **왜곡 강도**&#x200B;로 제어되는 뒤틀기 효과에 사용되는 *변형 패턴*&#x200B;의 비율을 제어합니다.
* **최소 수준** *정수*\
  프랙탈 패턴에 사용된 최소 *반복 수준*&#x200B;입니다. 최소/최대 범위가 넓으면 더 많은 주파수 범위에서 변동이 있는 *더 풍부한 패턴*&#x200B;이 만들어집니다.
* **최대 수준** *정수*\
  프랙탈 패턴에 사용된 최대 *반복 수준*&#x200B;입니다. 최소/최대 범위가 넓으면 더 많은 주파수 범위에서 변동이 있는 *더 풍부한 패턴*&#x200B;이 만들어집니다.
* **거칠음** *부동*\
  프랙탈 패턴에서 낮음 및 높음 *반복 수준* 사이의 *균형*&#x200B;을 제어합니다.\
  *참고*: **0**&#x200B;의 값을 지정하면 그 뒤에 다른 낮은 값이 오는 *줄이 아닌* 출력이 생성됩니다. 이것은 예상된 일입니다.\
  *참고 2*: 이 매개 변수는 **혼합 모드** 매개 변수가 *추가*(으)로 설정된 경우에만 사용할 수 있습니다.
* **라쿠나리티** *부동*\
  적용된 프랙탈 패턴 *공간을 채우는 방법*&#x200B;을 제어합니다. *더 높은* 값을 사용하면 패턴에 *간격*&#x200B;이 줄어들고 *더 조밀해지는* 노이즈가 발생합니다.
* **전체 불투명도** *부동*\
  프랙탈 3D Perlin 노이즈 값의 *범위*&#x200B;를 0에서 제어합니다.
* **둥근 곡선** *부동*\
  *경사*&#x200B;을(를) 소음의 각 지점 주위에 둥글게 하여 *볼록*&#x200B;으로 만듭니다.\
  *참고*: **Style** 매개 변수가 *Edge*(으)로 설정된 경우 이 매개 변수를 사용할 수 없습니다.
* **거리 눈금** *부동*\
  노이즈의 각 지점을 중심으로 *그레이디언트의 거리*&#x200B;를 조정합니다.
* **거리 모드** *정수*\
  노이즈의 각 지점을 중심으로 *거리 그레이디언트를 계산*&#x200B;하도록 메서드를 설정합니다.
  * *유클리드*
  * *맨해튼*
  * *체비쇼프*
  * *Minkowski*
* **민코프스키 수** *부동*\
  Minkowski 거리의 순서 *p*&#x200B;입니다. 우리가 거리 구배를 사분면으로 나누면 이 숫자는 다음과 같이 사분면에 영향을 준다.
  * p는 *정확히* 1입니다. Straight
  * p는 1보다 *낮음*: 오목
  * p가 1보다 *큼*: 볼록함\
    흥미로운 값:\
    *- 1.0*: 맨해튼 거리\
    *- 2.0*: 유클리드 거리\
    *- 무한대*: 체비셰프 거리\
    *참고*: 이 매개 변수는 **거리 모드** 매개 변수가 *Minkowski*(으)로 설정된 경우에만 사용할 수 있습니다.
* **혼합 모드** *정수*\
  3D 공간에서 *겹치는 셀*&#x200B;의 값을 함께 혼합하는 방법을 설정합니다.
  * *추가*: 값을 추가합니다.
  * *최대*: *가장 높은* 값 유지
  * *분*: *최하위* 값 유지
* **스타일** *정수*&#x200B;프랙탈 3D 보로노이 노이즈의 *데이터를 렌더링*&#x200B;하는 방법을 설정합니다. 노이즈가 3D 공간의 점 세트에 기반함을 고려합니다.
  * *F1*: 3D 공간에서 *가장 가까운 지점*&#x200B;까지의 거리
  * *F2*: 3D 공간에서 *두 번째 가장 가까운 지점*&#x200B;까지의 거리
  * *F2-F1*- *F1\* F2 *-* F1/F2 *-*&#x200B;가장자리&#x200B;*: 3D 공간 노이즈의*&#x200B;각 셀 사이의 가장자리*
  * *임의 색상*: 3D 공간에서 노이즈의 각 셀에 *임의 플랫 색상*&#x200B;을 할당합니다
* **가장자리 Thickness** *부동*&#x200B;프랙탈 3D 보로노이 노이즈의 셀 사이에서 감지된 가장자리의 Thickness을 조정합니다. 가장자리는 X, Y 및 Z축에서 감지되므로 셀의 *깊이*&#x200B;에 따라 일부 두께가 다른 두께보다 빠르게 증가할 수 있습니다.\
  *참고*: 이 매개 변수는 **Style** 매개 변수가 *Edge*(으)로 설정된 경우에만 사용할 수 있습니다.
* **타일링 사용** *부울*\
  프랙탈 3D 보로노이 노이즈를 조정하여 결과 패턴이 X, Y 및 Z축에서 *반복*&#x200B;되도록 합니다.

## 예제 이미지

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/3dvoronoifractal-variant6.jpg){width="256px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../../../assets/3dvoronoifractal-variant2.jpg){width="256px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../../../assets/3dvoronoifractal-variant4.jpg){width="256px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../../../assets/3dvoronoifractal-variant5.jpg){width="256px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../../../assets/3dvoronoifractal-variant.jpg){width="256px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../../../assets/3dvoronoifractal-variant3.jpg){width="256px"}

</td>
</tr>
</table>
