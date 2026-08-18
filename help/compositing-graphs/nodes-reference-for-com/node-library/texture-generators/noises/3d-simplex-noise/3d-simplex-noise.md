---
helpx_url: "https://helpx.adobe.com/kr/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/noises/3d-simplex-noise.html"
breadcrumb-title: ''
description: 3D 단순 노이즈 노드를 사용하여 3D 단순 노이즈 패턴을 생성하여 매끄럽고 자연스러워 보이는 볼륨 텍스처를 만듭니다.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Noises > 3D Simplex Noise
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 3D 단순 노이즈
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '133'
ht-degree: 1%

---


# 3D 단순 노이즈

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/3d-simplex-noise.png){width="128px"}

## 3D 단순 노이즈

**내부:** *텍스처 생성기**/잡음*

**중간**

</td>
<td style="border: 0;" valign="top">

## 설명

구워진 위치 맵을 입력 슬롯에 연결할 때 절차 노이즈를 생성합니다. GPU 엔진에만 사용됩니다.\
[3D Perlin Noise](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/3d-perlin-noise/3d-perlin-noise.md)와 비슷하지만 성능과 속도가 중요한 경우 더 빠르고 간단합니다.

이 노이즈는 실제 베이킹된 맵(아래 예제 이미지에 표시됨) 대신 [큐브 3D GBuffers](https://support.allegorithmic.com/documentation/display/SDDOC/Cube+3D+GBuffers)을(를) 입력으로 사용하여 테스트할 수 있습니다.

## 매개변수

* **비율**: *0.0 - 64.0*\
  효과의 전체 배율을 설정합니다.
* **크기**: *0.0 - 2.0* X, Y, Z축에 대해 개별적으로 균일하지 않은 크기 조절을 수행합니다.

## 예제 이미지

![](../../../../../../assets/3d-simplex.gif)

</td>
</tr>
</table>
