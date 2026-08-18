---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/mask-generators/light.html"
breadcrumb-title: ''
description: 조명 노드를 사용하여 사실적인 재질 변형을 만들기 위해 메시 조명 조건을 기반으로 마스크를 생성합니다.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Mask Generators > Light
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 조명
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '137'
ht-degree: 3%

---


# 조명

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/light-2.png){width="128px"}

## 조명

**내부:** *메시 기반 생성기**/마스크 생성기*

**단순**

</td>
<td style="border: 0;" valign="top">

## 설명

베이킹된 맵 및 사용자 설정을 기반으로 흑백 마스크를 생성합니다. [Painter](https://support.allegorithmic.com/documentation/display/SPDOC/Substance+Painter)의 [스마트 마스크](https://support.allegorithmic.com/documentation/display/SPDOC/Smart+Materials+and+Masks)와 비슷합니다.

이 마스크는 다른 Generator와 약간 다릅니다. 순수하게 World Space Normalmap을 기반으로 가짜 조명을 수행하여 흑백 &quot;라이트맵&quot; 마스크를 반환합니다.

## 매개변수

* **수평 각도**: *0.0 - 1.0*&#x200B;가짜 빛의 수평 각도를 설정합니다.
* **수직 각도**: *0.0 - 1.0*&#x200B;가짜 빛의 수직 각도를 설정합니다.
* **밝은 영역 광도**: *0.0 - 0.999*&#x200B;밝은 영역의 밝기 감소 확산을 설정합니다.
* **밝은 영역 수준**: *0.0 - 1.0*&#x200B;밝은 영역의 명도 수준을 설정합니다.

## 예제 이미지

![](../../../../../../assets/light-ex.gif)

</td>
</tr>
</table>
