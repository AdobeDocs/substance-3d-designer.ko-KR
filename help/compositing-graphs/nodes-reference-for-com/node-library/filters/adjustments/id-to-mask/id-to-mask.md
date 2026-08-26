---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/adjustments/id-to-mask.html"
breadcrumb-title: ''
description: '[ID를 사용하여 회색 음영 노드를 마스크함]을 사용하여 재료 선택을 위해 ID 맵 값을 회색 음영 마스크로 변환합니다.'
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Adjustments > ID To Mask Grayscale
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 회색 음영 마스크 ID
user-guide-description: ''
user-guide-title: ''
source-git-commit: 5b9c9d12e2ccd76f75ec2a74815f9c68c43c06a2
workflow-type: tm+mt
source-wordcount: '245'
ht-degree: 1%

---


# 회색 음영 마스크 ID

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![회색 음영 아이콘을 마스킹하는 ID](../../../../../../assets/IDToMask.png "회색 음영 아이콘을 마스킹하는 ID"){width="200px"}

<b>내부:</b> 필터 > 조정

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 설명

선택한 픽셀 값을 가진 픽셀이 흰색인 ID 맵에서 마스크를 만듭니다.

ID 맵은 전체(예를 들어, 모양)의 일부인 픽셀들이 모두 동일한 고유 식별 값을 갖는 이미지이다. 이 경우 값은 정수입니다.

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
| <b>ID</b> *회색 음영* 기본 | 마스크를 추출해야 하는 입력 ID 맵입니다. |

## 출력 커넥터

|  |  |
| --- | --- |
| <b>출력</b> *회색 음영* | 입력 ID 맵에서 추출한 이진 마스크입니다. |

## 매개변수

|  |  |
| --- | --- |
| <b>선택 모드</b> *정수* | ID 맵에서 마스크에서 흰색으로 표시되어야 하는 픽셀 값을 선택하는 방법:<ul data-preserve-html="true"> <li data-preserve-html="true"><b>솔로:</b> 단일 픽셀 값 선택</li> <li data-preserve-html="true"><b>범위:</b> 픽셀 값의 범위를 선택합니다.</li> </ul> |
| <b>ID 정수</b> *정수* *&#39;선택 모드&#39;가 &#39;솔로&#39;로 설정된 경우 사용 가능* | ID 맵의 픽셀 값으로, 출력 마스크에서 흰색이어야 합니다. |
| <b>ID 범위</b> *Integer2* *&#39;선택 모드&#39;가 &#39;범위&#39;로 설정된 경우 사용 가능* | ID 맵의 시작부터 끝까지 픽셀 값의 범위입니다. 픽셀값은 출력 마스크에서 흰색이어야 합니다. |

## 예

<table>
  <tr>
    <td>
      <img src="../../../../../../assets/id_to_mask_grayscale_example_1_before.jpg" alt="id_to_mask_grayscale_example_1_before">
      <br><i>이전</i>
    </td>
    <td>
      <img src="../../../../../../assets/id_to_mask_grayscale_example_1_after.jpg" alt="id_to_mask_grayscale_example_1_after">
      <br><i>이후</i>
    </td>
  </tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![마스킹할 ID: 예 2](../../../../../../assets/id_to_mask_example_2.gif "마스킹할 ID: 예 2"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![마스킹할 ID: 예 3](../../../../../../assets/id_to_mask_example_3.png "마스킹할 ID: 예 3"){zoomable="yes"}

</td>
</tr>
</table>
