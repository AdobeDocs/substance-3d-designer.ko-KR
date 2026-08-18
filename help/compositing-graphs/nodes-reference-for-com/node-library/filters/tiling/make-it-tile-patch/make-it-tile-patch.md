---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/tiling/make-it-tile-patch.html"
breadcrumb-title: ''
description: Make It Tile Patch 노드를 사용하여 입력 이미지에서 매끄러운 타일링 텍스처를 패치하고 만들 수 있습니다.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Tiling > Make It Tile Patch
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 타일 패치로 만들기
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '266'
ht-degree: 0%

---


# 타일 패치로 만들기

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/make-it-tile-patch.png)

![](../../../../../../assets/make-it-tile-patch-grayscale.png)

## 타일 패치로 만들기(회색 음영)

**내부:** *필터/타일링*

**복합**

</td>
<td style="border: 0;" valign="top">

## 설명

이 노드는 그리드 기반 세미 랜덤 타일러입니다. 입력 패치를 적용하고 스탬프를 찍어내 설정에 따라 너무 많은 반복 없이 타일링 이미지로 변환하려고 시도합니다.

텍스처 패치가 작고 대규모 타일링 텍스처를 만들려는 경우에 유용합니다.

이 사진은 주로 가장자리를 수정하는 [Make-It-Tile 사진](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/tiling/make-it-tile-photo/make-it-tile-photo.md)과는 다릅니다.

전체 재질을 사용하여 이 작업을 수행하려면 [스마트 자동 타일](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/smart-auto-tile/smart-auto-tile.md)을 참조하세요.

## 매개변수

* **마스크 크기**: *0.0 - 1.0*&#x200B;패치를 스탬프할 때 사용되는 둥근 마스크의 크기입니다.
* **마스크 정밀도**: *0.0 - 1.0*&#x200B;마스크의 밝기 감소/Smoothness 정밀도.
* **마스크 뒤틀기**: *-100.0 - 100.0*&#x200B;마스크 가장자리에 뒤틀기를 도입합니다. 패치 사이의 매끄럽고 정의되지 않은 전환을 피하는 데 유용합니다.
* **패턴 크기 너비**: *0.0 - 1000.0*&#x200B;패치의 너비를 일정하지 않게 변경합니다.
* **패턴 크기 Height**: *0.0 - 1000.0*&#x200B;패치의 Height을 일정하지 않게 변경합니다.
* **장애**: *0.0 - 1.0*\
  병진 임의성을 도입하고 패치가 약간 이동합니다.
* **크기 변형**: *0.0 - 100.0*&#x200B;마스크에 크기 변형을 도입합니다.
* **옥타브**: *0 - 6*&#x200B;전체 크기를 결정하는 기본 컨트롤입니다.
* **회전**: *-360.0 - 360.0*&#x200B;패치를 사전 회전합니다.
* **회전 변형**: *0.0 - 360.0*&#x200B;모든 패치 스탬프에 대해 임의의 회전을 도입합니다.
* **배경색**: *(색상 값)*패치가 표시되지 않는 영역의 배경색을 설정합니다.
* **색상 변형**: *0.0 - 1.0(색상 버전만)*패치당 색상 변형을 소개합니다.
* **광도 변형** *(회색 음영 버전만 해당)*패치당 광도 변형을 소개합니다.

## 예제 이미지

![](../../../../../../assets/patch-ex.gif)

</td>
</tr>
</table>
