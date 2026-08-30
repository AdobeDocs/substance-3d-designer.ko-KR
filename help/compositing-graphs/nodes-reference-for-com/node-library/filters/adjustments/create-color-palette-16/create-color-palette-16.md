---
helpx_url: "https://helpx.adobe.com/kr/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/adjustments/create-color-palette-16.html"
breadcrumb-title: ''
description: '[색상 팔레트 만들기] 텍스처를 사용하여 스타일화된 효과를 내기 위한 노드에서 16색 팔레트를 추출할 수 있습니다.'
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Adjustments > Create Color Palette (16)
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 색상 팔레트 만들기 (16)
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '296'
ht-degree: 1%

---


# 색상 팔레트 만들기 (16)

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![색상 아이콘 정량화](create-color-palette-16.resources/CreateColorPalette16.png "색상 아이콘 정량화"){width="200px"}

<b>내부:</b> 필터 > 조정

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 설명

최대 16가지 색상의 정렬된 색상 목록을 만들어 팔레트로 출력합니다.

노드는 &#39;Palette&#39; 입력 집합을 사용하여 기존 팔레트에 새 색상을 추가할 수 있습니다.

이 노드는 다음 노드와 함께 사용할 수 있습니다. [색상 정량화](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/quantize-color/quantize-color.md), [색상 팔레트 적용](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/apply-color-palette/apply-color-palette.md), [색상 팔레트 수정](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/modify-color-palette/modify-color-palette.md), [색상 팔레트 보기](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/view-color-palette/view-color-palette.md).

</td>
</tr>
</table>

<a name="inputs"></a>

## 입력

|  |  |
|:---|:---|
| <b>팔레트</b> 기본 <i>색상</i> | 픽셀 행으로 인코딩된 RGB 색상의 순서가 지정된 목록입니다. 팔레트에는 최대 256개의 색상을 사용할 수 있습니다.   이 입력은 선택 사항입니다. 이 옵션을 사용하면 노드에서 설정한 색상이 이 팔레트에 추가됩니다.   [색상 팔레트 보기](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/view-color-palette/view-color-palette.md) 노드를 사용하여 팔레트를 시각화할 수 있습니다. |
| <b>팔레트 색상 양</b> <i>정수</i> | 팔레트에 저장된 색상의 양입니다.   해당 숫자가 &#39;팔레트&#39; 이미지 입력의 실제 색상 양과 일치하지 않으면 시각화가 불완전하거나 필요한 것보다 더 많은 빈 슬롯이 있을 수 있습니다. |

<a name="outputs"></a>

## 출력

|  |  |
|:---|:---|
| <b>팔레트</b> <i>색상</i> | 지정된 색상이 추가된 업데이트된 팔레트 |
| <b>팔레트 색상 양</b> <i>정수</i> | 지정된 양의 색상이 추가되어 팔레트에 저장된 색상의 업데이트된 양입니다. |

<a name="parameters"></a>

## 매개변수

|  |  |
|:---|:---|
| <b>색상 양</b> *정수* | 팔레트에 추가해야 하는 색상의 양입니다. |
| <b>색상 #</b> *Float3* *&#39;Color amount&#39; 값으로 사용할 수 있는 매개 변수 수* | 팔레트에 추가해야 하는 색상입니다.   색상은 이 번호 매기기 목록과 같은 순서로 팔레트에 추가됩니다. |

## 예

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![색상 팔레트 만들기: 예 1](create-color-palette-16.resources/create_color_palette_example_1.png "색상 팔레트 만들기: 예 1"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![색상 팔레트 만들기: 예 2](create-color-palette-16.resources/create_color_palette_example_2.png "색상 팔레트 만들기: 예 2"){zoomable="yes"}

</td>
</tr>
</table>

![색상 팔레트 만들기: 예 3](create-color-palette-16.resources/create_color_palette_example_3.png "색상 팔레트 만들기: 예 3"){zoomable="yes"}
