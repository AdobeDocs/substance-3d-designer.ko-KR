---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/spline-paths-tools/spline-tools/spline-circle.html"
breadcrumb-title: ''
description: 스플라인 원형 노드(Spline Circle node)를 사용하여 원형 패턴 및 모양을 생성하기 위한 원형 스플라인을 생성할 수 있습니다.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Spline  Path Tools > Spline Tools > Spline Circle
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 스플라인 원
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '672'
ht-degree: 0%

---


# 스플라인 원

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![노드 아이콘](spline-circle.resources/spline-circle-01.png "노드 아이콘")

<b>인:</b> 스플라인 및 패스 도구 > 자유 곡선 도구

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 설명

원 모양으로 단일 스플라인을 생성합니다.

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
| <b>원 반경</b> <i>부동</i> | 텍스처 공간에서 원의 반경을 조정합니다. |
| <b>원 사전 회전</b> <i>부동</i> | [크기]를 적용하기 전에 기본 원에 회전을 적용합니다. |
| <b>원 크기</b> <i>부동2</i> | 원의 가로 크기(X) 및 세로 크기(Y)를 조정합니다. |
| <b>순환 후 회전</b> <i>부동</i> | [크기]를 적용한 후 기본 원에 회전을 적용합니다. |
| <b>원 위치</b> <i>부동2</i> | 텍스처 공간에서 원의 중심 위치를 설정합니다. |
| <b>시작 Thickness</b> <i>부동</i> | 원의 시작점 Thickness을 조정합니다. 이 Thickness은 스플라인을 따라 끝 Thickness으로 보간됩니다.<br>참고: Thickness은 특정 스플라인 노드에서 사용됩니다. |
| <b>최종 Thickness</b> <i>부동</i> | 원의 끝점 Thickness을 조정합니다. 이 Thickness은 스플라인을 따라 시작 Thickness으로 보간됩니다.<br>참고: Thickness은 특정 스플라인 노드에서 사용됩니다. |
| <b>시작 Height</b> <i>부동</i> | 값이 낮을수록 위치가 낮거나 깊은 원의 시작점 Height을 조정합니다. 이 Height은 스플라인을 따라 끝 Height으로 보간됩니다. |
| <b>최종 Height</b> <i>부동</i> | 값이 낮을수록 위치가 낮거나 깊은 원의 끝점에 대한 Height을 조정합니다. 이 Height은 시작 Height에서 스플라인을 따라 보간됩니다. |
| <b>자르기</b> <i>Float2</i> | 원을 따라 스플라인의 시작점과 끝점을 오프셋합니다. 이러한 값은 정규화됩니다. |
| <b>나선형</b> <i>부동</i> | 원의 시작점을 반지름에서 중심까지 변위합니다. 중심으로부터의 거리는 스플라인을 따라 스플라인의 끝까지 보간됩니다. 이 값은 정규화됩니다. |
| <b>나선형 회전</b> <i>부동</i> | 중심부를 중심으로 나선형으로 돌아가는 회전 수를 정의합니다. |
| <b>나선형 전원</b> <i>부동</i> | 나선을 그리는 데 사용되는 중심으로부터의 거리에 힘 곡선을 적용합니다. 값이 1보다 크면 나선의 더 큰 부분이 중심에 가깝게 유지됨을 의미합니다. |
| <b>방향 뒤집기</b> <i>부울</i> | 스플라인의 방향을 반전합니다. |
| <b>균일 배포</b> <i>부울</i> | True이면 스플라인의 점이 시작부터 끝까지 일정한 간격을 유지합니다. |
| <b>입력 스플라인 추가</b> <i>부울</i> | 생성된 스플라인을 <b>스플라인</b> 입력에 연결된 스플라인 목록의 끝에 추가합니다. |
| <b>정사각형이 아닌 수정</b> <i>부울</i> | 점의 위치와 Thickness을 조정하여 정사각형이 아닌 해상도에서 스플라인 모양을 유지합니다. 이는 또한 균일한 분포에도 영향을 미친다. |
| <b>미리 보기</b> |  |
| <b>방향 도우미 표시</b> <i>부울</i> | 미리 보기 출력에서 스플라인의 시작 부분에 점을 표시하고 끝 부분에 화살표를 표시합니다. |
| <b>Thickness 봉투 표시</b> <i>부울</i> | 스플라인 Thickness 모서리에 추가 선을 표시합니다. |
| <b>세그먼트 양</b> <i>정수</i> | [미리 보기] 출력에서 스플라인 시각화를 그리는 데 사용되는 선분의 수를 조정합니다. 값이 높을수록 선이 더 매끄러워집니다. |
| <b>Thickness(px)</b> <i>부동</i> | 미리 보기 출력에서 스플라인 시각화의 픽셀 단위로 Thickness을 조정합니다. |

## 예

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![노드 예 1](spline-circle.resources/spline-circle-02.jpg "노드 예 1")

</td>
<td style="border: 0;" valign="top">

![노드 예 2](spline-circle.resources/spline-circle-03.gif "노드 예 2")

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![예 3](spline-circle.resources/spline-circle-04.jpg "예 3")

</td>
<td style="border: 0;" valign="top">

![예 4](spline-circle.resources/spline-circle-05.jpg "예 4")

</td>
</tr>
</table>
