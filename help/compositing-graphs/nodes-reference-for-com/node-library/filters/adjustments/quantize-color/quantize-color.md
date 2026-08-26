---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/adjustments/quantize-color.html"
breadcrumb-title: ''
description: '[색상 정량화] 노드를 사용하면 스타일화된 포스터화 효과의 색상 레벨 수를 줄일 수 있습니다.'
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Adjustments > Quantize Color
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 색상 정량화
user-guide-description: ''
user-guide-title: ''
source-git-commit: 5b9c9d12e2ccd76f75ec2a74815f9c68c43c06a2
workflow-type: tm+mt
source-wordcount: '1002'
ht-degree: 0%

---


# 색상 정량화

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![색상 아이콘 정량화](../../../../../../assets/QuantizeColor.png "색상 아이콘 정량화"){width="200px"}

<b>내부:</b> 필터 > 조정

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 설명

색상 이미지의 색상 양을 줄여 그레이디언트를 효과적으로 병합합니다.

처리된 이미지 외에도 노드는 다음을 추출합니다.

* 다른 이미지에 색을 입히는 데 사용할 수 있는 나머지 색상의 <b>팔레트</b>
* 양자화된 영역의 <b>ID 맵</b>으로, 다른 팔레트를 사용하여 처리된 이미지를 다시 채색하는 데 사용할 수 있습니다.
* 남은 색상의 <b>양</b>을 원시 정수 값으로 설정합니다.

</td>
</tr>
</table>

&#39;알파 무시&#39; 매개 변수를 &#39;False&#39;로 설정하면 원본 이미지의 알파 채널이 사용되어 양자화 프로세스를 위해 색상을 추출해야 하는 이미지 영역을 선택하는 데 사용되는 반면 투명 영역의 색상은 무시됩니다.

이렇게 하면 추출된 색상을 일부 제어할 수 있습니다.

이 노드는 [색상 팔레트 만들기](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/create-color-palette-16/create-color-palette-16.md), [색상 팔레트 적용](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/apply-color-palette/apply-color-palette.md), [색상 팔레트 수정](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/modify-color-palette/modify-color-palette.md), [색상 팔레트 보기](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/view-color-palette/view-color-palette.md) 노드와 함께 사용할 수 있습니다.

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
| <b>입력</b> 기본 *색상* | 양자화되어야 하는 색상 이미지입니다. |

## 출력 커넥터

|  |  |
| --- | --- |
| <b>출력</b> *색상* | 양자화된 색상 이미지입니다. |
| <b>ID</b> *회색 음영* | 양자화된 각각의 컬러가 고유한 정수 식별자를 할당하는 맵.   이는 다음과 같은 경우에 사용될 수 있습니다.<ul data-preserve-html="true"> <li data-preserve-html="true">[ID to Mask](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/id-to-mask/id-to-mask.md) 노드를 사용하여 일부 양자화된 영역 중 <b>마스크 추출</b></li> <li data-preserve-html="true">[색상 팔레트 적용](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/apply-color-palette/apply-color-palette.md) 또는 [색상 팔레트 수정](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/modify-color-palette/modify-color-palette.md) 노드를 사용하여 양자화된 이미지를 <b>다시 채색</b></li> </ul> |
| <b>팔레트</b> *색상* | 양자화 후 남은 색상을 유지하면서 이미지에서 추출된 팔레트입니다.   이미지는 픽셀 행으로 인코딩된 RGB 색상의 정렬된 목록으로, 최대 256개의 색상을 보유할 수 있습니다.   [색상 팔레트 보기](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/view-color-palette/view-color-palette.md) 노드를 사용하여 팔레트를 시각화할 수 있습니다. |
| <b>팔레트 색상 양</b> *정수* | 팔레트에 저장된 색상의 양입니다. |

## 매개변수

|  |  |
| --- | --- |
| <b>최대. 색상 양</b> *정수* | 양자화된 이미지에 사용해야 하는 최대 색상 양입니다.   이 양은 이미지에서 추출한 팔레트에 사용된 것과 동일합니다.   &#39;최대&#39;는 사용되고 있는 양자화 기법 때문에 이 양을 충족하지 못할 수 있음을 의미합니다. &#39;팔레트 색상 양&#39; 출력에서 추출된 색상의 실제 양을 확인합니다. |
| <b>윤곽선 다듬기</b> *부동* | 입력 이미지에 적용되는 매끄러움 효과의 반경을 제어합니다. 이렇게 하면 양자화된 이미지를 보다 견고하고 응집력 있는 모양으로 단순화할 수 있습니다.   참고: 이 매끄럽게 하려면 많은 계산이 필요하므로 이 값을 올리면 노드의 계산 시간이 상당히 늘어납니다. |
| <b>디더링</b> *부동* | 원본 이미지에서 그레이디언트와 색상 혼합을 다시 만들려고 디더링 패턴을 적용하지만 양자화 이후에 남아 있는 색상만 사용합니다.   필요한 디더링 효과를 내려면 &#39;윤곽선 매끄럽게 하기&#39; 값을 0으로 사용해야 합니다. |
| <b>디더링 패턴</b> *정수* | 원본 이미지에서 그레이디언트와 색상 혼합을 다시 만드는 데 사용되는 디더링 패턴입니다.<ul data-preserve-html="true"> <li data-preserve-html="true">파란색 노이즈</li> <li data-preserve-html="true">바이어</li> </ul> |
| <b>알파 무시</b> *부울* | 기본적으로 원본 이미지의 알파 채널은 양자화 과정에서 색상을 추출해야 하는 이미지 영역을 선택하는 데 사용되는 반면 투명 영역의 색상은 무시됩니다. 이렇게 하면 추출된 색상을 일부 제어할 수 있습니다.   실제로, 양자화 프로세스를 위해 이미지의 보이는 부분에서만 색상을 사용하고자 할 수 있습니다.   이 토글을 사용하면 투명도에 관계없이 이 마스크를 비활성화하고 *전체* 이미지를 사용할 수 있습니다. |
| <b>거리 색상 공간</b> *정수* | 색상은 *정육면체*&#x200B;에 배열되며, 이 정육면체 폭, Height 및 깊이는 색상의 각 구성 요소가 0에서 1로 증가하는 그레이디언트입니다(예: 빨간색, 녹색, 파란색(RGB).   양자화 프로세스에는 이미지에서 *색상 정의*&#x200B;를 선택한 다음 큐브에서 가장 근접한 색상을 찾아 해당 정의된 색상으로 바꾸는 작업이 포함됩니다.   이 매개 변수를 사용하면 큐브에서 색상을 배포하는 데 사용되는 색상 공간을 선택할 수 있습니다. 이렇게 하면 정의된 색상을 감지하는 조건을 변경하고 인접한 색상을 다시 배치하여 양자화 결과를 변경할 수 있습니다.   사용 사례에 맞는 색상 공간을 선택할 수 있습니다.<ul data-preserve-html="true"> <li data-preserve-html="true"><b>Lab(색상):</b> 표준화된 가시 범위 색상 공간으로, &#39;느낌&#39;이 가까운 색상이 큐브에서 실제로 가까운 방식으로 색상이 분포됩니다. 이것은 디스플레이에서 시각화될 수 있는 이미지에 적합합니다</li> <li data-preserve-html="true"><b>RGB(데이터):</b> 색상은 빨강, 녹색 및 파랑으로 분할되고 인간의 인식을 무시하고 해당 축을 따라 똑바로 분포됩니다. 표준 맵과 같은 Raw 데이터가 있는 이미지에 적합합니다</li> </ul> |
| <b>ID 정렬 모드</b> *정수* | 색상은 *정육면체*&#x200B;에 배열됩니다. 여기서 폭, Height 및 깊이는 색상의 각 구성 요소가 0에서 1로 증가하는 그레이디언트입니다(예: 빨간색, 녹색, 파란색(RGB).   이 매개변수는 추출된 팔레트의 색상 목록과 추출된 ID 맵의 영역에 있는 색인의 순서를 지정하는 데 사용되는 방법을 선택합니다.<ul data-preserve-html="true"> <li data-preserve-html="true"><b>Z-곡선:</b> 색상은 Z-곡선을 사용하여 색상 큐브에 있는 다음 색상별로 정렬됩니다(흰색에서 검정으로).</li> <li data-preserve-html="true"><b>색조:</b> 색상은 가장 가까운 색조별로 정렬됩니다.</li> <li data-preserve-html="true"><b>대표성:</b> 색상은 양자화된 이미지에서 가장 많이 사용되는 것부터 가장 적게 사용되는 것까지 정렬됩니다</li> </ul> |
| <b>축소 필터링</b> *정수* | 컬러 양자화 프로세스는 이미지의 컬러를 중요도에 따라 정렬하기 위해 축소된 크기(즉, 축소된 크기)에서 이미지의 히스토그램을 계산하는 것을 포함한다. 이 매개 변수는 막대 그래프를 계산하기 전에 축소된 이미지를 필터링하는 방법을 제어합니다.<ul data-preserve-html="true"> <li data-preserve-html="true"><b>쌍선형:</b>은(는) 이미지에 쌍선형 필터링을 적용하여, 원본 이미지의 일부가 아닐 수도 있는 보간된 색상이 있는 히스토그램을 만들어 원본 색상의 일부를 희석합니다. 이렇게 하면 많은 색상을 사용하는 이미지에 도움이 됩니다.</li> <li data-preserve-html="true"><b>가장 가까운 픽셀:</b>은(는) 필터링하지 않고 가장 가까운 픽셀의 색상을 샘플링하므로 원본 이미지의 색상만 사용하는 막대 그래프가 생성됩니다. 적은 수의 색상을 사용하는 이미지에 적합합니다.</li> </ul> |

## 예

<table>
  <tr>
    <td>
      <img src="../../../../../../assets/quantize_color_example_6_before.jpg" alt="quantize_color_example_6_before">
      <br><i>이전</i>
    </td>
    <td>
      <img src="../../../../../../assets/quantize_color_example_6_after.jpg" alt="quantize_color_example_6_after">
      <br><i>이후</i>
    </td>
  </tr>
</table>

<table>
  <tr>
    <td>
      <img src="../../../../../../assets/quantize_color_example_2_before.jpg" alt="quantize_color_example_2_before">
      <br><i>이전</i>
    </td>
    <td>
      <img src="../../../../../../assets/quantize_color_example_2_after.jpg" alt="quantize_color_example_2_after">
      <br><i>이후</i>
    </td>
  </tr>
</table>

<table>
  <tr>
    <td>
      <img src="../../../../../../assets/quantize_color_example_3_before.jpg" alt="quantize_color_example_3_before">
      <br><i>이전</i>
    </td>
    <td>
      <img src="../../../../../../assets/quantize_color_example_3_after.jpg" alt="quantize_color_example_3_after">
      <br><i>이후</i>
    </td>
  </tr>
</table>

<table>
  <tr>
    <td>
      <img src="../../../../../../assets/quantize_color_example_4_before.jpg" alt="quantize_color_example_4_before">
      <br><i>이전</i>
    </td>
    <td>
      <img src="../../../../../../assets/quantize_color_example_4_after.jpg" alt="quantize_color_example_4_after">
      <br><i>이후</i>
    </td>
  </tr>
</table>

<table>
  <tr>
    <td>
      <img src="../../../../../../assets/quantize_color_example_5_before.jpg" alt="quantize_color_example_5_before">
      <br><i>이전</i>
    </td>
    <td>
      <img src="../../../../../../assets/quantize_color_example_5_after.jpg" alt="quantize_color_example_5_after">
      <br><i>이후</i>
    </td>
  </tr>
</table>
