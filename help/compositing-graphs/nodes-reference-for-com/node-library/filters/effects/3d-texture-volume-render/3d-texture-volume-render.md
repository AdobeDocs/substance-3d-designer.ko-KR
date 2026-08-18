---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/3d-texture-volume-render.html"
breadcrumb-title: ''
description: 3D 텍스처 볼륨 렌더링 노드를 사용하여 3D 데이터에서 흐림 및 안개 효과를 만들기 위한 볼륨 텍스처를 렌더링합니다.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > 3D Texture Volume Render
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 3D 텍스처 볼륨 렌더링
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '719'
ht-degree: 0%

---


# 3D 텍스처 볼륨 렌더링

<table>
<tr style="border: 0;">
<td width="41.60%" style="border: 0;" valign="top">

![](../../../../../../assets/3dtexturevolumerender.png){width="200px"}

**내부:** *필터/효과*

**단순**

</td>
<td width="58.30%" style="border: 0;" valign="top">

## 설명

**3D 텍스처 볼륨 렌더링** 노드는 **3D 부호 거리 필드** 이미지 입력의 해당 *부호 있는 거리 필드*&#x200B;를 사용하여 *3D 텍스처*&#x200B;로 설명된 모양의 볼륨을 렌더링합니다.

볼륨이 *단위 큐브*&#x200B;의 경계 내에 표시됩니다. 조명은 *직접 조명*&#x200B;과 *반구형 스카이라이트*&#x200B;를 사용하여 계산됩니다.

>[!NOTE]
>
> 서명된 거리 필드는 256개의 조각으로 된 **16x16** 격자로 모양을 설명하는 **4096x4096** 텍스처여야 합니다.\
> [3D 텍스처 SDF](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/3d-texture-sdf/3d-texture-sdf.md) 노드를 사용하여 256개 조각의 3D 텍스처에 대한 부호 있는 거리 필드를 계산할 수 있습니다.

</td>
</tr>
</table>

## 매개변수

### 입력

* **3D 부호 거리 필드** *회색 음영*\
  모양의 *부호 있는 거리 필드*&#x200B;의 256 *분할 영역*&#x200B;을 나타내는 4096x4096 이미지는 16x16 격자로 정렬됩니다.\
  [3D 텍스처 SDF](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/3d-texture-sdf/3d-texture-sdf.md) 노드를 사용하여 256개 조각의 3D 텍스처에 대한 부호 있는 거리 필드를 계산할 수 있습니다.
* **밀도** *회색 음영*\
  모양의 *밀도*&#x200B;의 256 *분할 영역*&#x200B;을 나타내는 4096x4096 이미지는 16x16 격자로 정렬됩니다. 0(완전 투명)부터 1(완전 불투명)까지의 회색 음영 값을 사용하여 밀도를 매핑합니다.\
  [3D 볼륨 마스크](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/3d-volume-mask/3d-volume-mask.md) 또는 3D 노이즈 노드([3D Perlin Noise](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/3d-perlin-noise/3d-perlin-noise.md), [3D 보로노이](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/3d-voronoi/3d-voronoi.md), [3D Ridged Noise Fractal](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/3d-ridged-noise-fractal/3d-ridged-noise-fractal.md) 등)를 [3D 텍스처 위치](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/3d-texture-position/3d-texture-position.md) 노드와 함께 위치 입력으로 사용하여 볼륨 마스크를 256개 조각의 3D 텍스처로 생성할 수 있습니다.

### 매개변수

* **출력 해상도** *정수2*\
  **X** 및 **Y**&#x200B;의 출력 이미지 해상도이며, *2의 제곱*&#x200B;으로 표시됩니다.
* **카메라 위치** *부동 소수점2*\
  모양 주위의 카메라 위치입니다.\
  노드를 선택하면 카메라의 **2D 보기**&#x200B;에서 *궤도*&#x200B;까지 위치 기즈모를 사용할 수 있습니다.
* **조명 위치** *부동 소수점2*\
  모양 주위의 *방향 조명*&#x200B;의 위치입니다.\
  노드를 선택하면 광원의 **2D 보기**&#x200B;에서 *궤도*&#x200B;까지 위치 기즈모를 사용할 수 있습니다.
* **카메라 거리** *부동*\
  카메라에서 모양까지의 거리입니다.
* **카메라 FOV** *부동*\
  *도*&#x200B;의 카메라 시야입니다.
* **흡수** *부동*\
  볼륨이 *을(를) 통과하면서 빛이 흡수되는 정도를 조정합니다*.
* **페더** *부동*\
  **밀도** 입력에 의해 제공된 값과 *내부* 거리 필드 값을 곱합니다.\
  이는 볼륨의 외부 한계에서 안쪽으로 *페이딩 그레이디언트*&#x200B;의 폭을 효과적으로 조정합니다.
* **조명 색상 모드** *정수*\
  직접 조명의 색상을 얻는 방법을 설정합니다.
  * *온도(켈빈)*: 색상은 빛의 온도로부터 비롯되며, 여기서 *더 낮음* 값은 *더 따뜻함* 색상이 됩니다.
  * *RGB 색상*: RGB 값을 사용하여 색상을 정의합니다.
* **색온도(켈빈)** *부동*\
  *색상*&#x200B;에 영향을 주는 직접 조명의 온도입니다. *더 낮음* 값을 사용하면 *더 따뜻한* 색상이 됩니다.\
  유용한 값:\
  1800 K - 캔들 라이트\
  2800 K - 백열구\
  5500 K - 일광\
  6200 K - 천연 흰색\
  7000K - 흐린 하늘\
  *참고*: 이 매개 변수는 **밝은 색상 모드** 매개 변수가 *온도(켈빈)*(으)로 설정된 경우에만 사용할 수 있습니다.
* **밝은 색상** *부동 소수점3*\
  직접 조명의 색상입니다.\
  *참고*: 이 매개 변수는 **조명 색상 모드** 매개 변수가 *RGB 색상*(으)로 설정된 경우에만 사용할 수 있습니다.
* **빛 강도** *부동*\
  직접 조명의 강도입니다.
* **주변 색상** *부동 소수점3*\
  주변 스카이라이트의 색상입니다.
* **주변 강도** *부동*\
  주변 스카이라이트의 강도입니다.
* **알베도** *부동 소수점3*\
  볼륨의 알베도 색상입니다.
* **배경 모드** *정수*\
  **배경색**&#x200B;을 기반으로 렌더링된 장면의 배경을 음영 하는 방법:
  * *음영*: 색상이 직접 조명의 *색상* 및 *강도*- *일정한 색상*&#x200B;에 영향을 받습니다. 색상이 직접 조명의 *관련 없음*&#x200B;에 균일하게 적용됩니다.
* **배경색** *부동 소수점4*\
  렌더링된 장면의 배경을 채우는 데 사용되는 색상입니다.
* **디더링** *부동*\
  음영을 매끄럽게 하는 데 사용되는 *파랑 노이즈 디더링*&#x200B;의 강도를 조정합니다.
* **기준 평면 사용** *부울*\
  *True*&#x200B;일 때 *무한* 기준 평면을 렌더링합니다. 모양을 둘러싸는 *단위 육면체*&#x200B;가 이 평면에 있습니다.
* **무한 평면** *부울*\
  지면을 수평선으로 *무한히 확장*&#x200B;하도록 설정합니다.\
  *참고*: 이 매개 변수는 **기준 평면 사용** 매개 변수가 *True*(으)로 설정된 경우에만 사용할 수 있습니다.
* **지표 평면 크기** *부동 소수점2*&#x200B;지표 평면의 크기를 조정합니다.\
  *참고*: 이 매개 변수는 **기준 평면 사용** 매개 변수가 *True*(으)로 설정되고 **무한 평면** 매개 변수가 *False*(으)로 설정된 경우에만 사용할 수 있습니다.

## 예제 이미지

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/3dtexturevolumerender-variant2.jpg){width="256px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../../../assets/3dtexturevolumerender-variant5.jpg){width="256px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../../../assets/3dtexturevolumerender-variant3.jpg){width="256px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../../../assets/3dtexturevolumerender-variant.jpg){width="256px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../../../assets/3dtexturevolumerender-variant4.jpg){width="256px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../../../assets/3dtexturevolumerender-node.png){width="512px"}

</td>
</tr>
</table>
