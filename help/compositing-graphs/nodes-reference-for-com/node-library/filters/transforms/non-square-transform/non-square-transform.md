---
helpx_url: "https://helpx.adobe.com/kr/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/transforms/non-square-transform.html"
breadcrumb-title: ''
description: 정사각형이 아닌 변형 노드를 사용하면 독립적인 X 및 Y 비율을 사용하여 정사각형이 아닌 텍스처에 변형을 적용할 수 있습니다.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Transforms > Non-Square Transform
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 정사각형이 아닌 변형
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '219'
ht-degree: 0%

---


# 정사각형이 아닌 변형

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/safe-transform.png)

![](../../../../../../assets/safe-transform-grayscale.png)

## 정사각형이 아닌 변형(회색 음영)

**내부:** *필터/변형*

**중간**

</td>
<td style="border: 0;" valign="top">

## 설명

정사각형이 아닌 [Transform 2D](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/transformation-2d/transformation-2d.md) 버전입니다. 정사각형이 아닌 비율을 자동으로 감지하여 정사각형 입력 이미지를 정사각형이 아닌 캔버스로 변환할 수 있습니다.

몇 가지 설정을 올바르게 설정해야 하므로 이 노드를 최대한 활용하려면 [그래프 매개 변수](../../../../../../compositing-graphs/graph-parameters/graph-parameters.md)를 완전히 이해해야 합니다.

* **그래프** 크기는 정사각형이 아니어야 합니다. 그렇지 않으면 이 노드가 필요하지 않습니다.
* 정사각형이 아닌 변환 **노드** 출력 크기를 &quot;*부모*&quot;에 상대적으로 설정합니다.
* 입력을 단일 위치로만 변환하려면 **노드** 타일링 모드를 &quot;*타일링 없음*&quot;으로 설정하십시오.

## 매개변수

* **타일 모드**: *자동, 수동*&#x200B;정사각형이 아닌 자동 보상 사용 여부.
* **타일**: *1 - 16*&#x200B;타일 모드가 수동으로 설정된 경우에만 액세스할 수 있습니다. 타일링에 적합한 방식으로 배율을 변경할 수 있습니다.
* **오프셋**: *0.0 - 1.0*\
  결과를 이동하거나 변환합니다. 슬라이더를 두 번 클릭하여 음수 값을 입력합니다.
* **회전**: *0.0 - 1.0*&#x200B;입력 이미지를 회전합니다.
* **안전한 회전(정사각형만)**: *False/True*&#x200B;픽셀의 선명도를 유지하기 위해 안전한 값에 스냅합니다.
* **배경색**: *(색상 값)*이미지를 채울 배경색입니다. 기본 매개 변수의 [타일링 모드가 &quot;*타일링 없음*&quot;](../../../../../../compositing-graphs/graph-parameters/graph-parameters.md)&quot;으로 설정된 경우에만 표시됩니다.

## 예제 이미지

| <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid_items_grid-cell1_position-par_dx_table_row-r0-column-c0_image" src="../../../../../../assets/nonsquare-ex.png" width="300px"/></div> |
| --- |
|  |

</td>
</tr>
</table>
