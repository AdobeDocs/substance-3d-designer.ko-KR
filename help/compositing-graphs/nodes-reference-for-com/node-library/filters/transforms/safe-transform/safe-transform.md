---
helpx_url: "https://helpx.adobe.com/kr/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/transforms/safe-transform.html"
breadcrumb-title: ''
description: 안전한 변형 노드를 사용하면 텍스처 경계를 유지하고 아티팩트를 방지하면서 변형을 적용할 수 있습니다.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Transforms > Safe Transform
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 안전한 변형
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '193'
ht-degree: 1%

---


# 안전한 변형

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/safe-transform.png)

![](../../../../../../assets/safe-transform-grayscale.png)

## 안전한 변형(회색 음영)

**내부:** *필터/변형*

**중간**

</td>
<td style="border: 0;" valign="top">

## 설명

[변형 2D](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/transformation-2d/transformation-2d.md)의 타일링 안전 버전입니다. 작은 오프셋과 회전으로 인해 타일링 없이 픽셀 세부 묘사를 손실하지 않고(선명도/선명도 손실) 비율 조정, 회전 및 오프셋을 수행할 수 있습니다.

최대 제어 또는 완벽한 선명도가 필요한 경우 노이즈를 변형하는 데 유용합니다.

## 매개변수

* **타일**: *1 - 16*&#x200B;타일링하여 입력 크기를 줄입니다.
* **오프셋 모드**: *수동, 임의*&#x200B;수동으로 정의된 오프셋 대신 임의 오프셋으로 전환합니다.
* **오프셋**: *0.0 - 1.0*\
  결과를 이동하거나 변환합니다. 픽셀이 스냅되고 보간되지 않았는지 확인합니다.
* **회전**: *0.0 - 1.0*&#x200B;각도를 따라 입력을 회전합니다.
* **타일 안전 회전**: *False/True*&#x200B;픽셀을 흐리게 하지 않는 안전 값에 스냅할지 여부를 결정하는 회전 동작입니다.
* **대칭**: *없음, X, Y, X+Y*
* **배경색**: *(색상 값)(색상 버전만)*
* **Mipmap 모드**: *자동, 수동* Mipmapping 모드를 결정합니다. 이를 수동으로 설정하면 결과가 더 선명해집니다.
* **밉맵 레벨**: *0 - 10* Mipmap 모드를 수동으로 설정하면 다른 Mipmap을 선택할 수 있습니다.

## 예제 이미지

|  |
| --- |
| 이 페이지에 첨부된 이미지가 없습니다. |

</td>
</tr>
</table>
