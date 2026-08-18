---
helpx_url: "https://helpx.adobe.com/kr/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/noises/caustics.html"
breadcrumb-title: ''
description: '[빛 무늬] 노드를 사용하여 수중 및 굴절 조명 효과를 만들기 위한 빛 무늬 패턴을 생성합니다.'
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Noises > Caustics
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 빛 무늬
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '231'
ht-degree: 0%

---


# 빛 무늬

<table>
<tr style="border: 0;">
<td width="41.60%" style="border: 0;" valign="top">

![](../../../../../../assets/rt-caustics-grayscale.png){width="128px"}

**내부:** *텍스처 생성기**/잡음*

**복합**

</td>
<td width="58.30%" style="border: 0;" valign="top">

## 설명

Height 맵과 조명 방향을 기준으로 투영된 빛 무늬 효과를 생성합니다.회색 음영과 색상 버전 모두에서 나타나며, 차이는 미세하지만 색상 버전은 색상 분산 효과를 추가합니다. 조명은 단일 지점에서 캐스팅되며 환경 맵은 사용되지 않습니다.

</td>
</tr>
</table>

## 매개변수

* **출력 색상 공간**: *Raw, sRGB*\
  출력 색상 공간을 설정합니다.
* **광자 격자 크기**: *자동, 512, 1024, 2048, 4096*\
  격자 크기를 조정하여 품질을 설정하지만 기본값은 일치하는 입력으로 설정됩니다. 계산 속도를 높이는 데 사용할 수 있습니다.
* **표면 Height 비율**: *0.0 - 1.0*\
  Height 해석 방법을 결정하는 승수입니다.
* **표면 Height 위치**: *0.0 - 1.0*\
  굴절된 서피스에서 투영까지의 거리를 설정합니다.
* **표면 IOR**: *1.0 - 2.0*\
  굴절률을 설정합니다. 색상 버전에서는 이 옵션이 더 많은 색상 분산을 추가합니다.
* **광자 크기**: *1.0 - 50.0*\
  광자 크기는 효과의 선명도에 영향을 줍니다.
* **분산**: *0.0 - 0.01(색상 버전만)*\
  색상 분산에만 영향을 줍니다. IOR가 낮으면 표시되지 않습니다.
* **떨림**: *0.0 - 1.0*\
  캐스트 광자 입자에 불규칙한 지터링을 추가합니다.
* **조명 위치**:\
  광원 위치를 이동합니다. 또한 2D 보기에서 gizmo를 통해 수행합니다.
* **배경색**: *(색상 값)(색상 버전만)*\
  배경색을 변경합니다. 회색 음영 버전에서 검은색으로 제한됩니다.
* **비정사각형 확장**: *False/True*\
  제곱이 아닌 비율로 스쿼시와 스트레치를 보정합니다.

## 예제 이미지

| <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dx_table_row-r0-column-c0_image" src="../../../../../../assets/rt-caustics-grayscale-1.png" width="300px"/></div> |
| --- |
|  |
