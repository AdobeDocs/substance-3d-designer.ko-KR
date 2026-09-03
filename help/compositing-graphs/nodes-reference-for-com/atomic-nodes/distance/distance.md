---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/atomic-nodes/distance.html"
breadcrumb-title: ''
description: 거리 노드를 사용하여 모양에서 마스크 및 절차 효과를 만들기 위한 거리 맵을 계산합니다.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Atomic nodes > Distance
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 거리
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '398'
ht-degree: 8%

---


# 거리

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Atomic node: Distance](distance.resources/distance-01.png "Atomic node: Distance"){width="200px"}

</td>
<td width="100.00%" style="border: 0;" valign="top">

마스크에서 가장 가까운 흰색 픽셀의 위치를 찾아 해당 위치에서 그레이디언트를 출력하거나 소스 이미지의 해당 위치에서 색상을 출력합니다.

이 노드는 0.5 회색 음영 값 이상의 입력 최대값에 있는 모든 픽셀에서 바깥쪽 선형 페이드(그레이디언트)를 만듭니다.

</td>
</tr>
</table>

팽창하는 바깥쪽 페이드는 그것이 다른 전지를 만나자마자 종결될 것이다: 그것들은 결코 겹치지 않을 것이다. 내부적으로 실제로 거리를 계산하여 0.5보다 작은 픽셀까지의 거리를 표시하고 거리 노드를 클램프/최대값으로 설정합니다.

선택적 소스 맵을 사용하면 보조 입력 맵의 텍스처와 셀을 결합할 수 있습니다.

거리 노드는 마스터하기 쉬운 노드는 아니지만 기존 마스크를 신뢰할 수 있는 방식으로 확장(흐림 및 대비 조정)하고, 보로노이(Voronoi)형 노이즈 셀을 생성하며, 선명한 선형 프로파일을 사용하여 기존 모양을 베벨(나중에 다시 매핑할 수 있음)하는 것이 주요 사용 사례입니다.

자세한 내용은 아래 [예](#examples)를 참조하세요.

<table>
<tr style="border: 0;">
<td width="100.00%" style="border: 0;" valign="top">



</td>
<td width="83.33%" style="border: 0;" valign="top">



</td>
<td width="100.00%" style="border: 0;" valign="top">



</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

## 출력 커넥터

</td>
<td style="border: 0;" valign="top">

### 예

</td>
</tr>
</table>

## 매개변수

|  |  |
| --- | --- |
| <b>색상 모드</b> *부울* | 회색 음영과 색상 출력 이미지 사이를 전환합니다. &#39;원본 입력&#39; 입력 유형도 변경합니다. |
| <b>최대 거리</b> *부동* | 마스크에서 가장 가까운 테두리를 감지하기 위한 최대 거리를 픽셀 단위로 조정합니다. |
| <b>소스/거리 결합</b> *부울* | 선택 사항인 &#39;원본 입력&#39;이 최종 셀과 결합되는 방법을 결정합니다.<ul data-preserve-html="true"> <li data-preserve-html="true"><i>결합:</i> &#39;소스 입력&#39; 값을 페이드 선형 마스크와 결합합니다. &#39;소스 입력&#39; 입력이 연결된 경우 해당 값은 계산된 거리와 결합됩니다.</li> <li data-preserve-html="true"><i>원본만:</i> &#39;원본 입력&#39;에서 단색으로 표시됩니다.</li> </ul> |
| <b>거리 모드</b> *정수* | 추출된 마스크에서 가장 가까운 경계까지의 거리를 계산하는 방법을 선택합니다.<ul data-preserve-html="true"> <li data-preserve-html="true"><i>유클리드:</i> 제곱 X/Y 차이의 합계.</li> <li data-preserve-html="true"><i>맨해튼:</i> X/Y 차이의 절대값의 합계</li> <li data-preserve-html="true"><i>Chebyshev:</i> X/Y 차이의 절대 값의 최대값입니다.</li> </ul>  <div><img alt="거리 모드 예" class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_table_copy_copy_copy_row-yj03rtt-column-0i13nfd_image" src="distance.resources/distance-02.jpg" title="거리 모드 예"/></div> |

## 입력 커넥터

|  |  |
| --- | --- |
| <b>마스크 입력</b> *회색 음영* 기본 | 거리 값을 계산해야 하는 테두리가 있는 회색 음영 마스크입니다.   이미지에서 0.5의 임계값을 사용하여 이진 마스크를 추출합니다. 이 임계값 위의 모든 값은 흰색이고 그 아래의 모든 값은 검정입니다. |
| <b>원본 입력</b> *색상/회색 음영* | &#39;마스크 입력&#39;에서 가장 가까운 테두리의 픽셀 값을 복사해야 하는 선택적 회색 음영 이미지입니다. |

## 출력 커넥터

|  |  |
| --- | --- |
| <b>출력</b> *색상/회색 음영* |  |

## 예

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](distance.resources/distance-03.gif){width="250px"}

</td>
<td style="border: 0;" valign="top">

![](distance.resources/distance-04.gif){width="250px"}

</td>
<td style="border: 0;" valign="top">

![](distance.resources/distance-05.gif){width="250px"}

</td>
</tr>
</table>
