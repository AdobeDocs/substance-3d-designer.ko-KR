---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/noises/cells-4.html"
breadcrumb-title: ''
description: 셀 4 노드를 사용하여 유기적 및 생물학적 텍스처 효과를 만들기 위한 고급 세포 패턴을 생성합니다.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Noises > Cells 4
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 셀 4
user-guide-description: ''
user-guide-title: ''
source-git-commit: 5b9c9d12e2ccd76f75ec2a74815f9c68c43c06a2
workflow-type: tm+mt
source-wordcount: '261'
ht-degree: 3%

---


# 셀 4

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![셀 4 - 아이콘](../../../../../../assets/cells_4.png "셀 4 - 아이콘"){width="200px"}

<b>내부:</b> 텍스처 생성기 > 노이즈

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 설명

<b>셀</b> 벽으로 둘러싸인 노이즈의 변형.

각 셀에는 플랫 컬러가 할당되는데, 이는 랜덤이거나 입력 이미지로부터 샘플링될 수 있다.

참고 항목: [셀 1](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/cells-1/cells-1.md), [셀 2](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/cells-2/cells-2.md), [셀 3](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/cells-3/cells-3.md)

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

### 입력

</td>
<td style="border: 0;" valign="top">

### 출력

</td>
<td style="border: 0;" valign="top">

### 매개변수

</td>
<td style="border: 0;" valign="top">

### 예

</td>
</tr>
</table>

## 입력

|  |  |
| --- | --- |
| <b>입력</b> *회색 음영* |  |

## 출력

|  |  |
| --- | --- |
| <b>출력</b> *회색 음영* | 회색 음영 비트맵으로 생성된 노이즈 |

## 매개변수

|  |  |
| --- | --- |
| <b>비율</b> 정수 | 노이즈 타일을 생성하는 데 사용되는 격자의 하위 분할입니다.    값이 높을수록 더 많은 타일이 그려지고 노이즈가 더 많아집니다. |
| <b>장애</b> 부동 | 소음의 성분을 제거합니다.    이 효과를 사용하면 노이즈에 애니메이션을 적용할 수 있습니다. |
| <b>장애 속도</b> 부동 | <b>Disorder</b> 매개 변수에 의해 적용된 변위의 거리를 조정합니다.    이 효과는 노이즈에 애니메이션을 적용할 때 변위 속도를 제어하는 데 사용할 수 있습니다. |
| <b>색상 소스</b> 정수 | 셀에 적용된 단색의 소스:<ul data-preserve-html="true"> <li data-preserve-html="true"><b><i>임의:</i></b> 노드의 임의 시드로 제어되는 임의 색상을 사용합니다.</li> <li data-preserve-html="true"><b><i>의사난수:</i></b> 별도의 사용자 설정 값으로 시드된 임의의 색상을 사용합니다.</li> <li data-preserve-html="true"><b><i>이미지 입력:</i></b> 입력 이미지의 셀 위치에서 샘플링된 색상을 사용합니다.</li> </ul> |
| <b>의사난수 시드</b> 정수 *&#39;색상 소스&#39;가 &#39;의사난수&#39;로 설정된 경우 사용 가능* | 노드 시드와 별도로 색상의 시드를 변경할 수 있습니다. |
| <b>정사각형이 아닌 확장</b> 부울 | 정사각형이 아닌 이미지에서 생성된 타일 사각형을 유지하고 노이즈 생성을 이미지 경계까지 확장합니다. |

## 예

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![셀 4 - 예 1](../../../../../../assets/cells_4_1.png "셀 4 - 예 1"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![셀 4 - 예 2](../../../../../../assets/noise_cells_4_v2_speed0.3_aniso0.6.gif "셀 4 - 예 2"){zoomable="yes"}

</td>
</tr>
</table>

</td>
<td style="border: 0;" valign="top">



</td>
<td style="border: 0;" valign="top">



</td>
</tr>
</table>
