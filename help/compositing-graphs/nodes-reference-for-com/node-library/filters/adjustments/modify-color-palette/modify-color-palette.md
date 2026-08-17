---
helpx_url: "https://helpx.adobe.com/kr/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/adjustments/modify-color-palette.html"
breadcrumb-title: ''
description: '[색상 팔레트 수정] 노드를 사용하여 텍스처에서 추출한 색상 팔레트를 조정하고 변형합니다.'
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Adjustments > Modify Color Palette
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 색상 팔레트 수정
user-guide-description: ''
user-guide-title: ''
source-git-commit: 27326c60e0247617a8f57554a68c9663934cd2bc
workflow-type: tm+mt
source-wordcount: '857'
ht-degree: 0%

---


# 색상 팔레트 수정

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![색상 아이콘 정량화](../../../../../../assets/ModifyColorPalette.png "색상 아이콘 정량화"){width="200px"}

<b>내부:</b> 필터 > 조정

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 설명

정렬된 팔레트의 색상을 수정하고 ID 맵을 사용하여 이미지에 적용합니다.

ID 맵의 색인을 팔레트의 색상 색인과 일치시켜 색상을 선택할 수 있습니다.

예를 들어 팔레트의 색상 #2은 ID 값이 2인 ID 맵의 모든 픽셀에 적용됩니다.

이 노드는 다음 노드와 함께 사용할 수 있습니다. [색상 수량화](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/quantize-color/quantize-color.md), [색상 팔레트 만들기](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/create-color-palette-16/create-color-palette-16.md), [색상 팔레트 적용](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/apply-color-palette/apply-color-palette.md), [색상 팔레트 보기](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/view-color-palette/view-color-palette.md).

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">



</td>
<td style="border: 0;" valign="top">

### 출력 커넥터

</td>
<td style="border: 0;" valign="top">

### 매개변수

</td>
</tr>
</table>

## 입력 커넥터

|  |  |
| --- | --- |
| <b>ID</b> *회색 음영* 기본 | 출력에서 색상을 수정하고 배포하기 위해 색상을 선택하는 데 사용되는 입력 ID 맵입니다.   ID 맵은 전체(예를 들어, 모양)의 일부인 픽셀들이 모두 동일한 고유 식별 값을 갖는 이미지이다. 이 경우 값은 정수입니다.   [색상 정량화](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/quantize-color/quantize-color.md) 노드를 사용하여 ID 맵을 생성할 수 있습니다. |
| <b>팔레트</b> *색상* | 픽셀 행으로 인코딩된 RGB 색상의 순서가 지정된 목록입니다. 팔레트에는 최대 256개의 색상을 사용할 수 있습니다. 노드가 수정하는 팔레트입니다.   팔레트는 [색상 정량화](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/quantize-color/quantize-color.md) 또는 [색상 팔레트 만들기](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/create-color-palette-16/create-color-palette-16.md) 노드를 사용하여 만들어질 수 있습니다. |

## 출력 커넥터

|  |  |
| --- | --- |
| <b>출력</b> *색상* | 수정된 팔레트의 색상을 ID 맵의 색인에 매핑한 결과입니다. |
| <b>팔레트</b> *색상* | 지정된 색상 수정이 적용된 업데이트된 팔레트입니다.   팔레트는 [색상 팔레트 적용](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/apply-color-palette/apply-color-palette.md) 노드를 사용하여 다른 이미지에 적용하거나 [색상 팔레트 보기](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/view-color-palette/view-color-palette.md) 노드를 사용하여 시각화할 수 있습니다. |

## 매개변수

|  |  |
| --- | --- |
| <b>색상 선택 모드</b> *정수* | 팔레트에서 수정해야 하는 대상 색상을 선택하는 방법:<ul data-preserve-html="true"> <li data-preserve-html="true"><b>색상 인덱스:</b> 대상 색상의 인덱스</li> <li data-preserve-html="true"><b>이미지 공간:</b> ID 맵에서 인덱스를 샘플링할 위치입니다. 이 모드를 선택하면 쉽게 선택할 수 있도록 2D 뷰에서 위치 기즈모를 사용할 수 있습니다</li> </ul> |
| <b>색상 위치</b> *Float2* *&#39;색상 선택 모드&#39;가 &#39;이미지 공간&#39;으로 설정된 경우 사용 가능* | ID 맵에서 인덱스를 샘플링할 위치입니다.   이미지에서 위치를 쉽게 선택하려면 2D 보기에서 기즈모를 사용합니다.   팁: ID 맵이 추출된 양자화된 이미지를 표시한 다음 색상 팔레트 수정 노드를 선택하여 gizmo를 표시할 수 있습니다. 그러면 수정할 색상을 더 직관적으로 선택할 수 있습니다. |
| <b>색상 색인</b> *정수* *&#39;색상 선택 모드&#39;가 &#39;색상 인덱스&#39;로 설정된 경우 사용 가능* | 대상 색상의 인덱스입니다.   팔레트의 색상은 왼쪽에서 오른쪽으로 정렬되며 첫 번째 색상의 색인은 0입니다. |
| <b>색상 선택 스프레드</b> *부동* | 선택 영역이 인접한 색상에 도달하는 거리를 제어합니다.   색상은 *정육면체*&#x200B;에 배열되며, 이 정육면체 폭, Height 및 깊이는 색상의 각 구성 요소가 0에서 1로 증가하는 그레이디언트입니다(예: 빨간색, 녹색, 파란색(RGB).   이 매개 변수는 큐브에서 선택한 색상을 중심으로 다른 색상도 수정할 수 있는 거리를 조정합니다. 여기서 1은 전체 큐브의 폭입니다. |
| <b>색상 선택 대비</b> *부동* | 인접한 색상에 걸쳐 선택 영역의 밝기 감소 그레이디언트를 제어합니다.   색상은 *정육면체*&#x200B;에 배열되며, 이 정육면체 폭, Height 및 깊이는 색상의 구성 요소가 0에서 1로 증가하는 그레이디언트입니다(예: 빨간색, 녹색, 파란색(RGB).   이 매개 변수는 선택한 색상 주위의 정육면체에 있는 다른 색상에 대한 선택 밝기 감소를 조정합니다. 0은 선택한 색상에서 가장 먼 색상까지의 매끄러운 그레이디언트이고 1은 완전히 포함에서 포함되지 않은 컷오프입니다. |
| <b>거리 색상 공간</b> *정수* | 색상은 *정육면체*&#x200B;에 배열되며, 이 정육면체 폭, Height 및 깊이는 색상의 구성 요소가 0에서 1로 증가하는 그레이디언트입니다(예: 빨간색, 녹색, 파란색(RGB).   이 매개 변수를 사용하면 큐브에서 색상을 배포하는 데 사용되는 색상 공간을 선택할 수 있으며, 이는 인접한 색상을 변경합니다.   사용 사례에 맞는 색상 공간을 선택할 수 있습니다.<ul data-preserve-html="true"> <li data-preserve-html="true"><b>Lab(색상):</b> 표준화된 가시 범위 색상 공간으로, &#39;느낌&#39;이 가까운 색상이 큐브에서 실제로 가까운 방식으로 색상이 분포됩니다. 이는 디스플레이에서 시각화할 수 있는 이미지에 적합합니다.</li> <li data-preserve-html="true"><b>RGB(데이터):</b> 색상은 빨강, 녹색 및 파랑으로 분할되고 인간의 인식을 무시하고 해당 축을 따라 똑바로 분포됩니다. 표준 맵과 같이 Raw 데이터가 있는 이미지에 적합합니다.</li> </ul> |
| <b>모드</b> *정수* | 대상 색상을 수정하는 방법:<ul data-preserve-html="true"> <li data-preserve-html="true"><b>색상 재정의:</b> 색상을 다른 색상으로 바꾸기</li> <li data-preserve-html="true"><b>HSL:</b> 색조, 채도 및 밝기 오프셋을 사용하여 색상 조정</li> </ul> |
| <b>불투명도</b> *부동* | 원본 색상과 수정된 색상 간의 보간을 제어합니다. 여기서 1은 수정된 색상이 원본 색상을 완전히 대체하는 것을 의미합니다. |
| <b>색상 재정의</b> *Float3* *&#39;Mode&#39;가 &#39;Override color&#39;로 설정된 경우 사용 가능* | 원래 색상을 대체할 색상을 지정합니다. |
| <b>HSL</b> *Float3* *&#39;Mode&#39;가 &#39;HSL&#39;로 설정된 경우 사용 가능* | 원본 색상에 적용된 색조, 채도 및 밝기 오프셋을 제어합니다. |

## 예

![색상 팔레트 수정: 예 1](../../../../../../assets/modify_color_palette_example_1.png "색상 팔레트 수정: 예 1"){zoomable="yes"}

![색상 팔레트 수정: 예 2](../../../../../../assets/modify_color_palette_example_3.png "색상 팔레트 수정: 예 2"){zoomable="yes"}

<table>
  <tr>
    <td>
      <img src="../../../../../../assets/modify_color_example_2_before.jpg" alt="modify_color_example_2_before">
      <br><i>이전</i>
    </td>
    <td>
      <img src="../../../../../../assets/modify_color_example_2_after.jpg" alt="modify_color_example_2_after">
      <br><i>이후</i>
    </td>
  </tr>
</table>
