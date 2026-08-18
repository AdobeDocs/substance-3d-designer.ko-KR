---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/adjustments/histogram-render.html"
breadcrumb-title: ''
description: 히스토그램 렌더링 노드를 사용하여 히스토그램 데이터를 분석 및 디버깅을 위한 텍스처로 시각화합니다.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Adjustments > Histogram render
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 히스토그램 렌더링
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '220'
ht-degree: 1%

---


# 히스토그램 렌더링

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![비등방성 구와하라 회색 음영 아이콘](../../../../../../assets/histogram_render.png "비등방성 구와하라 회색 음영 아이콘"){width="200px"}

<b>내부:</b> 필터 > 조정

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 설명

회색 음영 이미지에 대한 막대 그래프를 그립니다.

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
| <b>입력</b> *회색 음영* 기본 | 히스토그램을 그릴 이미지입니다. |

## 출력 커넥터

|  |  |
| --- | --- |
| <b>출력</b> *회색 음영* | 입력 이미지에서 계산된 막대 그래프 시각화입니다. |

## 매개변수

|  |  |
| --- | --- |
| <b>막대 그래프 해상도</b> *정수* | 막대 그래프의 폭입니다. 값이 높을수록 더 세밀한 값 배포가 가능합니다.   사용 가능한 해상도는 픽셀 단위로 256, 512, 1024, 2048, 4096입니다. |
| <b>자동 크기 조절</b> *부울* | &#39;True&#39;이면 이미지의 전체 Height을 사용하도록 막대 그래프를 다시 매핑합니다.   &#39;False&#39;인 경우 각 열은 입력 이미지에 값이 발생한 Height 픽셀 수만큼 픽셀을 사용합니다. |
| <b>크기 조절</b> *부동* | 히스토그램의 크기를 세로로 조절합니다. 여기서 1의 값은 히스토그램의 최대 Height이 됩니다. |
| <b>샘플링</b> *정수* | 막대 그래프 이미지를 필터링하는 방법은 막대 그래프 해상도 및 렌더링 해상도가 일치하지 않는 경우 결과에 영향을 줍니다.<ul data-preserve-html="true"> <li data-preserve-html="true"><b>쌍선형:</b>은 히스토그램에 쌍선형 필터링을 적용하여 보간된 점을 만듭니다.</li> <li data-preserve-html="true"><b>가장 가까운 픽셀:</b>은(는) 필터링하지 않고 가장 가까운 픽셀을 샘플링하므로 단계가 균일해집니다</li> </ul> |
| <b>Y축 뒤집기</b> *부울* | &#39;True&#39;이면 히스토그램을 세로로 미러링합니다. |

## 예

![막대 그래프 렌더링: 예 1](../../../../../../assets/histogram_render_example_1.png "막대 그래프 렌더링: 예 1"){zoomable="yes"}

![막대 그래프 렌더링: 예 2](../../../../../../assets/histogram_render_example_2.png "막대 그래프 렌더링: 예 2"){zoomable="yes"}
