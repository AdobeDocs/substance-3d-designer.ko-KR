---
helpx_url: "https://helpx.adobe.com/kr/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/blurs/non-uniform-blur.html"
breadcrumb-title: ''
description: 비균일 흐림 효과 노드를 사용하면 비등방성 효과를 내기 위해 X 방향과 Y 방향으로 강도를 달리하는 흐림 효과를 적용할 수 있습니다.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Blurs > Non Uniform Blur
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 균일하지 않은 흐림 효과
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '178'
ht-degree: 2%

---


# 균일하지 않은 흐림 효과

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/non-uniform-blur-grayscale.png){width="128px"}

![](../../../../../../assets/non-uniform-blur.png){width="128px"}

## 균일하지 않은 흐림(회색 음영)

**내부:** *필터/흐림 효과*

**중간**

</td>
<td style="border: 0;" valign="top">

## 설명

고품질 흐림 효과를 수행합니다. 여기서 강도는 입력 마스크에 의해 구동됩니다. 옵션을 사용하여 비등방성 및 측정 기능을 추가할 수 있습니다.

## 매개변수

### 입력

* **흐림 효과 맵**: *회색 음영 입력*&#x200B;효과 강도로 마스크 맵.

### 매개변수

* **강도**: *0.0 - 50.0*&#x200B;흐림 효과를 적용할 최대 강도. 흐림 효과 맵으로 마스크되어 이 설정은 해당 맵의 검정 영역에는 영향을 주지 않습니다.
* **비등방성**: *0.0 - 1.0*&#x200B;선택적으로 흐림 효과에 방향성을 추가합니다. 각도 매개변수에 의해 제어됩니다.
* **비대칭**: *0.0 - 1.0*&#x200B;선택적으로 샘플링에 편의를 추가합니다. 각도 매개변수에 의해 제어됩니다.
* **각도**: *0.0 - 1.0*&#x200B;각도 - 방향 및 샘플링 편향을 설정합니다.
* **샘플**: *1 - 16*&#x200B;샘플 양에 따라 품질이 결정됩니다. 블레이드의 양을 곱합니다.
* **블레이드**: *1 -* 9\
  샘플링 섹터의 양은 품질을 결정합니다. 샘플 양을 곱합니다.

## 예제 이미지

*아래 예제는 [흐림 효과 맵] 슬롯의 90도 경사도에 의해 구동됩니다.*

![](../../../../../../assets/nonuniform-example.gif)

</td>
</tr>
</table>
