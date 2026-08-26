---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/curvature-smooth.html"
breadcrumb-title: ''
description: 표면 세부 정보 추출을 위해 Height 맵에서 부드러운 곡률 맵을 생성하려면 곡률(Curvature) 부드러운(Smooth) 노드를 사용합니다.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Curvature Smooth
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 곡률 매끄럽게
user-guide-description: ''
user-guide-title: ''
source-git-commit: 5b9c9d12e2ccd76f75ec2a74815f9c68c43c06a2
workflow-type: tm+mt
source-wordcount: '296'
ht-degree: 1%

---


# 곡률 매끄럽게

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![곡률 부드러운 노드 아이콘](../../../../../../assets/CurvatureSmooth.png "곡률 부드러운 노드 아이콘"){width="200px"}

<b>인:</b> 필터 > 효과

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 설명

수직 맵으로 설명하는 서피스의 곡률을 계산합니다.

곡률 맵은 서피스의 오목 및 볼록 영역을 나타냅니다.\
밝은 영역은 50% 회색입니다. 볼록 영역은 더 밝고 오목 영역은 더 어둡습니다.

</td>
</tr>
</table>

오목 및 볼록 영역도 자체 출력으로 분할되어, 이러한 특성에 따라 영역을 더 쉽게 선택하거나 마스크할 수 있습니다.

>[!TIP]
>
> 더 선명한 버전은 [곡률](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/curvature-filter-node/curvature-filter-node.md)을 참조하거나 추가 옵션이 필요한 경우에는 [곡률 소벨](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/curvature-sobel/curvature-sobel.md)을 참조하세요.

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
| <b>표준</b> *색상* <b>기본</b> | 곡률을 계산해야 하는 서피스를 설명하는 표준 맵입니다. |

## 출력 커넥터

|  |  |
| --- | --- |
| <b>곡률</b> *회색 음영* | 입력된 표준 맵에서 계산된 곡률 맵입니다.   밝은 영역은 50% 회색입니다. 볼록 영역은 더 밝고 오목 영역은 더 어둡습니다. |
| <b>볼록함</b> *회색 음영* | 입력된 표준 맵에서 계산된 볼록도 맵입니다.   영역이 볼록할수록 지도에서의 밝은 영역입니다.  평면 또는 오목 영역은 검정색입니다. |
| <b>오목</b> *회색 음영* | 입력된 표준 맵에서 계산된 오목한 맵입니다.   오목한 영역이 많을수록 지도에서 더 밝아집니다.  평면 또는 볼록 영역은 검정색입니다. |

## 매개변수

|  |  |
| --- | --- |
| <b>일반 형식</b> *정수* | 입력 표준 맵의 형식입니다. 녹색 채널을 효과적으로 반전합니다.<ul data-preserve-html="true"> <li data-preserve-html="true"><b>DirectX:</b> Y축이 위쪽을 가리킵니다.</li> <li data-preserve-html="true"><b style="">OpenGL:</b> Y축은 아래를 가리킵니다.</li> </ul> |

## 예

<table>
  <tr>
    <td>
      <img src="../../../../../../assets/curvature_smooth_example_1_before.jpg" alt="curvature_smooth_example_1_before">
      <br><i>이전</i>
    </td>
    <td>
      <img src="../../../../../../assets/curvature_smooth_example_1_after.jpg" alt="curvature_smooth_example_1_after">
      <br><i>이후</i>
    </td>
  </tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![곡률 매끄럽게: 예제 2](../../../../../../assets/curvature_smooth_example_2.jpg "곡률 매끄럽게: 예제 2"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![곡률 매끄럽게: 예 3](../../../../../../assets/curvature_smooth_example_3.jpg "곡률 매끄럽게: 예 3"){zoomable="yes"}

</td>
</tr>
</table>

<table>
  <tr>
    <td>
      <img src="../../../../../../assets/curvature_smooth_example_4_before.jpg" alt="curvature_smooth_example_4_before">
      <br><i>이전</i>
    </td>
    <td>
      <img src="../../../../../../assets/curvature_smooth_example_4_after.jpg" alt="curvature_smooth_example_4_after">
      <br><i>이후</i>
    </td>
  </tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![곡률 매끄럽게: 예 4](../../../../../../assets/curvature_smooth_example_5.jpg "곡률 매끄럽게: 예 4"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![곡률 매끄럽게: 예 5](../../../../../../assets/curvature_smooth_example_6.jpg "곡률 매끄럽게: 예 5"){zoomable="yes"}

</td>
</tr>
</table>
