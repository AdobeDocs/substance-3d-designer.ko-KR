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
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '480'
ht-degree: 0%

---


# 3D 텍스처 표면 렌더링

<table>
<tr style="border: 0;">
<td width="41.60%" style="border: 0;" valign="top">

![](../../../../../../assets/3dtexturesurfacerender.png){width="200px"}

**내부:** *필터/효과*

**단순**

</td>
<td width="58.30%" style="border: 0;" valign="top">

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

## 매개변수

### 입력

* **3D 거리 필드** *회색 음영*\
  모양의 *거리 필드*&#x200B;의 256 *슬라이스*&#x200B;를 나타내는 4096x4096 이미지는 16x16 격자로 정렬됩니다.\
  [3D 텍스처 SDF](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/3d-texture-sdf/3d-texture-sdf.md) 노드를 사용하여 256개 조각의 3D 텍스처에 대한 거리 필드를 계산할 수 있습니다.
* **환경** *색상*\
  렌더링에서 무한 구에 매핑해야 하는 *환경*&#x200B;을(를) 나타내는 이미지이며 *조명*&#x200B;을(를) 계산하는 데 사용됩니다.\
  **배경 모드** 매개 변수가 *주변* 또는 *환경*(으)로 설정된 경우 이 이미지는 장면 배경을 렌더링하는 데에도 사용됩니다.

### 매개변수

* **출력 해상도** *정수2*\
  **X** 및 **Y**&#x200B;의 출력 이미지 해상도이며, *2의 제곱*&#x200B;으로 표시됩니다.
* **카메라 위치** *부동 소수점2*\
  모양 주위의 카메라 위치입니다.\
  노드를 선택하면 카메라의 **2D 보기**&#x200B;에서 *궤도*&#x200B;까지 위치 기즈모를 사용할 수 있습니다.
* **카메라 거리** *부동*\
  카메라에서 모양까지의 거리입니다.
* **카메라 FOV** *부동*\
  *도*&#x200B;의 카메라 시야입니다.
* **알베도** *부동 소수점3*\
  모양 표면의 알베도 색상입니다.
* **배경 모드** *정수*\
  렌더링된 장면의 배경을 나타내는 방법:
  * *지표 조도*: 지표 평면의 계산된 조도
  * *주변*: **환경** 이미지 입력의 주변 색상이 강한 흐림 효과가 적용된 버전의 이미지와 유사한 무한 구에 매핑되었습니다.
  * *균일한 색상*: 지정된 색상으로 배경을 균일하게 채웁니다.
  * *환경*: **환경** 이미지 입력이 무한 구에 매핑됨
* **배경색** *부동 소수점4*\
  렌더링된 장면의 배경을 균일하게 채우는 데 사용되는 색상입니다.\
  *참고*: 이 매개 변수는 **배경 모드** 매개 변수가 *균일 색상*(으)로 설정된 경우에만 사용할 수 있습니다.
* **기준 평면 사용** *부울*\
  *True*&#x200B;일 때 기준 평면을 렌더링합니다. 모양을 둘러싸는 *단위 육면체*&#x200B;가 이 평면에 있습니다.
* **무한 평면** *부울*\
  지면을 수평선으로 *무한히 확장*&#x200B;하도록 설정합니다.\
  *참고*: 이 매개 변수는 **기준 평면 사용** 매개 변수가 *True*(으)로 설정된 경우에만 사용할 수 있습니다.
* **지표 평면 크기** *부동 소수점2*&#x200B;지표 평면의 크기를 조정합니다.\
  *참고*: 이 매개 변수는 **기준 평면 사용** 매개 변수가 *True*(으)로 설정되고 **무한 평면** 매개 변수가 *False*(으)로 설정된 경우에만 사용할 수 있습니다.

## 예제 이미지

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/3dtexturesurfacerender-variant.jpg){width="256px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../../../assets/3dtexturesurfacerender-variant2.jpg){width="256px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../../../assets/3dtexturesurfacerender-variant3.jpg){width="256px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../../../assets/3dtexturesurfacerender-variant4.jpg){width="256px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../../../assets/3dtexturesurfacerender-node.png){width="512px"}

</td>
</tr>
</table>
