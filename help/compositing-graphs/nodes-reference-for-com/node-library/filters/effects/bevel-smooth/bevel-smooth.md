---
helpx_url: "https://helpx.adobe.com/kr/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/bevel-smooth.html"
breadcrumb-title: ''
description: 베벨 매끄럽게 노드를 사용하여 모양과 패턴에 사실적인 표면을 만들기 위해 경사진 가장자리를 매끄럽게 만듭니다.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Bevel smooth
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 베벨 매끄럽게
user-guide-description: ''
user-guide-title: ''
source-git-commit: 27326c60e0247617a8f57554a68c9663934cd2bc
workflow-type: tm+mt
source-wordcount: '598'
ht-degree: 0%

---


# 베벨 매끄럽게

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![비등방성 구와하라 회색 음영 아이콘](../../../../../../assets/bevel_smooth.png "비등방성 구와하라 회색 음영 아이콘"){width="200px"}

<b>인:</b> 필터 > 효과

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 설명

마스크 테두리에서 바깥쪽이나 안쪽으로 또는 둘 모두로 그래디언트 또는 플랫 색상을 그립니다.

겹쳐진 그레이디언트는 가장 가까운 경계까지의 거리가 그려지도록 반전된 정규화된 거리로 정렬됩니다.

거리 맵을 사용하여 테두리를 따라 그레이디언트의 거리를 동적으로 조정할 수 있습니다.

</td>
</tr>
</table>

>[!TIP]
>
> [방향 거리](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/directional-distance/directional-distance.md) 노드는 유사한 기능을 제공하며, 이 경우 확장이 특정 방향으로 수행됩니다.

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
| <b>마스크 입력</b> *회색 음영* 기본 | 마스크를 추출해야 하는 이미지입니다.   해당 마스크에서 &#39;마스크 임계값&#39; 값을 초과하는 모든 값은 흰색입니다. |
| <b>원본 입력</b> *회색 음영* | &#39;출력 모드&#39; 매개 변수가 &#39;확장&#39;으로 설정된 경우에만 사용되는 선택적 입력입니다.   이 경우 마스크의 흰색 영역에 이 이미지가 겹쳐지고 테두리의 회색 음영 값이 확장됩니다. |
| <b>거리 맵</b> *회색 음영* | &#39;거리 맵 승수&#39; 매개 변수 값이 0보다 높을 때 사용되는 선택적 입력입니다.   마스크의 테두리를 따라 경사/확장 거리를 조정하는 데 사용되며, 여기서 값이 더 어두우면 거리가 더 짧아집니다. |

## 출력 커넥터

|  |  |
| --- | --- |
| <b>출력</b> *회색 음영* | 선택한 &#39;출력 모드&#39;에 따른 결과 이미지 |
| <b>UV</b> *색상* | 마스크 테두리를 따라 UV가 확대되는 UV 맵   이렇게 확장된 UV를 사용하여 다른 이미지를 매핑하도록 [UV 매퍼](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/spline-tools/uv-mapper-color/uv-mapper-color.md) 노드에 연결할 수 있습니다. |

## 매개변수

|  |  |
| --- | --- |
| <b>출력 모드</b> *정수* | 마스크 테두리를 확장하는 방법:<ul data-preserve-html="true"> <li data-preserve-html="true"><b>경사:</b> 최대 &#39;거리&#39;에서 0에 도달하는 1부터 0까지 그레이디언트를 그립니다.</li> <li data-preserve-html="true"><b>확장:</b> &#39;최대 거리&#39;까지 단색을 그립니다. 이 색상은 흰색이거나 마스크 테두리의 색상 &#39;소스 입력&#39; 이미지(연결된 경우)입니다.</li> <li data-preserve-html="true"><b>거리:</b> 이미지에서 가장 짧은 변의 길이인 1인 정규화된 이미지 공간에서 가장 가까운 마스크 테두리로부터의 원시 거리입니다</li> </ul> |
| <b>방향</b> *정수* *&#39;출력 모드&#39;가 &#39;경사&#39; 또는 &#39;확장&#39;으로 설정된 경우 사용 가능* | 확장해야 하는 마스크 테두리의 측면:<ul data-preserve-html="true"> <li data-preserve-html="true"><b>내부:</b> 마스크 내부로 그리기</li> <li data-preserve-html="true"><b>아웃:</b> 마스크 바깥쪽으로 그리기</li> <li data-preserve-html="true"><b>시작/종료:</b> 마스크 내부와 외부 양쪽으로 그립니다.</li> </ul> |
| <b>최대 거리</b> *부동* | 1이 입력 영상의 짧은 변의 길이인 정규화된 영상 공간에서 확장의 거리이다. |
| <b>마스크 Smoothness</b> *부동* | 마스크에 적용된 매끄러움 강도입니다.   값은 흐림 효과의 반경이며, 1단위는 이미지의 1/256입니다. |
| <b>마스크 오프셋</b> *부동* | 마스크 테두리를 안쪽 또는 바깥쪽으로 이동합니다. |
| <b>마스크 임계값</b> *부동* | &#39;마스크 입력&#39; 이미지에서 마스크 테두리를 감지하는 데 사용되는 값입니다.   이 임계값 이상의 값은 마스크 모양의 *내부*&#x200B;이고, 아래의 값은 *외부*&#x200B;입니다. |
| <b>크기 조절</b> *Float2* | 확장의 가로(X) 및 세로(Y) 거리를 조정합니다.   이러한 값은 &#39;최대 거리&#39; 매개 변수 값에 대한 승수입니다. |
| <b>거리 맵 승수</b> *정수* | &#39;최대 거리&#39;에 대한 &#39;거리 맵&#39;의 영향을 조정합니다. |

## 예

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![베벨 매끄럽게: 예 1](../../../../../../assets/bevel_smooth_example_1.gif "베벨 매끄럽게: 예 1"){width="1024px" zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![베벨 매끄럽게: 예 8](../../../../../../assets/bevel_smooth_example_8.jpg "베벨 매끄럽게: 예 8"){width="1024px" zoomable="yes"}

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="../../../../../../assets/bevel_smooth_example_4_before.jpg" alt="bevel_smooth_example_4_before">
      <br><i>이전</i>
    </td>
    <td>
      <img src="../../../../../../assets/bevel_smooth_example_4_after.jpg" alt="bevel_smooth_example_4_after">
      <br><i>이후</i>
    </td>
  </tr>
</table>

</td>
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="../../../../../../assets/bevel_smooth_example_2_before.jpg" alt="bevel_smooth_example_2_before">
      <br><i>이전</i>
    </td>
    <td>
      <img src="../../../../../../assets/bevel_smooth_example_2_after.jpg" alt="bevel_smooth_example_2_after">
      <br><i>이후</i>
    </td>
  </tr>
</table>

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="../../../../../../assets/bevel_smooth_example_3_before.jpg" alt="bevel_smooth_example_3_before">
      <br><i>이전</i>
    </td>
    <td>
      <img src="../../../../../../assets/bevel_smooth_example_3_after.jpg" alt="bevel_smooth_example_3_after">
      <br><i>이후</i>
    </td>
  </tr>
</table>

</td>
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="../../../../../../assets/bevel_smooth_example_5_before.jpg" alt="bevel_smooth_example_5_before">
      <br><i>이전</i>
    </td>
    <td>
      <img src="../../../../../../assets/bevel_smooth_example_5_after.jpg" alt="bevel_smooth_example_5_after">
      <br><i>이후</i>
    </td>
  </tr>
</table>

</td>
</tr>
</table>

<table>
  <tr>
    <td>
      <img src="../../../../../../assets/bevel_smooth_example_7_before.jpg" alt="bevel_smooth_example_7_before">
      <br><i>이전</i>
    </td>
    <td>
      <img src="../../../../../../assets/bevel_smooth_example_7_after.jpg" alt="bevel_smooth_example_7_after">
      <br><i>이후</i>
    </td>
  </tr>
</table>
