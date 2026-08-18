---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/spline-paths-tools/spline-tools/spline-poly-quadratic.html"
breadcrumb-title: ''
description: 스플라인 폴리 2차 노드를 사용하여 여러 제어점이 있는 복잡한 2차 스플라인을 생성합니다.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Spline  Path Tools > Spline Tools > Spline (Poly Quadratic)
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 스플라인(폴리 이차)
user-guide-description: ''
user-guide-title: ''
source-git-commit: 27326c60e0247617a8f57554a68c9663934cd2bc
workflow-type: tm+mt
source-wordcount: '1147'
ht-degree: 0%

---


# 스플라인(폴리 이차)

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![노드 아이콘](../../../../../../assets/spline-poly-quadratic-icon.png "노드 아이콘")

<b>인:</b> 스플라인 및 패스 도구 > 자유 곡선 도구

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 설명

여러 점을 따라 스플라인을 생성합니다. 이러한 지점의 양과 위치는 임의이거나 [지점 목록](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/spline-tools/point-list/point-list.md) 노드에서 모일 수 있습니다.

</td>
</tr>
</table>

스플라인의 궤적은 각 중간점이 이웃의 &#39;아웃&#39; 및 &#39;인&#39; 접선의 만남점이라는 점에서 중간점에서 부드럽게 만들 수 있습니다.

## 입력 커넥터

<b>미리 보기</b> *회색 음영*&#x200B;입력 미리 보기가 회색 음영 이미지로 분할됩니다.

<b>스플라인 코드</b> *색상*&#x200B;색상 이미지의 RGBA 채널로 인코딩된 입력 스플라인의 점 좌표:\
<b> R</b> - X 위치\
<b> G</b> - Y 위치\
<b> B</b> - Height\
<b> A</b> - 압축된 데이터:\
        * Sign: 스플라인이 닫히거나(음수) 열림(양수);\
        * 절대값: Thickness + 1.

<b>스플라인 데이터</b> *색상*&#x200B;색상 이미지의 RGBA 채널로 인코딩된 입력 스플라인의 추가 데이터입니다.\
<b> R</b> - 접선 X\
<b> G</b> - 접선 Y\
<b> B</b> - 미사용\
<b> A</b> - 미사용

<b>스플라인 양</b> *정수*&#x200B;입력 스플라인 수입니다.

<b>포인트 미리 보기&#x200B;</b>*회색 음영*&#x200B;포인트를 회색 음영 이미지로 미리 봅니다.

<b>입력 지점 목록</b> *색상*(&#39;입력 지점 목록 사용&#39;이 True인 경우 사용 가능)\
색상 이미지의 RGBA 채널로 인코딩된 지점 목록:\
    <b>R</b> - X 위치\
    <b>G</b> - Y 위치\
    <b>B</b> - Height\
    <b>A</b> - 압축된 데이터:\
        * 정수 부분: Smoothness;\
        * 분수 부분: Thickness.

<b>지점 번호</b> *정수*(&#39;입력 지점 목록 사용&#39;이 True인 경우 사용 가능)\
포인트 수입니다.

>[!IMPORTANT]
>
> <b>포인트 목록</b> 및 <b>포인트 번호</b> 커넥터는 다른 데이터를 사용하기 때문에 <b>스플라인 코드</b>, <b>스플라인 데이터</b> 및 <b>스플라인 양</b> 커넥터와 *호환되지 않음*&#x200B;입니다.

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

<b>포인트 양</b> *정수*&#x200B;스플라인을 만드는 데 사용되는 임의의 포인트 수입니다.

<b>스플라인 연결 모드 입력</b> *정수*&#x200B;입력 스플라인을 연결하는 데 사용되는 방법:\
*- 자동:* 마지막 입력 스플라인의 끝이 생성된 스플라인의 시작과 연결되고 생성된 스플라인의 끝이 첫 번째 입력 스플라인의 시작과 연결됩니다.\
*- 수동:* 생성된 스플라인의 가장자리에 연결해야 하는 입력 스플라인과 입력 스플라인의 위치에 연결해야 하는 연결을 지정할 수 있습니다.

<b>스플라인 닫기</b> *부울*&#x200B;스플라인의 끝점을 시작점에 연결할지 여부를 제어합니다.\
시작점 및 끝점의 스플라인에 적용된 매끄러움은 해당 점의 Smoothness 값으로 지정됩니다.

<b>방향 뒤집기</b> *부울*\
스플라인의 방향을 반전합니다.

<b>입력 지점 목록 사용</b> *부울*&#x200B;임의 포인트 목록 대신 입력 포인트 목록 및 포인트 번호 입력 커넥터에 제공된 포인트 목록을 사용합니다.\
포인트 목록은 [포인트 목록](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/spline-tools/point-list/point-list.md) 노드에서 제공할 수 있습니다.

<b>시작 부분을 입력 스플라인에 연결</b> *부울* True인 경우 생성된 스플라인의 시작 부분이 입력 스플라인의 마지막 스플라인의 마지막 점에 연결됩니다.

<b>연결 스플라인 인덱스 시작</b> *정수*(&#39;입력 스플라인 연결 모드&#39;가 &#39;수동&#39;으로 설정되고 &#39;입력 스플라인에 연결 시작&#39;이 &#39;True&#39;로 설정된 경우 사용 가능)생성된 스플라인의 시작과 연결되어야 하는 입력 스플라인의 인덱스입니다.

<b>연결 위치 시작</b> *Float*(&#39;입력 스플라인 연결 모드&#39;가 &#39;수동&#39;으로 설정되고 &#39;입력 스플라인에 연결 시작&#39;이 &#39;True&#39;로 설정된 경우 사용 가능)생성된 스플라인의 시작에 대한 연결이 연결되는 선택한 입력 스플라인의 위치입니다.\
이 값은 선택한 입력 스플라인의 정규화된 길이입니다.

<b>입력 스플라인에 끝 연결</b> *부울* True이면 생성된 스플라인의 끝이 입력 스플라인의 첫 번째 스플라인의 첫 번째 점에 연결됩니다.

<b>연결 스플라인 인덱스 종료</b> *정수*(&#39;입력 스플라인 연결 모드&#39;가 &#39;수동&#39;으로 설정되고 &#39;입력 스플라인에 끝 연결&#39;이 &#39;참&#39;으로 설정된 경우 사용 가능)생성된 스플라인의 끝에 연결해야 하는 입력 스플라인의 인덱스입니다.

<b>연결 위치 종료</b> *부동*(&#39;입력 스플라인 연결 모드&#39;가 &#39;수동&#39;으로 설정되고 &#39;입력 스플라인에 끝 연결&#39;이 &#39;참&#39;으로 설정된 경우 사용 가능)생성된 스플라인의 끝에 대한 연결이 놓여야 하는 선택한 입력 스플라인의 위치입니다.\
이 값은 선택한 입력 스플라인의 정규화된 길이입니다.

<b>균일 배포</b> *부울*\
True이면 스플라인의 점이 시작부터 끝까지 일정한 간격을 유지합니다.

<b>입력 스플라인 추가</b> *부울*\
생성된 스플라인을 <b>스플라인</b> 입력에 연결된 스플라인 목록의 끝에 추가합니다.

<b>정사각형이 아닌 교정&#x200B;</b>*부울*&#x200B;점의 위치와 Thickness을 조정하여 정사각형이 아닌 해상도에서 스플라인 모양을 유지합니다.\
이는 또한 균일한 분포에도 영향을 미친다.

<b>전역 Smoothness 조정</b> *부동*&#x200B;모든 점의 Smoothness 값에 균일 오프셋을 적용합니다.\
결과 Smoothness 값은 [0;1] 범위로 클램프됩니다.

+++포인트 속성
<b>p# 속성</b> *Float3* p# 지점의 속성을 설정합니다.\
*- Height:* 값이 낮을수록 위치가 낮거나 깊은 지점의 Height을 조정합니다.\
*- Smoothness:* p#에서 스플라인의 매끄럽게 하기 시작을 오프셋합니다. 여기서 0의 값을 사용하면 단단한 궤적이 만들어지고 1은 완전히 매끄러운 궤적이 만들어집니다.\
*- Thickness:* p#에서 스플라인의 Thickness을 조정합니다. Thickness은 특정 스플라인 노드에서 사용됩니다.

+++

+++포인트 좌표
<b>p#</b> *Float2*&#x200B;텍스처 공간에서 p# 지점의 위치를 설정합니다.

+++

+++미리보기
<b>접선 표시</b> *부울*&#x200B;미리 보기 출력에서 p1 및 p3 지점의 접선을 p2에 표시합니다.

<b>방향 도우미 표시</b> *부울*&#x200B;미리 보기 출력에서 스플라인의 시작 부분에 점을 표시하고 끝 부분에 화살표를 표시합니다.

<b>Thickness 봉투 표시</b> *부울*\
스플라인 Thickness 모서리에 추가 선을 표시합니다.

<b>포인트 레이블 표시</b> *부울*\
각 점에 대해 &#39;미리 보기&#39; 출력에서 해당 점 옆에 점의 이름을 표시합니다.

<b>포인트 레이블 크기</b> *부동*(&#39;Show Points Label&#39;이 &#39;True&#39;로 설정된 경우 사용 가능)\
텍스처 공간의 각 점에 대한 레이블의 크기입니다. 여기서 0.1은 텍스처 폭의 10분의 1입니다.

<b>포인트 표시</b> *부울*\
스플라인의 조절점을 표시합니다.

<b>포인트 크기</b> *부동*(&#39;Show Points&#39;가 &#39;True&#39;로 설정된 경우 사용 가능)\
텍스처 공간에서 점의 반경입니다. 여기서 0.1은 텍스처 폭의 10분의 1입니다.

<b>세그먼트 양</b> *정수*&#x200B;미리 보기 출력에서 스플라인 시각화를 그리는 데 사용되는 세그먼트 수를 조정합니다.\
값이 높을수록 선이 더 매끄러워집니다.

<b>Thickness(px)</b> *부동*&#x200B;미리 보기 출력에서 스플라인 시각화의 Thickness을 픽셀 단위로 조정합니다.

+++

## 예

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="../../../../../../assets/SplinePolyQuadratic-Variant1-Before.jpg" alt="SplinePolyQuadratic-Variant1-Before">
      <br><i>이전</i>
    </td>
    <td>
      <img src="../../../../../../assets/SplinePolyQuadratic-Variant1-After.jpg" alt="SplinePolyQuadratic-Variant1-After">
      <br><i>이후</i>
    </td>
  </tr>
</table>

</td>
<td style="border: 0;" valign="top">

![노드 예 2](../../../../../../assets/SplinePolyQuadratic-Demo.gif "노드 예 2")

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
