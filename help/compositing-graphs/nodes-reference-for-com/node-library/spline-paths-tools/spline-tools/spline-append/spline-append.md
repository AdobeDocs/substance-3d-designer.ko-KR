---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/spline-paths-tools/spline-tools/spline-append.html"
breadcrumb-title: ''
description: 스플라인 첨부(Spline Append) 노드를 사용하여 여러 스플라인을 함께 추가하여 보다 긴 연속 패스를 만듭니다.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Spline  Path Tools > Spline Tools > Spline Append
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 스플라인 첨부
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '518'
ht-degree: 0%

---


# 스플라인 첨부

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![노드 아이콘](spline-append.resources/spline-append-01.png "노드 아이콘")

<b>인:</b> 스플라인 및 패스 도구 > 자유 곡선 도구

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 설명

스플라인은 목록으로 패키지됩니다. 이 노드는 기존 목록(세트 #2)에 입력 스플라인(세트 #1) 목록을 추가합니다.

목록 D-E-F를 목록 A-B-C에 추가하면 목록 A-B-C-D-E-F가 표시된다는 것을 의미하는 목록의 순서가 유지됩니다.

</td>
</tr>
</table>

>[!TIP]
>
> [스플라인의 산란](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/spline-tools/scatter-on-spline-color/scatter-on-spline-color.md), [스플라인 브리지](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/spline-tools/spline-bridge-list/spline-bridge-list.md) 노드 등과 같은 다른 노드에서는 이 순서를 고려하므로 스플라인을 추가하는 순서에 주의해야 합니다.

<a name="inputs"></a>

## 입력

|  |  |
|:---|:---|
| <b>미리 보기 #1</b> <i>회색 음영</i> | 첫 번째 입력 세트 미리보기가 회색 음영 이미지로 분할됩니다. |
| <b>스플라인 #1 코드</b> <i>색상</i> | 색상 이미지의 RGBA 채널로 인코딩된 첫 번째 입력 스플라인 지점 세트의 좌표입니다.<br><b>R</b> - X 위치<br><b>G</b> - Y 위치<br><b>B</b> - Height<br><b>A</b> - 압축된 데이터:<br>- 기호: 스플라인이 닫히거나(음수) 열림(양수);<br>- 절대값: Thickness + 1. |
| <b>스플라인 #1 데이터</b> <i>색상</i> | 색상 이미지의 RGBA 채널에 인코딩된 첫 번째 입력 스플라인 세트의 추가 데이터입니다.<br><b>R</b> - 탄젠트 X<br><b>G</b> - 탄젠트 Y<br><b>B</b> - 미사용<br><b>A</b> - 미사용 |
| <b>스플라인 #1 양</b> <i>정수</i> | 첫 번째 세트의 입력 스플라인 수입니다. |
| <b>미리 보기 #2</b> <i>회색 음영</i> | 두 번째 입력 세트 미리보기가 회색 음영 이미지로 분할됩니다. |
| <b>스플라인 #2 코드</b> <i>색상</i> | 색상 이미지의 RGBA 채널로 인코딩된 두 번째 입력 스플라인 지점 세트의 좌표입니다.<br><b>R</b> - X 위치<br><b>G</b> - Y 위치<br><b>B</b> - Height<br><b>A</b> - 압축된 데이터:<br>- 기호: 스플라인이 닫히거나(음수) 열림(양수);<br>- 절대값: Thickness + 1. |
| <b>스플라인 #2 데이터</b> <i>색상</i> | 색상 이미지의 RGBA 채널에 인코딩된 두 번째 입력 스플라인 세트의 추가 데이터입니다.<br><b>R</b> - 탄젠트 X<br><b>G</b> - 탄젠트 Y<br><b>B</b> - 미사용<br><b>A</b> - 미사용 |
| <b>스플라인 #2 양</b> <i>정수</i> | 두 번째 세트의 입력 스플라인 수입니다. |

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
| <b>스플라인 #1 방향 뒤집기</b> <i>부울</i> | 첫 번째 세트의 스플라인의 방향을 반전합니다. |
| <b>스플라인 #2 방향 뒤집기</b> <i>부울</i> | 두 번째 세트의 스플라인의 방향을 반전합니다. |
| <b>미리 보기</b> |  |
| <b>세그먼트 양</b> <i>정수</i> | [미리 보기] 출력에서 스플라인 시각화를 그리는 데 사용되는 선분의 수를 조정합니다. 값이 높을수록 선이 더 매끄러워집니다. |
| <b>방향 도우미 표시</b> <i>부울</i> | 미리 보기 출력에서 스플라인의 시작 부분에 점을 표시하고 끝 부분에 화살표를 표시합니다. |
| <b>Thickness 봉투 표시</b> <i>부울</i> | 스플라인 Thickness 모서리에 추가 선을 표시합니다. |
| <b>Thickness(px)</b> <i>부동</i> | 미리 보기 출력에서 스플라인 시각화의 Thickness을 픽셀 단위로 조정합니다. |

## 예

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![노드 예 1](spline-append.resources/spline-append-02.jpg "노드 예 1")

</td>
<td style="border: 0;" valign="top">

![노드 예 2](spline-append.resources/spline-append-03.jpg "노드 예 2")

</td>
</tr>
</table>

![노드 데모](spline-append.resources/spline-append-04.gif "노드 데모")
