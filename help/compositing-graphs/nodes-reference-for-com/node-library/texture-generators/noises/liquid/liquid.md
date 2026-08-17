---
helpx_url: "https://helpx.adobe.com/kr/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/noises/liquid.html"
breadcrumb-title: ''
description: Liquid node를 사용하여 물, 기름 및 기타 유체 표면 효과를 만들기 위한 액체 및 유체 패턴을 생성합니다.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Noises > Liquid
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 액체
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '96'
ht-degree: 2%

---


# 액체

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/liquid.png){width="128px"}

## 액체

**내부:** *텍스처 생성기**/잡음*

**단순**

</td>
<td style="border: 0;" valign="top">

## 설명

이는 [가우시안 노이즈](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/gaussian-noise/gaussian-noise.md)의 간단한 변형이며, [뒤틀기](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/warp/warp.md)를 자체적으로 만들어 액체와 같은 효과를 만듭니다.

## 매개변수

* **비율**: *1 - 128*\
  효과의 전체 배율을 설정합니다.
* **장애**: *0.0 - 1.0*\
  작은 변화를 가져오기 위해 노이즈를 위상 이동
* **뒤틀기 강도**: *0.0 - 1.0*\
  뒤틀기 효과의 강도를 설정합니다.
* **비정사각형 확장**: *False/True*\
  제곱이 아닌 비율로 스쿼시와 스트레치를 보정할 수 있습니다.

## 예제 이미지

![](../../../../../../assets/liquid-ex.gif)

</td>
</tr>
</table>
