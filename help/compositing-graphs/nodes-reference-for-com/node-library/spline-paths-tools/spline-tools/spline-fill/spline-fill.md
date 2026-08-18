---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/spline-paths-tools/spline-tools/spline-fill.html"
breadcrumb-title: ''
description: 스플라인 채우기 노드를 사용하여 닫힌 스플라인으로 정의된 영역을 텍스처 또는 색상으로 채웁니다.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Spline  Path Tools > Spline Tools > Spline Fill
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 스플라인 채우기
user-guide-description: ''
user-guide-title: ''
source-git-commit: 27326c60e0247617a8f57554a68c9663934cd2bc
workflow-type: tm+mt
source-wordcount: '224'
ht-degree: 0%

---


# 스플라인 채우기

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![노드 아이콘](../../../../../../assets/spline-fill-icon.png "노드 아이콘")

<b>인:</b> 스플라인 및 패스 도구 > 자유 곡선 도구

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 설명

입력 스플라인의 내부를 단색 흰색으로 채웁니다. 외부는 단색 검정으로 채워져 있습니다.

열린 스플라인은 처음부터 끝까지 직선으로 닫힙니다. 스플라인이 그 자체로 교차하는 교차점은 해당 접합점에서 선의 내부와 외부를 반전하여 해결됩니다.

</td>
</tr>
</table>

>[!IMPORTANT]
>
> [0,1] 타일에서 벗어난 스플라인에는 이 노드를 사용하지 않는 것이 좋습니다. 그 경우 충진 과정은 신뢰할 수 없다.

## 입력 커넥터

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

## 출력 커넥터

<b>출력</b> *회색 음영*\
검정 배경의 분할 영역을 흰색으로 칠한 결과 이미지입니다.

## 예

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="../../../../../../assets/SplineFill-Variant1-Before.jpg" alt="SplineFill-Variant1-Before">
      <br><i>이전</i>
    </td>
    <td>
      <img src="../../../../../../assets/SplineFill-Variant1-After.jpg" alt="SplineFill-Variant1-After">
      <br><i>이후</i>
    </td>
  </tr>
</table>

</td>
<td style="border: 0;" valign="top">

![노드 예 2](../../../../../../assets/SplineFill-Demo.gif "노드 예 2")

</td>
</tr>
</table>
