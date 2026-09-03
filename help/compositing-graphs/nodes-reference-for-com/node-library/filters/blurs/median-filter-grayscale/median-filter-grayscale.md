---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/blurs/median-filter-grayscale.html"
breadcrumb-title: ''
description: '[중간값 필터 회색 음영] 노드를 사용하여 노이즈를 줄이고 회색 음영 텍스처의 가장자리를 유지합니다.'
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Blurs > Median filter grayscale
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 중간 필터 회색 음영
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '326'
ht-degree: 1%

---


# 중간 필터 회색 음영

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![중간 필터 회색 음영: 아이콘](median-filter-grayscale.resources/median-filter-grayscale-01.png "중간 필터 회색 음영: 아이콘")

<b>인:</b> 필터 > 흐림 효과

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 설명

이 필터는 가장자리를 유지하면서 이미지의 노이즈를 부드럽게 합니다.

모든 픽셀에 대해 노드는 픽셀 이웃의 중간값에 따라 회색 음영 값을 계산한다.

</td>
</tr>
</table>

>[!NOTE]
>
> [중간 필터 색상](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/blurs/median-filter-color/median-filter-color.md)도 참조하세요.

<a name="inputs"></a>

## 입력

|  |  |
|:---|:---|
| <b>입력</b> <i>회색 음영</i> | 필터를 적용해야 하는 회색 음영 이미지입니다. |

<a name="outputs"></a>

## 출력

|  |  |
|:---|:---|
| <b>출력</b> <i>회색 음영</i> | 입력 회색 음영 이미지에 필터를 적용하여 계산된 회색 음영 이미지입니다. |

<a name="parameters"></a>

## 매개변수

|  |  |
|:---|:---|
| <b>커널 크기</b> *정수* | 커널은 필터의 계산에 사용되는 특정 값 그룹입니다. 이러한 맥락에서 인접 픽셀의 값입니다.<br><br>모든 픽셀에 대해 이 필터는 사각형 커널에서 해당 픽셀 주위의 모든 이웃을 가져와서 모든 이웃의 중간값을 계산합니다.<br><br>이 매개 변수는 해당 정사각형 커널의 크기를 픽셀 단위로 제어합니다. 커널이 클수록 더 세밀하고 멀리 있는 스무딩 효과를 얻을 수 있습니다.<br><br>*- 3x3:* 커널의 너비가 3픽셀, 높이가 3픽셀이며, 주변 픽셀이 총 8개입니다.<br>*- 5x5:* 커널의 너비가 5픽셀, 높이가 5픽셀이며, 주변 픽셀이 총 24개입니다. |
| <b>필터 형식</b> *정수* | 커널에서 샘플링된 인접 라우터에 적용된 계산입니다.<br><br>*- 중간값:* 모든 인접 라우터의 중간값을 직접 사용합니다.<br>*- MLMAD:*&#x200B;은 &#39;최소 중간값 절대 편차의 중간값&#39;을 나타냅니다. 편차는 값이 중앙값과 얼마나 다른지 설명합니다. MLMAD 방법은 편차가 높은 이상치 픽셀에 의해 기울어질 수 있는 중간값을 직접 사용하는 대신 모든 편차의 중간값을 사용한다. 이 방법은 커널 크기에 따라 영역들을 평평평하게 할 수 있는 더 강한 평활화 효과를 초래한다. |

## 예

<table>
  <tr>
    <td>
      <img src="median-filter-grayscale.resources/median-filter-grayscale-02.png" alt="MedianFilter_Variant2A">
      <br><i>이전</i>
    </td>
    <td>
      <img src="median-filter-grayscale.resources/median-filter-grayscale-03.png" alt="MedianFilter_Variant2B">
      <br><i>이후</i>
    </td>
  </tr>
</table>

<table>
  <tr>
    <td>
      <img src="median-filter-grayscale.resources/median-filter-grayscale-04.png" alt="MedianFilter_Variant4A">
      <br><i>이전</i>
    </td>
    <td>
      <img src="median-filter-grayscale.resources/median-filter-grayscale-05.png" alt="MedianFilter_Variant4B">
      <br><i>이후</i>
    </td>
  </tr>
</table>

<table>
  <tr>
    <td>
      <img src="median-filter-grayscale.resources/median-filter-grayscale-06.png" alt="MedianFilter_Variant1A">
      <br><i>이전</i>
    </td>
    <td>
      <img src="median-filter-grayscale.resources/median-filter-grayscale-07.png" alt="MedianFilter_Variant1B">
      <br><i>이후</i>
    </td>
  </tr>
</table>
