---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/adjustments/hald-clut.html"
breadcrumb-title: ''
description: 색상 보정 및 교정을 위해 Hald CLUT 형식을 사용하여 색상 검색 테이블을 적용하려면 Hald CLUT 노드를 사용합니다.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Adjustments > Hald CLUT
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 할드 클루트
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '91'
ht-degree: 4%

---


# 할드 클루트

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/hald-clut.png){width="128px"}

## 할드 클루트

**내부:** *필터/조정*

**중간**

</td>
<td style="border: 0;" valign="top">

## 설명

입력 이미지에 LUT를 적용합니다. LUT는 4096\*4096 해상도에서 Hald 형식이어야 합니다. 자세한 내용은 <http://www.quelsolaar.com/technology/clut.html>을(를) 참조하십시오.

### 입력

* **입력**: *색상 입력*\
  LUT를 적용할 이미지입니다.
* **lut**: *색상 입력* Lut 입력 슬롯. 4096x4096이어야 합니다.

## 매개변수

* **Alpha에 의한 LUT 강도**: *거짓/참* LUT 효과에 알파 채널이 가중치를 적용하는지 정의합니다.

예

![](../../../../../../assets/content-hald-clut.jpg)

</td>
</tr>
</table>
