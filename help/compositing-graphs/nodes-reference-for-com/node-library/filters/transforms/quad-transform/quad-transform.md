---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/transforms/quad-transform.html"
breadcrumb-title: ''
description: 원근 교정 및 뒤틀기를 위해 4차원 변형을 텍스처에 적용하려면 [4차원 변형] 노드를 사용합니다.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Transforms > Quad Transform
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 쿼드 변형
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '113'
ht-degree: 1%

---


# 쿼드 변형

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/quad-transform-grayscale.png){width="128px"}

![](../../../../../../assets/quad-transform.png){width="128px"}

## 4중 변형(회색 음영)

**내부:** *필터/변형*

**중간**

</td>
<td style="border: 0;" valign="top">

## 설명

모퉁이점과의 상호 작용을 통해 쿼드 모양의 변형을 허용하는 특별한 변형 노드. 매우 구체적인 변형 작업을 직접 수행할 수 있습니다.

## 매개변수

* **p00**: 왼쪽 위 지점.
* **p01**: 왼쪽 아래 지점
* **p10**: 오른쪽 위 지점.
* **p11**: 오른쪽 아래 지점입니다.
* **컬링**: *앞에만, 뒤에만, 앞뒤로, 앞뒤로*&#x200B;지점이 서로 교차할 때 모양의 컬링/숨기기를 설정합니다.
* **타일링 사용**: *False/True*
* **배경색**: *(회색 음영 값)*타일링이 꺼져 있는 경우 단색 배경색입니다.
* **샘플링**: *쌍선형, 가장 가까운*&#x200B;샘플링 품질을 설정합니다.

## 예제 이미지

![](../../../../../../assets/quad-example.gif)

</td>
</tr>
</table>
