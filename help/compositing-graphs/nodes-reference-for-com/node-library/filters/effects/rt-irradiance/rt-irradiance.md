---
helpx_url: "https://helpx.adobe.com/kr/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/rt-irradiance.html"
breadcrumb-title: ''
description: RT 조도 노드를 사용하여 사실적인 조명 계산을 위해 기하학에서 실시간 조도 정보를 계산합니다.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > RT Irradiance
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 방사광
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '319'
ht-degree: 1%

---


# 방사광

<table>
<tr style="border: 0;">
<td width="41.60%" style="border: 0;" valign="top">

![](../../../../../../assets/rt-irradiance.png){width="128px"}

**내부:** *필터/효과*

**복합**

</td>
<td width="58.30%" style="border: 0;" valign="top">

## 설명

환경 맵 및 발광 맵으로부터 생성된 Height 맵 입력에 광선 추적형 조도를 생성한다. 조명을 그래프 내의 텍스처로 &quot;굽기&quot;하는 데 사용할 수 있습니다. 가짜 전역 조명 및 광선에 사용됩니다.이 노드는 계산 시간으로 인해 CPU(SSE) 엔진과 함께 사용하면 안 됩니다. 두 개의 맵을 반환합니다. 조도가 재료 입력에 적용되는 한 개의 조도 출력과 계산된 조도 값만 포함하는 한 개의 원시 조도 맵을 반환합니다.

</td>
</tr>
</table>

## 매개변수

### 입력

* **Height:** *회색 음영 입력* Height은 재질 슬롯에서 유일한 필수 입력입니다. 그것이 없으면, 그 노드는 제대로 기능하지 않을 것이다.
* **발광:** *색상 입력*&#x200B;발광 형식은 순수한 검정으로 빛을 방출하지 않고 다른 색 값으로 빛을 방출하는 형식이어야 합니다. Alpha은 무시됩니다. 결과를 보려면 이 슬롯 또는 환경 슬롯에 연결해야 합니다.
* **환경**: *색상 입력*\
  조도를 계산하는 HDR 조명 환경. 결과를 확인하려면 이 슬롯 또는 방출 슬롯에 연결해야 합니다.

### 매개변수

* **Height 크기**: *0.0 - 1.0*\
  Height 을 해석하도록 크기를 조정합니다. 전체 장면 모양에 영향을 줍니다.
* **품질**: *32개 광선, 64개 광선, 128개 광선*\
  결과 품질을 결정하지만 성능에도 영향을 줍니다. 광선이 적으면 노이즈가 많아집니다.
* **바운스 계산**: *False/True*\
  바운스의 컴퓨팅을 토글합니다. 품질과 속도에 영향을 줍니다.
* **환경 회전**: *0.0 - 1.0*\
  환경을 회전합니다.
* **환경 노출(EV)**: *-4.0 - 4.0*\
  환경에 사용할 노출 값으로 효과의 전체 명도에 영향을 줍니다.
* **발광 강도**: *0.0 - 20.0*\
  방출 입력을 위한 승수는 방출로부터의 방사 강도에 영향을 미친다.
* **발광 색상 공간**: *sRGB, 선형*\
  감수성 입력을 해석하는 데 사용되는 색상 공간입니다.
* Raw 조도 Alpha의 **IBL 그림자**: *False/True*\
  그림자를 추가할지 여부 전환
* **발광 LOD 바이어스**: *-1.0 - 1.0*&#x200B;발광 조도의 품질을 조정합니다. 값이 낮을수록 노이즈가 많아집니다.

## 예제 이미지

| <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dx_table_row-r0-column-c0_image" src="../../../../../../assets/rt-irr-03-1.jpg" width="300px"/></div> | <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dx_table_row-r0-column-c1_image" src="../../../../../../assets/rt-irr-01-1.jpg" width="300px"/></div> | <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dx_table_row-r0-column-c2_image" src="../../../../../../assets/rt-irr-02-1.jpg" width="300px"/></div> |
| --- | --- | --- |
|  |  |  |
