---
helpx_url: "https://helpx.adobe.com/kr/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/spline-paths-tools/spline-tools/spline-sample-height.html"
breadcrumb-title: ''
description: 스플라인 샘플 Height 노드를 사용하면 절차 변위 효과를 위해 스플라인을 따라 Height 값을 샘플링할 수 있습니다.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Spline  Path Tools > Spline Tools > Spline Sample Height
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 스플라인 샘플 Height
user-guide-description: ''
user-guide-title: ''
source-git-commit: 5b9c9d12e2ccd76f75ec2a74815f9c68c43c06a2
workflow-type: tm+mt
source-wordcount: '603'
ht-degree: 0%

---


# 스플라인 샘플 Height

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![노드 아이콘](../../../../../../assets/spline-sample-height-icon.png "노드 아이콘")

<b>인:</b> 스플라인 및 패스 도구 > 자유 곡선 도구

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 설명

입력 스플라인에 입력 Height 맵을 매핑하여 입력 스플라인의 Height을 수정합니다.

혼합 모드와 해당 효과의 불투명도를 변경하여 매핑된 Height 맵의 효과를 조정할 수 있습니다.

</td>
</tr>
</table>

## 입력 커넥터

<b>미리 보기</b> *회색 음영*&#x200B;입력 미리 보기가 회색 음영 이미지로 분할됩니다.

<b>스플라인 코드</b> *색상*&#x200B;색상 이미지의 RGBA 채널로 인코딩된 입력 스플라인의 점 좌표:\
<b> R</b> - X 위치\
<b> G</b> - Y 위치\
<b> B</b> - Height\
<b>A</b> - 압축된 데이터:\
* Sign: 스플라인이 닫히거나(음수) 열림(양수);\
* 절대값: Thickness + 1.

<b>스플라인 데이터</b> *색상*&#x200B;색상 이미지의 RGBA 채널로 인코딩된 입력 스플라인의 추가 데이터입니다.\
<b> R</b> - 접선 X\
<b> G</b> - 접선 Y\
<b> B</b> - 미사용\
<b> A</b> - 미사용

<b>스플라인 양</b> *정수*&#x200B;입력 스플라인 수입니다.

<b>Height 맵</b> *회색 음영*&#x200B;입력 스플라인의 Height을 변경하는 데 사용되는 입력 회색 음영 이미지입니다.

## 출력 커넥터

<b>미리 보기</b> *회색 음영*&#x200B;출력물의 미리 보기가 회색 음영 이미지로 분할됩니다.

<b>스플라인 코드</b> *색상*&#x200B;색상 이미지의 RGBA 채널로 인코딩된 출력 스플라인의 점 좌표입니다.\
<b>R</b> - X 위치\
<b>G</b> - Y 위치\
<b>B</b> - Height\
<b>A</b> - 압축된 데이터:\
* Sign: 스플라인이 닫히거나(음수) 열림(양수);\
* 절대값: Thickness + 1.

<b>스플라인 데이터</b> *색상*&#x200B;색상 이미지의 RGBA 채널로 인코딩된 출력 스플라인의 추가 데이터입니다.\
<b>R</b> - 접선 X\
<b>G</b> - 접선 Y\
<b>B</b> - 사용되지 않음\
<b>A</b> - 사용되지 않음

<b>스플라인 양</b> *정수*&#x200B;출력 스플라인 수입니다.

## 매개변수

<b>샘플링 모드</b> *정수* Height 맵의 값을 스플라인에 매핑하는 방법:\
*- 텍스처 공간*: 해당 값은 텍스처의 UV 좌표를 사용하여 텍스처에 배치할 경우 스플라인에 적용됩니다. 그러면 값이 스플라인에 &#39;제자리에&#39; 효과적으로 적용됩니다.\
*- 스플라인을 따라 수평*: 이 값은 인코딩된 스플라인의 좌표에 직접 적용됩니다(스플라인 좌표 입력 참조). 여기서 각 행은 위에서 아래로 다른 스플라인에 적용됩니다.\
*-. 스플라인을 따라(랜드). 오프셋 X)*: 이 값은 인코딩된 스플라인의 좌표에 직접 적용됩니다(스플라인 좌표 입력 참조). 각 스플라인(즉, 스플라인 좌표의 각 행)에 대한 비율 맵의 임의 수평 오프셋은 다음과 같습니다.\
*-. 스플라인을 따라(랜드). 오프셋 Y)*: 이 값은 인코딩된 스플라인의 좌표에 직접 적용됩니다(스플라인 좌표 입력 참조). 각 스플라인(즉, 스플라인 좌표의 각 행)에 대한 비율 맵의 임의 수직 오프셋은 다음과 같습니다.

<b>불투명도</b> *부동*&#x200B;스플라인 Height에 대한 Height 맵 입력의 기여도 강도에 대한 승수입니다.<b></b>

<b>혼합 모드</b> *정수* Height 맵의 데이터를 입력 스플라인의 Height과 혼합하는 방법:\
*- 복사*: 스플라인의 Height을 Height 맵 값으로 재정의합니다.\
*- 추가*: 스플라인의 Height에 Height 맵 값을 추가합니다.\
*- 빼기*: Height 맵 값을 스플라인의 Height에 뺍니다.\
*- 곱하기*: 스플라인의 Height에 대해 Height 맵 값을 곱합니다.

+++미리보기
<b>세그먼트 양</b> *정수*&#x200B;미리 보기 출력에서 스플라인 시각화를 그리는 데 사용되는 세그먼트 수를 조정합니다.\
값이 높을수록 선이 더 매끄러워집니다.

<b>방향 도우미 표시</b> *부울*&#x200B;미리 보기 출력에서 스플라인의 시작 부분에 점을 표시하고 끝 부분에 화살표를 표시합니다.

<b>Thickness 봉투 표시</b> *부울*\
스플라인 Thickness 모서리에 추가 선을 표시합니다.

<b>Thickness(px)</b> *부동*&#x200B;미리 보기 출력에서 스플라인 시각화의 Thickness을 픽셀 단위로 조정합니다.

+++

## 예

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="../../../../../../assets/SplineSampleHeight-Variant1-Before.jpg" alt="SplineSampleHeight-Variant1-Before">
      <br><i>이전</i>
    </td>
    <td>
      <img src="../../../../../../assets/SplineSampleHeight-Variant1-After.jpg" alt="SplineSampleHeight-Variant1-After">
      <br><i>이후</i>
    </td>
  </tr>
</table>

</td>
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="../../../../../../assets/SplineSampleHeight-Variant1-Before.jpg" alt="SplineSampleHeight-Variant1-Before">
      <br><i>이전</i>
    </td>
    <td>
      <img src="../../../../../../assets/SplineSampleHeight-Variant1-After3.jpg" alt="SplineSampleHeight-Variant1-After3">
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

![노드 예 1](../../../../../../assets/SplineSampleHeight-Variant1-After4.jpg "노드 예 1")

</td>
<td style="border: 0;" valign="top">

![노드 예 2](../../../../../../assets/SplineSampleHeight-Demo.gif "노드 예 2")

</td>
</tr>
</table>

</td>
<td style="border: 0;" valign="top">



</td>
<td style="border: 0;" valign="top">



</td>
</tr>
</table>
