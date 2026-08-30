---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/spline-paths-tools/spline-tools/spline-sample-thickness.html"
breadcrumb-title: ''
description: 스플라인 샘플 Thickness 노드를 사용하여 절차 효과를 위해 스플라인을 따라 Thickness 값을 샘플링합니다.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Spline  Path Tools > Spline Tools > Spline Sample Thickness
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 스플라인 샘플 Thickness
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '598'
ht-degree: 0%

---


# 스플라인 샘플 Thickness

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![노드 아이콘](spline-sample-thickness.resources/spline-sample-thickness-icon.png "노드 아이콘")

<b>인:</b> 스플라인 및 패스 도구 > 자유 곡선 도구

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 설명

입력 스플라인에 입력 Thickness 맵을 매핑하여 입력 스플라인의 Thickness을 수정합니다.

혼합 모드와 해당 효과의 불투명도를 변경하여 매핑된 Height 맵의 효과를 조정할 수 있습니다.

</td>
</tr>
</table>

<a name="inputs"></a>

## 입력

|  |  |
|:---|:---|
| <b>미리 보기</b> <i>회색 음영</i> | 입력 미리보기가 회색 음영 이미지로 분할됩니다. |
| <b>스플라인 코드</b> <i>색상</i> | 색상 이미지의 RGBA 채널로 인코딩된 입력 스플라인의 좌표:<br><b>R</b> - X 위치<br><b>G</b> - Y 위치<br><b>B</b> - Height<br><b>A</b> - 압축된 데이터:<br> - 기호: 스플라인이 닫힘(네거티브) 또는 열림(포지티브);<br> - 절대값: Thickness + 1. |
| <b>스플라인 데이터</b> <i>색상</i> | 색상 이미지의 RGBA 채널에 인코딩된 입력 스플라인의 추가 데이터입니다.<br><b>R</b> - 탄젠트 X<br><b>G</b> - 탄젠트 Y<br><b>B</b> - 미사용<br><b>A</b> - 미사용 |
| <b>스플라인 양</b> <i>정수</i> | 입력 스플라인의 수입니다. |
| <b>Thickness 맵</b> <i>회색 음영</i> | 입력 스플라인의 Thickness을 변경하는 데 사용되는 입력 회색 음영 이미지입니다. |

<a name="outputs"></a>

## 출력

|  |  |
|:---|:---|
| <b>미리 보기</b> <i>회색 음영</i> | 출력 미리 보기가 회색 음영 이미지로 분할됩니다. |
| <b>스플라인 코드</b> <i>색상</i> | 색상 이미지의 RGBA 채널로 인코딩된 출력 스플라인의 좌표입니다.<br><b>R</b> - X 위치<br><b>G</b> - Y 위치<br><b>B</b> - Height<br><b>A</b> - 압축된 데이터:<br> - 기호: 스플라인이 닫힘(음수) 또는 열림(양수);<br> - 절대값: Thickness + 1. |
| <b>스플라인 데이터</b> <i>색상</i> | 색상 이미지의 RGBA 채널로 인코딩된 출력 스플라인의 추가 데이터입니다.<br><b>R</b> - 탄젠트 X<br><b>G</b> - 탄젠트 Y<br><b>B</b> - 미사용<br><b>A</b> - 미사용 |
| <b>스플라인 양</b> <i>정수</i> | 출력 스플라인의 수입니다. |

<a name="parameters"></a>

## 매개변수

|  |  |
|:---|:---|
| <b>샘플링 모드</b> <i>정수</i> | 두께 맵의 값을 스플라인에 매핑하는 방법:<br>- <i>텍스처 공간</i>: 값은 텍스처의 UV 좌표를 사용하여 텍스처에 배치할 경우 스플라인에 적용됩니다. 이는 스플라인의 &#39;제자리&#39;,<br>- <i>스플라인을 따라 수평</i>에 값을 효과적으로 적용합니다. 값은 인코딩된 스플라인의 좌표에 직접 적용됩니다(스플라인 좌표 입력 참조). 여기서 각 행은 위에서 아래로 다른 스플라인에 적용됩니다.<br>- <i>Hor. 스플라인을 따라(랜드). 오프셋 X)</i>: 값은 인코딩된 스플라인의 좌표에 직접 적용됩니다(스플라인 좌표 입력 참조). 각 스플라인(즉, 스플라인 좌표의 각 행)에 대한 배율 맵의 임의 수평 오프셋은 다음과 같습니다.<br>- <i>Hor. 스플라인을 따라(랜드). 오프셋 Y)</i>: 이 값은 인코딩된 스플라인의 좌표에 직접 적용됩니다(스플라인 좌표 입력 참조). 각 스플라인(즉, 스플라인 좌표의 각 행)에 대한 비율 맵의 임의 수직 오프셋은 다음과 같습니다. |
| <b>불투명도</b> <i>부동</i> | 스플라인 Thickness에 대한 두께 맵 입력의 기여도 강도를 나타내는 승수입니다. |
| <b>혼합 모드</b> <i>정수</i> | 두께 맵의 데이터를 입력 스플라인의 <span id="_Hlk135820484"></span>Thickness과 혼합하는 방법:<br>- <i>복사</i>: 높이 맵 값으로 스플라인의 Thickness 재정의;<br>- <i>추가</i>: 스플라인의 Thickness에 두께 맵 값 추가;<br>- <i>스플라인의 Thickness에 두께 맵 값 빼기;<br>- <i>곱하기</i>: 두께 맵 값을 스플라인의 Thickness에 곱합니다.</i> |
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
      <img src="spline-sample-thickness.resources/SplineSampleThickness-Variant1-Before.jpg" alt="SplineSampleThickness-Variant1-Before">
      <br><i>이전</i>
    </td>
    <td>
      <img src="spline-sample-thickness.resources/SplineSampleThickness-Variant1-After.jpg" alt="SplineSampleThickness-Variant1-After">
      <br><i>이후</i>
    </td>
  </tr>
</table>

</td>
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="spline-sample-thickness.resources/SplineSampleThickness-Variant2-Before.jpg" alt="SplineSampleThickness-Variant2-Before">
      <br><i>이전</i>
    </td>
    <td>
      <img src="spline-sample-thickness.resources/SplineSampleThickness-Variant2-After.jpg" alt="SplineSampleThickness-Variant2-After">
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

![노드 예 1](spline-sample-thickness.resources/SplineSampleThickness-Variant1-After1.jpg "노드 예 1")

</td>
<td style="border: 0;" valign="top">

![노드 예 2](spline-sample-thickness.resources/SplineSampleThickness-Demo.gif "노드 예 2")

</td>
</tr>
</table>
