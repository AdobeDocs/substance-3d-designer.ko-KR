---
helpx_url: "https://helpx.adobe.com/kr/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/noises/3d-perlin-noise.html"
breadcrumb-title: ''
description: 3D Perlin 노이즈 노드를 사용하여 3D 공간에 부드러운 Perlin 노이즈 패턴을 생성하여 자연스러워 보이는 볼륨 텍스처를 만들 수 있습니다.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Noises > 3D Perlin Noise
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 3D Perlin 노이즈
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '276'
ht-degree: 0%

---


# 3D Perlin 노이즈

<table>
<tr style="border: 0;">
<td width="41.60%" style="border: 0;" valign="top">

![](../../../../../../assets/3dperlinnoise.png){width="200px"}

**내부:** *텍스처 생성기**/잡음*

**중간**

</td>
<td width="58.30%" style="border: 0;" valign="top">

## 설명

**3D Perlin Noise** 노드는 **위치 맵** 입력을 기반으로 3D 공간에서 Perlin 노이즈를 생성합니다.

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
  3D Perlin 노이즈의 크기를 제어합니다.
* **크기** *부동 소수점3*\
  **X**, **Y** 및 **Z** 축의 3D Perlin 노이즈 크기를 제어합니다. 균일하지 않은 값을 사용하면 *스트레치 또는 스쿼싱* 효과가 발생합니다.
* **오프셋** *부동 소수점3*\
  **X**, **Y** 및 **Z** 축에서 3D Perlin 노이즈의 *위치*&#x200B;에 오프셋을 적용합니다.
* **왜곡 강도** *부동*\
  3D 펄린 노이즈에 적용된 *뒤틀기 효과*&#x200B;의 강도를 제어합니다.
* **왜곡 배율 배율** *부동*\
  **왜곡 강도**&#x200B;로 제어되는 뒤틀기 효과에 사용되는 *변형 패턴*&#x200B;의 비율을 제어합니다.
* **기준선** *부동*\
  3D Perlin 노이즈 값 분포의 기준선 *광도* 값에 *오프셋*&#x200B;을 적용합니다.
* **대비** *부동*\
  3D Perlin 노이즈의 대비를 조정합니다.
* **절대** *부울*\
  3D Perlin 노이즈에 절대값을 사용합니다. 이렇게 하면 *0.5* 아래의 값에 대한 값 분포가 효과적으로 *반전*&#x200B;됩니다.
* **타일링 사용** *부울*\
  3D Perlin 노이즈를 조정하여 결과 패턴이 X, Y 및 Z축에서 *반복*&#x200B;되도록 합니다.

## 예제 이미지

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/3dperlin.gif){width="256px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../../../assets/3dperlinnoise-variant2.jpg){width="256px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../../../assets/3dperlinnoise-variant.jpg){width="256px"}

</td>
</tr>
</table>
