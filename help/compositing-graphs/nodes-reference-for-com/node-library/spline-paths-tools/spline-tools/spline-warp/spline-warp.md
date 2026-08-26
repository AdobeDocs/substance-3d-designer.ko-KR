---
helpx_url: "https://helpx.adobe.com/kr/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/spline-paths-tools/spline-tools/spline-warp.html"
breadcrumb-title: ''
description: 스플라인 뒤틀기 노드를 사용하면 곡선 및 유기적인 패턴을 만들기 위해 스플라인 경로를 따라 텍스처를 뒤틀 수 있습니다.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Spline  Path Tools > Spline Tools > Spline Warp
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 스플라인 뒤틀기
user-guide-description: ''
user-guide-title: ''
source-git-commit: 5b9c9d12e2ccd76f75ec2a74815f9c68c43c06a2
workflow-type: tm+mt
source-wordcount: '1139'
ht-degree: 0%

---


# 스플라인 뒤틀기

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![노드 아이콘](../../../../../../assets/spline-warp-icon.png "노드 아이콘")

<b>인:</b> 스플라인 및 패스 도구 > 자유 곡선 도구

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 설명

입력 강도 맵 또는 벡터 맵을 기준으로 입력 스플라인을 변위합니다.

감쇠 컨트롤을 사용하여 스플라인을 따라 뒤틀기 효과의 강도를 조정할 수 있습니다.

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

<b>강도 맵</b> *회색 음영*(벡터 맵 사용이 &#39;거짓&#39;으로 설정된 경우 사용 가능)\
입력 스플라인의 뒤틀기 효과 방향과 강도를 제어하는 데 사용되는 입력 회색 음영 이미지입니다.\
이미지의 각 픽셀 색상은 스플라인의 점을 표준(스플라인에 수직한 방향)을 따라 최대 이미지 전체 스팬까지 변위하기 위한 승수를 지정합니다.\
승수로 읽을 때 이미지의 [0; 1] 값이 [-1; 1] 범위에 다시 매핑됩니다. 0과 1은 스플라인을 같은 거리지만 반대 방향으로 변위합니다. 0.5를 지정하면 스플라인이 제자리에 남아 있습니다.

<b>벡터 맵</b> *회색 음영*(&#39;벡터 맵 사용&#39;이 &#39;True&#39;로 설정된 경우 사용 가능)입력 스플라인에서 뒤틀기 효과의 방향과 강도를 제어하는 데 사용되는 입력 색상 이미지입니다.\
이미지의 각 픽셀 색상은 좌표가 빨강(X) 및 녹색(Y) 채널로 인코딩되는 벡터(X, Y)를 지정합니다. +X는 오른쪽이고 +Y는 아래쪽입니다.\
이미지의 [0; 1] 값이 벡터 좌표로 읽을 때 [-1; 1] 범위에 다시 매핑됩니다. 빨강 0은 점을 왼쪽, 녹색 0은 점을 위 방향으로 변위합니다. 0.5 빨간색과 녹색은 스플라인을 제자리에 둡니다.

<b>감쇠 곡선</b> *회색 음영*&#x200B;첫 번째 픽셀 행 값을 사용하여 곡선을 설명하는 이미지입니다.\
감쇠 곡선 사용(Use Attenuation Curve) 매개변수를 True로 설정하면 이 입력을 사용하여 스플라인의 시작과 끝 부근에서 뒤틀기 효과의 감쇠를 제어합니다.\
곡선은 감쇠를 위한 프로파일을 제공하며, 행의 첫 번째 픽셀은 스플라인의 시작 시 뒤틀기 효과의 강도이고 마지막 픽셀은 끝의 강도입니다. 회색 음영 값은 [강도]입니다.\
곡선 노드를 사용하여 곡선을 만들 수 있습니다.

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

<b>뒤틀기 강도</b> *부동*&#x200B;스플라인이 이동되는 강도입니다.

<b>뒤틀기 중심</b> *부동*&#x200B;스플라인을 제자리에 두면 해당하는 강도 맵 값을 지정합니다.\
값이 0 또는 1이면 스플라인이 한 면에서만 변위될 수 있음을 의미합니다.

<b>샘플링 모드</b> *정수*&#x200B;강도 맵 또는 벡터 맵의 값을 스플라인에 매핑하는 방법:\
*- 텍스처 공간*: 해당 값은 텍스처의 UV 좌표를 사용하여 텍스처에 배치할 경우 스플라인에 적용됩니다. 그러면 값이 스플라인에 &#39;제자리에&#39; 효과적으로 적용됩니다.\
*- 스플라인을 따라 수평*: 이 값은 인코딩된 스플라인의 좌표에 직접 적용됩니다(스플라인 좌표 입력 참조). 여기서 각 행은 위에서 아래로 다른 스플라인에 적용됩니다.\
*-. 스플라인을 따라(랜드). 오프셋 X)*: 이 값은 인코딩된 스플라인의 좌표에 직접 적용됩니다(스플라인 좌표 입력 참조). 각 스플라인(즉, 스플라인 좌표의 각 행)에 대한 비율 맵의 임의 수평 오프셋은 다음과 같습니다.\
*-. 스플라인을 따라(랜드). 오프셋 Y)*: 이 값은 인코딩된 스플라인의 좌표에 직접 적용됩니다(스플라인 좌표 입력 참조). 각 스플라인(즉, 스플라인 좌표의 각 행)에 대한 비율 맵의 임의 수직 오프셋은 다음과 같습니다.

<b>벡터 맵 사용</b> *부울*&#x200B;스플라인의 변위 방법을 변위 방향을 지정하는 [벡터 맵] 입력의 사용으로 전환합니다.\
이미지의 각 픽셀 색상은 좌표가 빨강(X) 및 녹색(Y) 채널로 인코딩되는 벡터(X, Y)를 지정합니다. +X는 오른쪽이고 +Y는 아래쪽입니다.\
이미지의 [0; 1] 값이 벡터 좌표로 읽을 때 [-1; 1] 범위에 다시 매핑됩니다. 빨강 0은 점을 왼쪽, 녹색 0은 점을 위 방향으로 변위합니다. 0.5 빨간색과 녹색은 스플라인을 제자리에 둡니다.

<b>감쇠 곡선 사용</b> *부울*&#x200B;감쇠 곡선 입력 이미지에 인코딩된 곡선을 사용하여 스플라인을 따라 뒤틀기 효과의 강도를 제어할 수 있습니다.<b></b>

<b>강도 맵 타일링</b> *부동*(&#39;샘플링 모드&#39;가 &#39;텍스처 공간&#39;으로 설정되지 않은 경우 사용 가능)스플라인 좌표에 직접 매핑될 때 강도 맵의 타일링을 조정합니다(스플라인 좌표 입력 참조).<b></b>

<b>감쇠 시작</b> *Float*(&#39;감쇠 곡선 사용&#39;이 &#39;거짓&#39;으로 설정된 경우 사용 가능)스플라인의 시작 부분에서 뒤틀기 효과의 감쇠를 위한 승수입니다.\
값이 1이면 스플라인의 시작 부분에 뒤틀기가 적용되지 않습니다.

<b>감쇠 종료</b> *Float*(&#39;감쇠 곡선 사용&#39;이 &#39;거짓&#39;으로 설정된 경우 사용 가능)스플라인 끝 근처의 뒤틀기 효과의 감쇠를 위한 승수입니다.\
값이 1이면 스플라인의 끝에 뒤틀기가 적용되지 않습니다.<b></b>

<b>접선 다시 계산</b> *부울* True이면 뒤틀기 효과가 적용된 후 스플라인의 접선이 다시 계산됩니다.\
이렇게 하면 스플라인의 접선이 스플라인 상의 산란(Plugin on Spline) 또는 스플라인 플로우 매퍼(Spline Flow Mapper)와 같은 노드에서 사용될 때 해당 궤적과 일관되게 유지됩니다.

+++미리보기
<b>세그먼트 양</b> *정수*&#x200B;미리 보기 출력에서 스플라인 시각화를 그리는 데 사용되는 세그먼트 수를 조정합니다.\
값이 높을수록 선이 더 매끄러워집니다.

<b>방향 도우미 표시</b> *부울*&#x200B;미리 보기 출력에서 스플라인의 시작 부분에 점을 표시하고 끝 부분에 화살표를 표시합니다.

<b>Thickness 봉투 표시</b> *부울*\
스플라인 Thickness 모서리에 추가 선을 표시합니다.

<b>Thickness(px)</b> *부동*&#x200B;미리 보기 출력에서 스플라인 시각화의 Thickness을 픽셀 단위로 조정합니다.

<b>배경 미리 보기 강도</b> *부동*\
배경 미리 보기 입력 이미지에 대해 곱해진 값입니다.

+++

## 예

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="../../../../../../assets/SplineWarp-Variant1-Before.jpg" alt="SplineWarp-Variant1-Before">
      <br><i>이전</i>
    </td>
    <td>
      <img src="../../../../../../assets/SplineWarp-Variant1-After.jpg" alt="SplineWarp-Variant1-After">
      <br><i>이후</i>
    </td>
  </tr>
</table>

</td>
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="../../../../../../assets/SplineWarp-Variant2-Before.jpg" alt="SplineWarp-Variant2-Before">
      <br><i>이전</i>
    </td>
    <td>
      <img src="../../../../../../assets/SplineWarp-Variant2-After.jpg" alt="SplineWarp-Variant2-After">
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

![노드 예 1](../../../../../../assets/SplineWarp-Demo.gif "노드 예 1")

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
