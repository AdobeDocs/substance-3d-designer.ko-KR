---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/normal-map/normal-uncombine.html"
breadcrumb-title: ''
description: 결합된 표준 맵 데이터를 개별 X, Y 및 Z 구성 요소로 분리하려면 표준 결합 해제 노드를 사용합니다.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Normal map > Normal uncombine
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 표준 결합 해제
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '213'
ht-degree: 2%

---


# 표준 결합 해제

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![표준 결합 해제 아이콘](normal-uncombine.resources/NormalUncombine.png "표준 결합 해제 아이콘"){width="200px"}

<b>내부:</b> 필터 > 표준 맵

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 설명

표준 맵에서 Height 맵으로 설명하는 서피스 세부 정보를 제거합니다.

</td>
</tr>
</table>

<a name="inputs"></a>

## 입력

|  |  |
|:---|:---|
| <b>결합된 표준</b> 기본 <i>색상</i> | 세부 정보를 제거해야 하는 일반 맵입니다. |
| <b>Height</b> <i>회색 음영</i> | Height 맵은 결합된 표준 맵에서 제거해야 할 표면 세부 정보를 나타냅니다. |

<a name="outputs"></a>

## 출력

|  |  |
|:---|:---|
| <b>결합되지 않은 정상</b> <i>색상</i> | 입력 Height 맵에 의해 기술된 표면 세부 정보가 제거된 표준 맵. |
| <b>추정 강도</b> <i>부동</i> | 입력 표준 맵의 강도와 일치하도록 입력 Height 맵에 연결된 [표준](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/normal/normal.md) 노드로 설정되어야 하는 강도의 추정치입니다. |

<a name="parameters"></a>

## 매개변수

|  |  |
|:---|:---|
| <b>일반 형식</b> *정수* | 입력 표준 맵의 형식입니다. 녹색 채널을 효과적으로 반전합니다.<ul data-preserve-html="true"> <li data-preserve-html="true"><b>DirectX:</b> Y축이 위쪽을 가리킵니다.</li> <li data-preserve-html="true"><b>OpenGL:</b> Y축은 아래를 가리킵니다.</li> </ul> |

## 예

<table>
  <tr>
    <td>
      <img src="normal-uncombine.resources/normal_uncombine_example_3_before.jpg" alt="normal_uncombine_example_3_before">
      <br><i>이전</i>
    </td>
    <td>
      <img src="normal-uncombine.resources/normal_uncombine_example_3_after.jpg" alt="normal_uncombine_example_3_after">
      <br><i>이후</i>
    </td>
  </tr>
</table>

![일반 결합 해제: 예 2](normal-uncombine.resources/normal_uncombine_example_4.png "일반 결합 해제: 예 2"){zoomable="yes"}

<table>
  <tr>
    <td>
      <img src="normal-uncombine.resources/normal_uncombine_example_1_before.jpg" alt="normal_uncombine_example_1_before">
      <br><i>이전</i>
    </td>
    <td>
      <img src="normal-uncombine.resources/normal_uncombine_example_1_after.jpg" alt="normal_uncombine_example_1_after">
      <br><i>이후</i>
    </td>
  </tr>
</table>

![일반 결합 해제: 예 4](normal-uncombine.resources/normal_uncombine_example_6.png "일반 결합 해제: 예 4"){zoomable="yes"}

<table>
  <tr>
    <td>
      <img src="normal-uncombine.resources/normal_uncombine_example_2_before.jpg" alt="normal_uncombine_example_2_before">
      <br><i>이전</i>
    </td>
    <td>
      <img src="normal-uncombine.resources/normal_uncombine_example_2_after.jpg" alt="normal_uncombine_example_2_after">
      <br><i>이후</i>
    </td>
  </tr>
</table>

![일반 결합 해제: 예 6](normal-uncombine.resources/normal_uncombine_example_5.png "일반 결합 해제: 예 6"){zoomable="yes"}
