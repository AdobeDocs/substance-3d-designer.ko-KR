---
helpx_url: "https://helpx.adobe.com/kr/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/patterns/3d-linear-gradient.html"
breadcrumb-title: ''
description: 공간 효과를 위해 3D 세계 위치를 기반으로 선형 그레이디언트를 만들려면 3D Linear gradient 노드를 사용합니다.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Patterns > 3D Linear Gradient
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 3D Linear gradient
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '157'
ht-degree: 1%

---


# 3D Linear gradient

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/3d-linear-gradient.png){width="128px"}

## 3D Linear gradient

**인:** *텍스처 생성기**/패턴*

**중간**

</td>
<td style="border: 0;" valign="top">

## 설명

입력 위치 맵을 기반으로 볼륨 그레이디언트를 만듭니다. 3D 공간에서 2개 지점 사이에 검정에서 흰색으로 전환을 효과적으로 생성합니다. GPU 엔진에서만 사용하도록 설계되었습니다.

또한 유사한 효과에 대해서는 [3D 볼륨 마스크](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/3d-volume-mask/3d-volume-mask.md)를 참조하세요.

## 매개변수

* **점 위치 모드**: *UV 위치, 세계 공간 위치*&#x200B;그레이디언트 점이 UV 공간에서 작동하는지(2D 보기에서 설정할 때 가장 잘 작동하는지) 또는 3D 좌표에서 작동하는지를 선택합니다. 정확한 위치를 수동으로 입력하려면.
* **지점 1**:\
  그레이디언트의 시작점입니다. 위치 모드에 따라 2D 또는 3D 좌표가 될 수 있습니다.
* **지점 2**:\
  그레이디언트의 끝점입니다. 위치 모드에 따라 2D 또는 3D 좌표가 될 수 있습니다.
* **대비**: *0.0 - 1.0*\
  결과의 대비를 조정합니다.

## 예제 이미지

![](../../../../../../assets/3d-gradient.gif)

</td>
</tr>
</table>
