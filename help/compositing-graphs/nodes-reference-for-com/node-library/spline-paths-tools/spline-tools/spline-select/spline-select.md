---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/spline-paths-tools/spline-tools/spline-select.html"
breadcrumb-title: ''
description: 스플라인 선택(Spline Select) 노드를 사용하여 그래프의 스플라인 경로를 기반으로 특정 영역을 선택하고 마스킹합니다.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Spline  Path Tools > Spline Tools > Spline Select
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 스플라인 선택
user-guide-description: ''
user-guide-title: ''
source-git-commit: 27326c60e0247617a8f57554a68c9663934cd2bc
workflow-type: tm+mt
source-wordcount: '514'
ht-degree: 0%

---


# 스플라인 선택

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![노드 아이콘](../../../../../../assets/spline-select-icon.png "노드 아이콘")

<b>인:</b> 스플라인 및 패스 도구 > 자유 곡선 도구

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 설명

지정된 기준에 따라 입력 목록에서 스플라인을 선택하고 선택한 스플라인만 포함하는 새 목록을 출력합니다.

선택한 스플라인을 트리밍할 수도 있습니다.

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

<b>선택 모드</b> *정수*&#x200B;입력 목록에서 스플라인을 선택하는 방법:\
*- 첫 번째*: 목록의 첫 번째 스플라인을 선택합니다.\
*- 마지막*: 목록에서 마지막 스플라인을 선택합니다.\
*- 인덱스*: 지정된 인덱스가 있는 스플라인을 선택합니다.\
*- 범위*: 지정한 범위에 포함된 인덱스를 선택합니다.

<b>스플라인 인덱스</b> *정수*(&#39;선택 모드&#39;가 &#39;색인&#39;으로 설정된 경우 사용 가능)선택해야 하는 스플라인의 인덱스입니다.

<b>범위 시작</b> *정수*(&#39;선택 모드&#39;가 &#39;범위&#39;로 설정된 경우 사용 가능)선택한 스플라인 범위의 가장 낮은 인덱스입니다.

<b>범위 끝</b> *정수*(&#39;선택 모드&#39;가 &#39;범위&#39;로 설정된 경우 사용 가능)선택한 스플라인 범위에서 가장 높은 인덱스입니다.<b></b>

<b>시작</b> *부동*&#x200B;선택할 스플라인 부분의 시작을 오프셋합니다. 이렇게 하면 스플라인이 효과적으로 트림됩니다.\
값은 스플라인의 정규화된 길이를 나타냅니다.

<b>종료</b> *부동*&#x200B;선택할 스플라인 부분의 끝을 오프셋합니다. 이렇게 하면 스플라인이 효과적으로 트림됩니다.\
값은 스플라인의 정규화된 길이를 나타냅니다.

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
      <img src="../../../../../../assets/SplineSelect-Variant1-Before.jpg" alt="SplineSelect-Variant1-Before">
      <br><i>이전</i>
    </td>
    <td>
      <img src="../../../../../../assets/SplineSelect-Variant1-After2.jpg" alt="SplineSelect-Variant1-After2">
      <br><i>이후</i>
    </td>
  </tr>
</table>

</td>
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="../../../../../../assets/SplineSelect-Variant2-Before.jpg" alt="SplineSelect-Variant2-Before">
      <br><i>이전</i>
    </td>
    <td>
      <img src="../../../../../../assets/SplineSelect-Variant2-After.jpg" alt="SplineSelect-Variant2-After">
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

![노드 예 1](../../../../../../assets/SplineSelect-Demo.gif "노드 예 1")

</td>
<td style="border: 0;" valign="top">



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
