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
source-git-commit: 27326c60e0247617a8f57554a68c9663934cd2bc
workflow-type: tm+mt
source-wordcount: '362'
ht-degree: 1%

---


# 스플라인 병합 목록

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![노드 아이콘](../../../../../../assets/spline-merge-list-icon.png "노드 아이콘")

<b>인:</b> 스플라인 및 패스 도구 > 자유 곡선 도구

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 설명

입력 목록의 모든 스플라인을 단일 스플라인으로 병합합니다.

</td>
</tr>
</table>

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

<b>미리 보기</b> *회색 음영*&#x200B;병합된 스플라인을 회색 음영 이미지로 미리 봅니다.

<b>스플라인 코드</b> *색상*&#x200B;색상 이미지의 RGBA 채널로 인코딩된 병합된 스플라인의 점 좌표입니다.\
    <b>R</b> - X 위치\
    <b>G</b> - Y 위치\
    <b>B</b> - Height\
    <b>A</b> - 압축된 데이터:\
        * Sign: 스플라인이 닫히거나(음수) 열림(양수);\
        * 절대값: Thickness + 1.

<b>스플라인 데이터</b> *색상*&#x200B;색상 이미지의 RGBA 채널에 인코딩된 병합된 스플라인의 추가 데이터입니다.\
    <b>R</b> - 접선 X\
    <b>G</b> - 접선 Y\
    <b>B</b> - 사용되지 않음\
    <b>A</b> - 사용되지 않음

<b>스플라인 양</b> *정수*&#x200B;병합된 스플라인의 수입니다.

## 매개변수

<b>닫힌 스플라인 거리 임계값</b> *부동*&#x200B;텍스처 공간에서 같은 스플라인의 두 가장자리가 해당 스플라인을 닫는 단일 점으로 처리되는 거리입니다.\
이렇게 하면 스플라인을 따라 모양을 분산하거나 이미지를 매핑할 때 겹치는 것을 방지할 수 있습니다.

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
      <img src="../../../../../../assets/SplineMergeList-Variant2-Before.jpg" alt="SplineMergeList-Variant2-Before">
      <br><i>이전</i>
    </td>
    <td>
      <img src="../../../../../../assets/SplineMergeList-Variant2-After.jpg" alt="SplineMergeList-Variant2-After">
      <br><i>이후</i>
    </td>
  </tr>
</table>

</td>
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="../../../../../../assets/SplineMergeList-Variant1-Before.jpg" alt="SplineMergeList-Variant1-Before">
      <br><i>이전</i>
    </td>
    <td>
      <img src="../../../../../../assets/SplineMergeList-Variant1-After.jpg" alt="SplineMergeList-Variant1-After">
      <br><i>이후</i>
    </td>
  </tr>
</table>

</td>
</tr>
</table>

![노드 데모](../../../../../../assets/SplineMergeList-Demo.gif "노드 데모")

</td>
<td style="border: 0;" valign="top">



</td>
<td style="border: 0;" valign="top">



</td>
</tr>
</table>
