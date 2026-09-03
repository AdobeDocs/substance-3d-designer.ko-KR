---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/blurs/mlv-color.html"
breadcrumb-title: ''
description: MLV 색상 흐림 효과 필터를 사용하면 동적 시각적 효과를 위해 색상 텍스처에 동작 흐림 효과를 적용할 수 있습니다.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Blurs > MLV color
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: MLV 색상
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '352'
ht-degree: 1%

---


# MLV 색상

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![MLV 색상: 아이콘](mlv-color.resources/mlv-color-01.png "MLV 색상: 아이콘")

<b>인:</b> 필터 > 흐림 효과

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 설명

MLV는 <b>&#39;최소 분산 평균&#39;</b>을(를) 나타냅니다. 이 필터는 가장자리를 개선하고 이미지의 노이즈를 부드럽게 합니다.

이 필터는 이미지에서 구조화된 영역을 찾아 이를 사용하여 선명하게 하고 고르게 합니다. 일부 경우에는 구조화 영역보다 더 넓은 그레이디언트를 따라 단계가 발생할 수 있습니다.

</td>
</tr>
</table>

>[!NOTE]
>
> [MLV 회색 음영](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/blurs/mlv-grayscale/mlv-grayscale.md)도 참조하세요.

<a name="inputs"></a>

## 입력

|  |  |
|:---|:---|
| <b>입력</b> <i>색상</i> | 처리해야 하는 색상 이미지입니다. |

<a name="outputs"></a>

## 출력

|  |  |
|:---|:---|
| <b>출력</b> <i>색상</i> | 필터링된 색상 이미지. |

<a name="parameters"></a>

## 매개변수

|  |  |
|:---|:---|
| <b>강도</b> *부동* | 이미지에 적용된 필터링의 강도입니다.<br><br>값이 높을수록 더 밝은 영역의 세부 사항과 노이즈가 더 매끄러워집니다. |
| <b>Smoothness</b> *부동* | 구조화 영역에 적용되는 매끄러움의 강도로 인해 더 둥근 영역이 생기며 더 높은 필터링 강도에서 발생할 수 있는 스테핑 효과가 줄어듭니다. |
| <b>조건</b> *정수* | 이미지에서 구조화 영역을 정의할 값을 선택하는 데 사용되는 기준입니다.<br><br>즉, 픽셀을 매끄럽게 만들어야 하는 영역으로 *그룹화*&#x200B;하는 방법입니다.<br><br>*- 분산:* 평균 주위에 분산이 가장 낮은 값을 선택하여 서로 유사한 픽셀 클러스터를 만듭니다.<br>*- 변화 계수:* 평균을 고려하는 동안 값을 선택하여 더 밝은 영역에서 더 적은 변화를 만듭니다. |
| <b>가우스</b> *부울* | 픽셀을 구조화 영역으로 그룹화하려면 가우시안 분포를 사용하십시오.<br><br>True이면 영역이 더 매끄러워지고 병합 효과가 줄어듭니다. |
| <b>알파 영향</b> *부울* | &#39;True&#39;이면 이미지의 알파 채널에도 필터링이 적용됩니다.<br><br>&#39;False&#39;이면 알파 채널이 완전히 무시되고 그대로 출력됩니다. |
| <b>반복</b> *정수* | 필터가 실행된 횟수입니다. 여기서 각 반복은 이전 필터의 결과에 적용됩니다.<br><br>더 많은 반복을 사용하면 영역이 더 평평하고 선명하게 구조화됩니다. |

## 예

<table>
  <tr>
    <td>
      <img src="mlv-color.resources/mlv-color-02.png" alt="MLV_Variant4A">
      <br><i>이전</i>
    </td>
    <td>
      <img src="mlv-color.resources/mlv-color-03.png" alt="MLV_Variant4B">
      <br><i>이후</i>
    </td>
  </tr>
</table>

<table>
  <tr>
    <td>
      <img src="mlv-color.resources/mlv-color-04.png" alt="MLV_Variant5A">
      <br><i>이전</i>
    </td>
    <td>
      <img src="mlv-color.resources/mlv-color-05.png" alt="MLV_Variant5B">
      <br><i>이후</i>
    </td>
  </tr>
</table>

<table>
  <tr>
    <td>
      <img src="mlv-color.resources/mlv-color-06.png" alt="MLV_Variant3A">
      <br><i>이전</i>
    </td>
    <td>
      <img src="mlv-color.resources/mlv-color-07.png" alt="MLV_Variant3B">
      <br><i>이후</i>
    </td>
  </tr>
</table>
