---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/spline-paths-tools/spline-tools/spline-merge-list.html"
breadcrumb-title: ''
description: 스플라인 병합 목록 노드(Spline Merge List node)를 사용하여 결합된 작업을 위해 여러 스플라인을 단일 스플라인 목록으로 병합합니다.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Spline  Path Tools > Spline Tools > Spline Merge List
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 스플라인 병합 목록
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '354'
ht-degree: 1%

---


# 스플라인 병합 목록

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![노드 아이콘](spline-merge-list.resources/spline-merge-list-01.png "노드 아이콘")

<b>인:</b> 스플라인 및 패스 도구 > 자유 곡선 도구

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 설명

입력 목록의 모든 스플라인을 단일 스플라인으로 병합합니다.

</td>
</tr>
</table>

<a name="inputs"></a>

## 입력

|  |  |
|:---|:---|
| <b>스플라인 코드</b> <i>색상</i> | 색상 이미지의 RGBA 채널로 인코딩된 입력 스플라인의 좌표:<br><b>R</b> - X 위치<br><b>G</b> - Y 위치<br><b>B</b> - Height<br><b>A</b> - 압축된 데이터:<br> - 기호: 스플라인이 닫힘(네거티브) 또는 열림(포지티브);<br> - 절대값: Thickness + 1. |
| <b>스플라인 데이터</b> <i>색상</i> | 색상 이미지의 RGBA 채널에 인코딩된 입력 스플라인의 추가 데이터입니다.<br><b>R</b> - 탄젠트 X<br><b>G</b> - 탄젠트 Y<br><b>B</b> - 미사용<br><b>A</b> - 미사용 |
| <b>스플라인 양</b> <i>정수</i> | 입력 스플라인의 수입니다. |

<a name="outputs"></a>

## 출력

|  |  |
|:---|:---|
| <b>미리 보기</b> <i>회색 음영</i> | 병합된 스플라인을 회색 음영 이미지로 미리 봅니다. |
| <b>스플라인 코드</b> <i>색상</i> | 색상 이미지의 RGBA 채널에 인코딩된 병합된 스플라인의 점의 좌표입니다.<br><b>R</b> - X 위치<br><b>G</b> - Y 위치<br><b>B</b> - Height<br><b>A</b> - 압축된 데이터:<br> - 기호: 스플라인이 닫히거나(음수) 열림(양수);<br> - 절대값: Thickness + 1. |
| <b>스플라인 데이터</b> <i>색상</i> | 색상 이미지의 RGBA 채널에 인코딩된 병합된 스플라인의 추가 데이터입니다.<br><b>R</b> - 탄젠트 X<br><b>G</b> - 탄젠트 Y<br><b>B</b> - 미사용<br><b>A</b> - 미사용 |
| <b>스플라인 양</b> <i>정수</i> | 병합된 스플라인의 수입니다. |

<a name="parameters"></a>

## 매개변수

|  |  |
|:---|:---|
| <b>닫힌 스플라인 거리 임계값</b> <i>부동</i> | 텍스처 공간에서 같은 스플라인의 두 가장자리가 해당 스플라인을 닫는 단일 점으로 처리되는 거리입니다.<br>모양을 스플라인을 따라 분산하거나 이미지를 매핑할 때 겹치지 않도록 합니다. |
| <b>미리 보기</b> |  |
| <b>세그먼트 양</b> <i>정수</i> | 미리 보기 출력에서 스플라인 시각화를 그리는 데 사용되는 선분의 수를 조정합니다.<br>값이 높을수록 선이 더 매끄러워집니다. |
| <b>방향 도우미 표시</b> <i>부울</i> | 미리 보기 출력에서 스플라인의 시작 부분에 점을 표시하고 끝 부분에 화살표를 표시합니다. |
| <b>Thickness 봉투 표시</b> <i>부울</i> | 스플라인 Thickness 모서리에 추가 선을 표시합니다. |
| <b>Thickness(px)</b> <i>부동</i> | 미리 보기 출력에서 스플라인 시각화의 Thickness을 픽셀 단위로 조정합니다. |

## 예

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="spline-merge-list.resources/spline-merge-list-02.jpg" alt="SplineMergeList-Variant2-Before">
      <br><i>이전</i>
    </td>
    <td>
      <img src="spline-merge-list.resources/spline-merge-list-03.jpg" alt="SplineMergeList-Variant2-After">
      <br><i>이후</i>
    </td>
  </tr>
</table>

</td>
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="spline-merge-list.resources/spline-merge-list-04.jpg" alt="SplineMergeList-Variant1-Before">
      <br><i>이전</i>
    </td>
    <td>
      <img src="spline-merge-list.resources/spline-merge-list-05.jpg" alt="SplineMergeList-Variant1-After">
      <br><i>이후</i>
    </td>
  </tr>
</table>

</td>
</tr>
</table>

![노드 데모](spline-merge-list.resources/spline-merge-list-06.gif "노드 데모")
