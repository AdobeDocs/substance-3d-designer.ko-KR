---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/adjustments/view-color-palette.html"
breadcrumb-title: ''
description: '[색상 팔레트 보기] 노드를 사용하여 분석을 위해 텍스처에서 추출한 색상 팔레트 데이터를 시각화할 수 있습니다.'
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Adjustments > View Color Palette
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 색상 팔레트 보기
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '232'
ht-degree: 1%

---


# 색상 팔레트 보기

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![색상 아이콘 정량화](view-color-palette.resources/view-color-palette-01.png "색상 아이콘 정량화"){width="200px"}

<b>내부:</b> 필터 > 조정

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 설명

색상 팔레트를 사각형 또는 사각형으로 압축하여 그래프 보기 또는 2D 보기에서 보다 쉽게 시각화할 수 있습니다.\
그 패킹은 가능한 한 적은 빈 공간을 남기는 것을 목표로 한다.

</td>
</tr>
</table>

팔레트의 색상 순서는 텍스트 감싸기와 유사하게 왼쪽에서 오른쪽으로, 위에서 아래로 흐르면서 유지됩니다.

이 노드는 다음 노드에서 생성된 팔레트를 시각화하는 데 사용할 수 있습니다. [색상 정량화](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/quantize-color/quantize-color.md), [색상 팔레트 만들기](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/create-color-palette-16/create-color-palette-16.md), [색상 팔레트 수정](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/modify-color-palette/modify-color-palette.md).

<a name="inputs"></a>

## 입력

|  |  |
|:---|:---|
| <b>팔레트</b> 기본 <i>색상</i> | 픽셀 행으로 인코딩된 RGB 색상의 순서가 지정된 목록입니다. 팔레트에는 최대 256개의 색상을 사용할 수 있습니다.   노드가 팩하고 렌더링하는 팔레트입니다. |
| <b>팔레트 색상 양</b> <i>정수</i> | 팔레트에 저장된 색상의 양입니다.   해당 숫자가 &#39;팔레트&#39; 이미지 입력의 실제 색상 양과 일치하지 않으면 시각화가 불완전하거나 필요한 것보다 더 많은 빈 슬롯이 있을 수 있습니다. |

<a name="outputs"></a>

## 출력

|  |  |
|:---|:---|
| <b>출력</b> <i>색상</i> | 압축된 팔레트의 시각화입니다. |

## 예

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![색상 팔레트 보기: 예 1](view-color-palette.resources/view-color-palette-02.png "색상 팔레트 보기: 예 1"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![색상 팔레트 보기: 예 2](view-color-palette.resources/view-color-palette-03.png "색상 팔레트 보기: 예 2"){zoomable="yes"}

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![색상 팔레트 보기: 예 3](view-color-palette.resources/view-color-palette-04.png "색상 팔레트 보기: 예 3"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![색상 팔레트 보기: 예 4](view-color-palette.resources/view-color-palette-05.png "색상 팔레트 보기: 예 4"){zoomable="yes"}

</td>
</tr>
</table>
