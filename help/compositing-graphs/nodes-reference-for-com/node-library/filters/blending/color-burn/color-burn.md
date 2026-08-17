---
helpx_url: "https://helpx.adobe.com/kr/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/blending/color-burn.html"
breadcrumb-title: ''
description: 색상 번 혼합 노드를 사용하면 대비를 높여 그림자 및 번 효과를 만들어 텍스처를 어둡게 할 수 있습니다.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Blending > Color Burn
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 색상 번
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '102'
ht-degree: 9%

---


# 색상 번

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/color-burn.png){width="128px"}

## 색상 번

**내부:** *필터/혼합*

**단순**

</td>
<td style="border: 0;" valign="top">

## 설명

전경과 배경 사이에서 색상 번 혼합을 수행합니다. 수학적으로 공식은 1 - (1-배경) / 전경이다.

## 매개변수

### 입력

* **전경**: *색상 입력*
* **배경**: *색상 입력*
* **마스크**: *회색 음영 입력*\
  노드의 효과를 마스킹하는 데 사용되는 마스크 슬롯입니다.

### 매개변수

* **불투명도**: *0.0 - 1.0*\
  전경과 배경 간 불투명도 혼합.
* **Alpha 혼합**: *False/True*\
  전경 및 배경 알파 채널의 혼합을 전환합니다. False로 설정하면 전경의 알파 채널이 무시됩니다.

## 예제 이미지

</td>
</tr>
</table>
