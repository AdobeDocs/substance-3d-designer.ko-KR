---
helpx_url: "https://helpx.adobe.com/kr/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/adjustments/histogram-equalize.html"
breadcrumb-title: ''
description: 히스토그램 균일화 노드를 사용하여 대비 및 밝기를 개선하기 위해 픽셀 강도를 재분포합니다.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Adjustments > Histogram equalize
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 막대 그래프 균일화
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '184'
ht-degree: 2%

---


# 막대 그래프 균일화

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![막대 그래프 균일화: 아이콘](histogram-equalize.resources/histogram_equalize.png "막대 그래프 균일화: 아이콘"){width="200px"}

<b>내부:</b> 필터 > 조정

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 설명

회색 음영 이미지에 대한 막대 그래프를 균일화하여 동일한 분포를 목표로 회색 음영 값을 효과적으로 조정합니다.

</td>
</tr>
</table>

<a name="inputs"></a>

## 입력

|  |  |
|:---|:---|
| <b>입력</b> <i>회색 음영</i> 기본 | 막대 그래프를 균일화할 이미지입니다. |

<a name="outputs"></a>

## 출력

|  |  |
|:---|:---|
| <b>출력</b> <i>회색 음영</i> | 막대 그래프 균일화가 적용된 결과 이미지. |

<a name="parameters"></a>

## 매개변수

|  |  |
|:---|:---|
| <b>막대 그래프 해상도</b> *정수* | 막대 그래프의 폭입니다. 값이 높을수록 더 세밀한 값 배포가 가능합니다.   사용 가능한 해상도는 픽셀 단위로 256, 512, 1024, 2048, 4096입니다. |
| <b>막대 그래프 매끄럽게</b> *부동* | 이미지의 회색 음영 값을 재분포하여 각 값 간의 *차이*&#x200B;를 균일화하여 막대 그래프를 다듬을 수 있습니다.   이 매개 변수는 보정 강도를 조정합니다. |

## 예

<table>
  <tr>
    <td>
      <img src="histogram-equalize.resources/histogram_equalize_example_1_before.jpg" alt="histogram_equalize_example_1_before">
      <br><i>이전</i>
    </td>
    <td>
      <img src="histogram-equalize.resources/histogram_equalize_example_1_after.jpg" alt="histogram_equalize_example_1_after">
      <br><i>이후</i>
    </td>
  </tr>
</table>

![막대 그래프 균일화: 예 1](histogram-equalize.resources/histogram_equalize_example_3.png "막대 그래프 균일화: 예 1"){zoomable="yes"}

<table>
  <tr>
    <td>
      <img src="histogram-equalize.resources/histogram_equalize_example_2_before.jpg" alt="histogram_equalize_example_2_before">
      <br><i>이전</i>
    </td>
    <td>
      <img src="histogram-equalize.resources/histogram_equalize_example_2_after.jpg" alt="histogram_equalize_example_2_after">
      <br><i>이후</i>
    </td>
  </tr>
</table>

![막대 그래프 균일화: 예 2](histogram-equalize.resources/histogram_equalize_example_5.png "막대 그래프 균일화: 예 2"){zoomable="yes"}

<table>
  <tr>
    <td>
      <img src="histogram-equalize.resources/histogram_equalize_example_4_before.jpg" alt="histogram_equalize_example_4_before">
      <br><i>이전</i>
    </td>
    <td>
      <img src="histogram-equalize.resources/histogram_equalize_example_4_after.jpg" alt="histogram_equalize_example_4_after">
      <br><i>이후</i>
    </td>
  </tr>
</table>

![막대 그래프 균일화: 예 3](histogram-equalize.resources/histogram_equalize_example_6.png "막대 그래프 균일화: 예 3"){zoomable="yes"}
