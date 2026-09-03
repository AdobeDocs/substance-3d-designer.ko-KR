---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/spline-paths-tools/spline-tools/spline-cubic.html"
breadcrumb-title: ''
description: 스플라인 큐빅 노드를 사용하여 곡선 경로에 대한 네 개의 제어점으로 매끄러운 큐빅 스플라인을 생성합니다.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Spline  Path Tools > Spline Tools > Spline (Cubic)
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 스플라인(큐빅)
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '777'
ht-degree: 0%

---


# 스플라인(큐빅)

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![노드 아이콘](spline-cubic.resources/spline-cubic-01.png "노드 아이콘")

<b>인:</b> 스플라인 및 패스 도구 > 자유 곡선 도구

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 설명

임의의 위치에서 두 점 <b>p1 </b>과(와) <b>p2</b> 사이의 단일 스플라인을 생성합니다.

스플라인의 궤적은 <b>p1</b>의 &#39;out&#39; 탄젠트와 <b>p2</b>의 &#39;in&#39; 탄젠트로 제어됩니다.

</td>
</tr>
</table>

<a name="inputs"></a>

## 입력

|  |  |
|:---|:---|
| <b>미리 보기</b> <i>회색 음영</i> | 입력 미리보기가 회색 음영 이미지로 분할됩니다. |
| <b>스플라인 코드</b> <i>색상</i> | 색상 이미지의 RGBA 채널로 인코딩된 입력 스플라인의 좌표:<br><b>R</b> - X 위치<br><b>G</b> - Y 위치<br><b>B</b> - Height<br><b>A</b> - 압축된 데이터:<br>- 기호: 스플라인이 닫힘(음수) 또는 열림(양수);<br>- 절대값: Thickness + 1. |
| <b>스플라인 데이터</b> <i>색상</i> | 색상 이미지의 RGBA 채널에 인코딩된 입력 스플라인의 추가 데이터입니다.<br><b>R</b> - 탄젠트 X<br><b>G</b> - 탄젠트 Y<br><b>B</b> - 미사용<br><b>A</b> - 미사용 |
| <b>스플라인 양</b> <i>정수</i> | 입력 스플라인의 수입니다. |

<a name="outputs"></a>

## 출력

|  |  |
|:---|:---|
| <b>미리 보기</b> <i>회색 음영</i> | 출력 미리 보기가 회색 음영 이미지로 분할됩니다. |
| <b>스플라인 코드</b> <i>색상</i> | 색상 이미지의 RGBA 채널로 인코딩된 출력 스플라인의 좌표입니다.<br><b>R</b> - X 위치<br><b>G</b> - Y 위치<br><b>B</b> - Height<br><b>A</b> - 압축된 데이터:<br>- 기호: 스플라인이 닫힘(음수) 또는 열림(양수);<br>- 절대값: Thickness + 1. |
| <b>스플라인 데이터</b> <i>색상</i> | 색상 이미지의 RGBA 채널로 인코딩된 출력 스플라인의 추가 데이터입니다.<br><b>R</b> - 탄젠트 X<br><b>G</b> - 탄젠트 Y<br><b>B</b> - 미사용<br><b>A</b> - 미사용 |
| <b>스플라인 양</b> <i>정수</i> | 출력 스플라인의 수입니다. |

<a name="parameters"></a>

## 매개변수

|  |  |
|:---|:---|
| <b>방향 뒤집기</b> <i>부울</i> | 스플라인의 방향을 반전합니다. |
| <b>입력 스플라인 추가</b> <i>부울</i> | 생성된 스플라인을 <b>스플라인</b> 입력에 연결된 스플라인 목록의 끝에 추가합니다. |
| <b>정사각형이 아닌 수정</b> <i>부울</i> | 점의 위치와 Thickness을 조정하여 정사각형이 아닌 해상도에서 스플라인 모양을 유지합니다. 이는 또한 균일한 분포에도 영향을 미친다. |
| <b>Height</b> |  |
| <b>시작 Height</b> <i>부동</i> | 값이 낮을수록 위치가 낮거나 깊은 p1 지점의 Height을 조정합니다. 이는 p1에서의 스플라인 Height에 영향을 줍니다. |
| <b>최종 Height</b> <i>부동</i> | 값이 낮을수록 위치가 낮거나 깊은 p2 지점의 Height을 조정합니다. 이는 p2에서의 스플라인 Thickness에 영향을 줍니다. |
| <b>자동 접선 Height</b> <i>부울</i> | 시작 Height에서 끝 Height으로 선형으로 보간할 스플라인 탄젠트의 Height을 자동으로 설정합니다. |
| <b>p1 접선 Height</b> <i>부동</i>(&#39;자동 접선 Height&#39;가 True인 경우 사용 가능) | p1 지점 &#39;out&#39; 접선의 Height을 조정합니다. 값이 낮을수록 위치가 더 낮거나 깊어집니다. 이는 p1에서 멀어질 때 스플라인을 따라 Height에 영향을 미칩니다. |
| <b>p2 접선 Height</b> <i>부동</i>(&#39;자동 접선 Height&#39;가 True인 경우 사용 가능) | p2 지점 &#39;in&#39; 접선의 Height을 조정합니다. 값이 낮을수록 위치가 더 낮거나 깊어집니다. 이는 p2에서 멀어질 때 스플라인을 따라 Height에 영향을 미칩니다. |
| <b>Thickness</b> |  |
| <b>시작 Thickness</b> <i>부동</i> | p1 지점의 Thickness을 조정합니다. 이는 p1에서의 스플라인 Thickness에 영향을 줍니다.<br>참고: Thickness은 특정 스플라인 노드에서 사용됩니다. |
| <b>최종 Thickness</b> <i>부동</i> | p2 지점의 Thickness을 조정합니다. 이는 p2에서의 스플라인 Thickness에 영향을 줍니다.<br>참고: Thickness은 특정 스플라인 노드에서 사용됩니다. |
| <b>자동 접선 Thickness</b> <i>부울</i> | 시작 Thickness에서 끝 Thickness으로 선형으로 보간되도록 스플라인 접선의 Thickness을 자동으로 설정합니다.<br>참고: Thickness은 특정 스플라인 노드에서 사용됩니다. |
| <b>p1 접선 Thickness</b> <i>부동</i>(&#39;자동 접선 Thickness&#39;가 True인 경우 사용 가능) | p1 지점 &#39;out&#39; 접선의 Thickness을 조정합니다. 이는 p1에서 멀어질 때 스플라인을 따라 Thickness에 영향을 줍니다.<br>참고: Thickness은 특정 스플라인 노드에서 사용됩니다. |
| <b>p2 접선 Thickness</b> <i>부동</i>(&#39;자동 접선 Thickness&#39;가 True인 경우 사용 가능) | p2 지점 &#39;in&#39; 접선의 Thickness을 조정합니다. 이는 p2에서 멀어질 때 스플라인을 따라 Thickness에 영향을 줍니다.<br>참고: Thickness은 특정 스플라인 노드에서 사용됩니다. |
| <b>점 좌표</b> |  |
| <b>p1</b> <i>Float2</i> | 텍스처 공간에서 p1 점의 위치를 설정합니다. |
| <b>p1 접선</b> <i>Float2</i> | 텍스처 공간에서 p1 지점 &#39;out&#39; 접선 핸들의 위치를 설정합니다. |
| <b>p2</b> <i>Float2</i> | 텍스처 공간에서 p2 점의 위치를 설정합니다. |
| <b>p2 접선</b> <i>Float2</i> | 텍스처 공간에서 p2 지점 &#39;in&#39; 접선 핸들의 위치를 설정합니다. |
| <b>미리 보기</b> |  |
| <b>접선 표시</b> <i>부울</i> | 미리 보기 출력에 p1 포인트 &#39;out&#39; 탄젠트와 p2 포인트 &#39;in&#39; 탄젠트를 표시합니다. |
| <b>방향 도우미 표시</b> <i>부울</i> | 미리 보기 출력에서 스플라인의 시작 부분에 점을 표시하고 끝 부분에 화살표를 표시합니다. |
| <b>세그먼트 양</b> <i>정수</i> | [미리 보기] 출력에서 스플라인 시각화를 그리는 데 사용되는 선분의 수를 조정합니다. 값이 높을수록 선이 더 매끄러워집니다. |
| <b>Thickness(px)</b> <i>부동</i> | 미리 보기 출력에서 스플라인 시각화의 픽셀 단위로 Thickness을 조정합니다. |

## 예

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![노드 예 1](spline-cubic.resources/spline-cubic-02.jpg "노드 예 1")

</td>
<td style="border: 0;" valign="top">

![노드 예 2](spline-cubic.resources/spline-cubic-03.jpg "노드 예 2")

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![노드 예 3](spline-cubic.resources/spline-cubic-04.gif "노드 예 3")

</td>
<td style="border: 0;" valign="top">



</td>
</tr>
</table>
