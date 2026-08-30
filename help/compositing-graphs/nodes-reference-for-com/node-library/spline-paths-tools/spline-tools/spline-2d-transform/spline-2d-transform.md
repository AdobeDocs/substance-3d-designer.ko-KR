---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/spline-paths-tools/spline-tools/spline-2d-transform.html"
breadcrumb-title: ''
description: 스플라인 2D 변환 노드를 사용하여 평행 이동, 회전 및 배율 조정 작업을 통해 스플라인을 변형할 수 있습니다.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Spline  Path Tools > Spline Tools > Spline 2D Transform
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 스플라인 2D 변형
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '442'
ht-degree: 1%

---


# 스플라인 2D 변형

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![노드 아이콘](spline-2d-transform.resources/spline-2d-transform-icon.png "노드 아이콘")

<b>인:</b> 스플라인 및 패스 도구 > 자유 곡선 도구

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 설명

모든 입력 스플라인의 방향 반전을 포함하여 전체 변환을 적용합니다.

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
| <b>매트릭스 변환</b> <i>Float4</i> | 스플라인에 적용된 변형 행렬<br>2D 보기 매개 변수를 편집하는 세 가지 모드를 사용할 수 있습니다.<br><br>- <i>변형 기즈모</i>: 스플라인 2Spline d 노드를 선택할 때 기즈모 변환에 표시되는 핸들의 조정}- 4 노드 선택 시 <br>;스플라인의 회전 <i>회전 제어/개별 회전 제어</i>: 스플라인의 회전 및 개별 회전 제어. 값은 항상 현재 변환에 상대적으로 적용됩니다. 예를 들어, 50% 너비를 두 번 적용하면 25% 너비가 됩니다.<br>- <i>행렬 값</i>: [행렬 값 편집] 버튼을 클릭하여 행렬의 원시 숫자 값을 직접 입력합니다. |
| <b>오프셋</b> <i>Float2</i> | X(가로) 및 Y(세로)의 스플라인에 위치 오프셋을 적용합니다. |
| <b>미리 보기</b> |  |
| <b>방향 도우미 표시</b> <i>부울</i> | 미리 보기 출력에서 스플라인의 시작 부분에 점을 표시하고 끝 부분에 화살표를 표시합니다. |
| <b>Thickness 봉투 표시</b> <i>부울</i> | 스플라인 Thickness 모서리에 추가 선을 표시합니다. |
| <b>세그먼트 양</b> <i>정수</i> | [미리 보기] 출력에서 스플라인 시각화를 그리는 데 사용되는 선분의 수를 조정합니다. 값이 높을수록 선이 더 매끄러워집니다. |
| <b>Thickness(px)</b> <i>부동</i> | 미리 보기 출력에서 스플라인 시각화의 Thickness을 픽셀 단위로 조정합니다. |

## 예

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="spline-2d-transform.resources/Spline2DTransform-Variant1-Before.jpg" alt="Spline2DTransform-Variant1-Before">
      <br><i>이전</i>
    </td>
    <td>
      <img src="spline-2d-transform.resources/Spline2DTransform-Variant2-After.jpg" alt="Spline2DTransform-Variant2-After">
      <br><i>이후</i>
    </td>
  </tr>
</table>

</td>
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="spline-2d-transform.resources/Spline2DTransform-Variant1-Before.jpg" alt="Spline2DTransform-Variant1-Before">
      <br><i>이전</i>
    </td>
    <td>
      <img src="spline-2d-transform.resources/Spline2DTransform-Variant1-After.jpg" alt="Spline2DTransform-Variant1-After">
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

![노드 예 1](spline-2d-transform.resources/Spline2DTransform-Demo1.gif "노드 예 1")

</td>
<td style="border: 0;" valign="top">



</td>
</tr>
</table>
