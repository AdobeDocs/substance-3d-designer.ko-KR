---
helpx_url: "https://helpx.adobe.com/kr/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/adjustments/histogram-compute.html"
breadcrumb-title: ''
description: '[히스토그램 계산] 노드를 사용하여 분석 및 처리를 위한 텍스처의 히스토그램 데이터를 계산합니다.'
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Adjustments > Histogram compute
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 히스토그램 컴퓨팅
user-guide-description: ''
user-guide-title: ''
source-git-commit: 27326c60e0247617a8f57554a68c9663934cd2bc
workflow-type: tm+mt
source-wordcount: '315'
ht-degree: 1%

---


# 히스토그램 컴퓨팅

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![막대 그래프 계산: 아이콘](../../../../../../assets/histogram_compute.png "막대 그래프 계산: 아이콘"){width="200px"}

<b>내부:</b> 필터 > 조정

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 설명

회색 음영 이미지에 대한 막대 그래프를 계산합니다.

막대 그래프는 이미지의 픽셀 행으로 인코딩됩니다. 여기서 각 픽셀 값은 X축의 픽셀 위치와 일치하는 색상 값의 *모집단*&#x200B;입니다.\
예를 들어, (0.25, 0)에서 75의 픽셀 값은 이미지에 0.25 색상 값을 갖는 75개의 픽셀이 있음을 의미합니다.

</td>
</tr>
</table>

또한 노드는 이미지에 대해 계산된 *누적 분포 함수*(CDF)을 출력합니다.

&#39;예제&#39; 섹션에 나와 있는 것처럼 사용자 정의 마스크와 같이 노드에서 계산한 데이터를 사용하여 사용자 정의 도구를 만들 수 있습니다.

>[!IMPORTANT]
>
> [0,1] 범위를 벗어나는 모든 값은 클램핑되므로, 히스토그램이 HDR 이미지에 대해 정확하지 않을 수 있다.

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
| <b>입력</b> *회색 음영* 기본 | 히스토그램을 계산할 이미지입니다. |

## 출력 커넥터

|  |  |
| --- | --- |
| <b>막대 그래프</b> *회색 음영* | 입력 이미지에 대해 계산된 막대 그래프로, 각 픽셀 값이 X축의 픽셀 위치와 일치하는 색상 값의 *모집단*&#x200B;인 픽셀 행으로 인코딩됩니다.   예를 들어, (0.25, 0)에서 75의 픽셀 값은 이미지에 0.25 색상 값을 갖는 75개의 픽셀이 있음을 의미합니다. |
| <b>CDF</b> *회색 음영* | 이미지에 대해 계산한 *누적 분포 함수*(CDF)의 결과로, 픽셀 행으로 인코딩됩니다. 여기서 각 픽셀은 왼쪽에 있는 모든 픽셀 값의 합계입니다.   그 합계는 이미지의 총 픽셀 수에 대해 *정규화*&#x200B;됩니다. |

## 매개변수

|  |  |
| --- | --- |
| <b>막대 그래프 해상도</b> *정수* | 막대 그래프의 폭입니다. 값이 높을수록 더 세밀한 값 배포가 가능합니다.   사용 가능한 해상도는 픽셀 단위로 256, 512, 1024, 2048, 4096입니다. |

## 예

![막대 그래프 계산: 예 1](../../../../../../assets/histogram_compute_example_1.jpg "막대 그래프 계산: 예 1"){zoomable="yes"}

<table>
  <tr>
    <td>
      <img src="../../../../../../assets/histogram_compute_example_2_before.jpg" alt="histogram_compute_example_2_before">
      <br><i>이전</i>
    </td>
    <td>
      <img src="../../../../../../assets/histogram_compute_example_2_after.jpg" alt="histogram_compute_example_2_after">
      <br><i>이후</i>
    </td>
  </tr>
</table>
