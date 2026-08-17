---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/spline-paths-tools/spline-tools/spline-render.html"
breadcrumb-title: ''
description: 스플라인 렌더링 노드를 사용하여 사용자 정의 가능한 폭, 색상 및 혼합 모드를 사용하여 스플라인을 텍스처로 렌더링합니다.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Spline  Path Tools > Spline Tools > Spline Render
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 스플라인 렌더링
user-guide-description: ''
user-guide-title: ''
source-git-commit: 27326c60e0247617a8f57554a68c9663934cd2bc
workflow-type: tm+mt
source-wordcount: '798'
ht-degree: 0%

---


# 스플라인 렌더링

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![노드 아이콘](../../../../../../assets/spline-render-icon.png "노드 아이콘")

<b>인:</b> 스플라인 및 패스 도구 > 자유 곡선 도구

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 설명

입력 <b>배경</b> 위에 입력 <b>스플라인</b>을 따라 세그먼트 문자열을 그립니다.

</td>
</tr>
</table>

## 입력 커넥터

<b>배경&#x200B;</b>*회색 음영*&#x200B;스플라인을 그릴 회색 음영 이미지입니다.

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
배경 위에 입력 스플라인을 그리는 결과 이미지입니다.

## 매개변수

<b>모드</b> *정수*&#x200B;그릴 스플라인을 선택하는 방법:
* *스플라인 목록 그리기*: 입력 목록에 모든 스플라인을 그립니다.
* *단일 스플라인 그리기*: 입력 목록에서 지정된 스플라인만 그립니다.
* *스플라인 범위 그리기*: 입력 목록에서 지정된 범위의 스플라인만 그립니다.

<b>스플라인 색인 그리기</b> *정수*(&#39;모드&#39;가 &#39;단일 스플라인 그리기&#39;로 설정된 경우 사용 가능)그릴 스플라인의 인덱스입니다.

<b>스플라인 범위 그리기</b> *정수2*(&#39;모드&#39;가 &#39;스플라인 범위 그리기&#39;로 설정된 경우 사용 가능)그릴 스플라인의 인덱스 범위입니다.

<b>방향 도우미 표시</b> *부울*&#x200B;각 스플라인에 대해 스플라인의 시작 부분에 점을 그리고 그 끝에 화살표를 그립니다.

<b>세그먼트 양</b> *정수*&#x200B;스플라인을 따라 그려지는 세그먼트의 수를 조정합니다.\
값이 높을수록 선이 더 매끄러워집니다.

<b>엔벌로프 스플라인 양</b> *정수*\
각 스플라인의 Thickness을 따라 그려져야 하는 중복 세그먼트의 수입니다.

<b>시작</b> *부동*&#x200B;그릴 스플라인 부분의 시작을 오프셋합니다.\
값은 스플라인의 정규화된 길이를 나타냅니다.

<b>종료</b> *부동*&#x200B;스플라인 부분의 끝을 오프셋합니다.\
값은 스플라인의 정규화된 길이를 나타냅니다.

<b>Thickness 크기 모드</b> *정수*&#x200B;그려진 세그먼트의 Thickness 계산 방법:
* *이미지*: 텍스처 공간에서 값이 정규화됩니다. 여기서 1은 이미지의 전체 폭입니다. Thickness은 텍스처 해상도를 기준으로 합니다.
* *픽셀*: 이 값은 텍스처의 절대 픽셀 수이며 1은 전체 픽셀입니다. Thickness은 텍스처 해상도와 별개입니다.

<b>Thickness(이미지)</b> *부동*(&#39;Thickness 크기 모드&#39;가 [이미지]로 설정되어 있을 때 사용 가능)텍스처 공간에서 정규화된 그려진 세그먼트의 Thickness. 여기서 1은 이미지의 전체 폭입니다.

<b>Thickness(px)</b> *부동*(&#39;Thickness 크기 모드&#39;가 픽셀로 설정된 경우 사용 가능)그려진 선분의 Thickness을 텍스처의 절대 픽셀 수로 지정합니다. 여기서 1은 전체 픽셀입니다.

<b>조인트 사용</b> *부울*&#x200B;디스크를 사용하여 스플라인을 따라 그려진 개별 세그먼트 사이의 간격을 채웁니다.

<b>정사각형이 아닌 교정&#x200B;</b>*부울*&#x200B;점의 위치와 Thickness을 조정하여 정사각형이 아닌 해상도에서 스플라인 모양을 유지합니다.\
이는 또한 균일한 분포에도 영향을 미친다.

+++색상
<b>배경 강도</b> *부동*&#x200B;배경 입력 이미지에 곱해진 값입니다.

<b>스플라인 스타일</b> *정수*&#x200B;스플라인에 색상을 지정하는 데 사용되는 방법:
* *단색*: 선분은 균일한 회색 음영 값을 사용하여 그려집니다.
* *그레이디언트*: 검정에서 흰색으로의 그레이디언트가 처음부터 끝까지 각 세그먼트 문자열을 따라 적용됩니다.
* *Height*: 스플라인의 Height이 세그먼트를 그리는 회색 음영 값으로 사용됩니다.

<b>스플라인 색상</b> *부동*&#x200B;선분을 그리는 데 사용되는 균일한 회색 음영 값입니다.\
&#39;단색&#39; 이외의 스플라인 스타일을 선택하면 이 색상이 스타일링된 색상에 곱해집니다.

<b>임의 광도</b> *부동*&#x200B;스플라인에서 잘리지 않은 세그먼트의 각 문자열에 대해 지정된 범위의 임의 오프셋을 해당 문자열을 그리는 데 사용되는 회색 음영 값에 적용합니다.

<b>혼합 모드</b> *정수*&#x200B;배경의 색상과 스플라인을 따라 그려진 겹치는 선분을 혼합하는 방법:
* *최대*: 가장 밝은 값이 사용됩니다.
* *추가*: 값이 함께 추가됩니다.

+++

+++무작위 세그먼트
<b>무작위 세그먼트 시작</b> *부동*&#x200B;스플라인의 시작 부분에 가까운 선분 문자열이 잘릴 확률을 조정합니다.

<b>임의 세그먼트 끝</b> *부동*&#x200B;스플라인 끝에 가까운 선분 문자열이 잘릴 확률을 조정합니다.

<b>임의 오프셋</b> *부동*&#x200B;각 컷 선분에 적용되는 최대 변위 양을 표준을 따라 설정합니다.\
[시작]과 [종료]가 모두 0으로 설정되어 있으면 이 매개 변수는 영향을 주지 않습니다.

<b>임의 오프셋 가운데</b> *부동*&#x200B;각 오려내기 선분에 적용된 무작위 변위의 가운데를 법선을 따라 오프셋합니다.

+++

## 예

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="../../../../../../assets/SplineRender-Variant2-Before.jpg" alt="SplineRender-Variant2-Before">
      <br><i>이전</i>
    </td>
    <td>
      <img src="../../../../../../assets/SplineRender-Variant2-After.jpg" alt="SplineRender-Variant2-After">
      <br><i>이후</i>
    </td>
  </tr>
</table>

</td>
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="../../../../../../assets/SplineRender-Variant1-Before.jpg" alt="SplineRender-Variant1-Before">
      <br><i>이전</i>
    </td>
    <td>
      <img src="../../../../../../assets/SplineRender-Variant1-After.jpg" alt="SplineRender-Variant1-After">
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

<table>
  <tr>
    <td>
      <img src="../../../../../../assets/SplineRender-Variant1-Before.jpg" alt="SplineRender-Variant1-Before">
      <br><i>이전</i>
    </td>
    <td>
      <img src="../../../../../../assets/SplineRender-Variant3.jpg" alt="SplineRender-Variant3">
      <br><i>이후</i>
    </td>
  </tr>
</table>

</td>
<td style="border: 0;" valign="top">

![노드 예 1](../../../../../../assets/SplineRender-Demo.gif "노드 예 1")

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
