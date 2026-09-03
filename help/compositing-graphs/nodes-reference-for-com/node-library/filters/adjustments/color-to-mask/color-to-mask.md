---
helpx_url: "https://helpx.adobe.com/kr/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/adjustments/color-to-mask.html"
breadcrumb-title: ''
description: '[색상으로 마스크] 노드를 사용하여 특정 색상을 마스크로 변환하여 선택 처리 및 마스크 효과를 만들 수 있습니다.'
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Adjustments > Color to mask
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 마스킹할 색상
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '459'
ht-degree: 1%

---


# 마스킹할 색상

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![마스킹할 색상 - 아이콘](color-to-mask.resources/color-to-mask-01.png "마스킹할 색상 - 아이콘"){width="200px"}

<b>내부:</b> 필터 > 조정

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 설명

색상 이미지의 선택한 색상에서 회색 음영 마스크를 추출합니다.

</td>
</tr>
</table>

<a name="inputs"></a>

## 입력

|  |  |
|:---|:---|
| <b>입력</b> <i>색상</i> | 마스크의 색상을 기반으로 마스크를 추출해야 하는 입력 색상 이미지입니다. |
| <b>색상 입력</b> <i>색상</i>   *색상 입력 사용&#39;이 &#39;True&#39;로 설정된 경우 사용 가능* | 픽셀당 참조 색상을 정의하는 데 사용되는 입력 색상 이미지입니다. |

<a name="outputs"></a>

## 출력

|  |  |
|:---|:---|
| <b>출력</b> <i>회색 음영</i> | 회색 음영 비트맵으로 생성된 마스크 |

<a name="parameters"></a>

## 매개변수

|  |  |
|:---|:---|
| <b>색상 입력 사용</b> *부울* | 픽셀당 참조 색상을 정의하려면 균일한 색상 대신 입력 이미지를 사용합니다.    입력 이미지는 <b>색상 입력</b> 입력에 의해 제공됩니다. |
| <b>색상</b> *부동3* *&#39;색상 입력 사용&#39;이 &#39;거짓&#39;으로 설정된 경우 사용 가능* | 색상 선택을 수행할 때 기준이 되는 균일한 색상입니다. |
| <b>임계값</b> *부동* | 색상이 선택되는 참조 색상까지의 거리입니다. |
| <b>선택 페이드</b> *부동* | 참조 색상까지의 거리를 기준으로 색상 선택 영역을 페이드 합니다. |
| <b>거리 색상 공간</b> *정수* | 균일화 프로세스에는 색상을 비교하여 두 색상 간의 거리가 결정됩니다. 특정 색상 공간 및 거리 알고리즘은 특정 사용 사례에 더 적합합니다.   이 드롭다운 목록을 사용하여 색상을 비교하는 데 사용되는 색상 공간을 선택할 수 있습니다.<ul data-preserve-html="true"> <li data-preserve-html="true"><b><i>RGB(데이터):</i></b> 색을 빨강, 녹색, 파랑 채널로 분할하고 사람의 인식에 관계없이 해당 축을 따라 똑바로 분포합니다. Raw 데이터가 들어 있는 이미지에 적합합니다.</li> <li data-preserve-html="true"><i>선형 sRGB(색상):</i> 색상은 빨강, 녹색, 파랑 채널로 분할되고 픽셀 조명 강도에 선형 관계로 분포됩니다. 이것은 디스플레이에서 시각화될 수 있는 이미지에 적합하다.</li> <li data-preserve-html="true"><b><i>광도(색상):</i></b> 색상은 색조, 크로마, 광도 값으로 분할됩니다. 여기서 광도 값만 비교에 사용됩니다. 이것은 디스플레이에서 시각화될 수 있는 이미지에 적합하다.</li> <li data-preserve-html="true"><i>Lab(색상):</i> 표준화된 가시 범위 색상 공간으로, &#39;느낌&#39;이 가까운 색상이 큐브에서 실제로 가까운 방식으로 색상이 분포됩니다. 이것은 디스플레이에서 시각화될 수 있는 이미지에 적합하다.</li> <li data-preserve-html="true"><i>각도(표준):</i> 색상이 벡터의 X, Y, Z축으로 분할되고 내적을 통해 비교됩니다. 탄젠트 공간 수직(Tangent Space Normals)이 있는 이미지에 적합합니다.</li> </ul> |
| <b>거리 두께</b> *Float3* | Lab 색상 거리 알고리즘(DeltaE2000)에는 각 밝기, 크로마, 색조 값에 대해 특정 가중치 요인이 도입됩니다.   값을 낮추면 색차 알고리즘의 요소 영향이 감소합니다.   눈은 일반적으로 크로마(C) 또는 색조(H)보다 밝기(L)의 더 큰 차이를 받아들이기 때문에, (L:C:H)에 대한 기본 비율은 (0.5:1:1)이다. 0.5:1:1 비율을 사용하면 채도나 색조보다 명도가 두 배 정도 차이가 납니다. |

## 예

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">



</td>
<td style="border: 0;" valign="top">



</td>
</tr>
</table>
