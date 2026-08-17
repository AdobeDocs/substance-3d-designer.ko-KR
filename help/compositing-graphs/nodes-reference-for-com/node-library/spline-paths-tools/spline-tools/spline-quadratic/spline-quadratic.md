---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/spline-paths-tools/spline-tools/spline-quadratic.html"
breadcrumb-title: ''
description: 스플라인 2차 노드를 사용하여 3개의 제어점으로 매끄러운 2차 스플라인을 만듭니다.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Spline  Path Tools > Spline Tools > Spline (Quadratic)
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 스플라인(2차)
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '843'
ht-degree: 0%

---


# 스플라인(2차)

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![스플라인(2차): 아이콘](../../../../../../assets/spline-quadratic-icon.png "스플라인(2차): 아이콘")

<b>인:</b> 스플라인 및 패스 도구 > 자유 곡선 도구

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 설명

임의의 위치에서 두 점 <b>p1</b>과(와) <b>p3</b> 사이의 단일 스플라인을 생성합니다.

스플라인의 궤적은 <b>p1</b>의 &#39;out&#39; 접선과 <b>p3</b>의 &#39;in&#39; 접선으로 제어되며, *둘 다*&#x200B;는 단일 지점 <b>p3</b>으로 제어됩니다.

스플라인에 의해 형성된 호의 범위는 *조정 가능*&#x200B;이므로, 그것의 끝으로부터 궤적의 일부는 직선으로 유지될 수 있다.

</td>
</tr>
</table>

## 입력 커넥터

|  |  |
| --- | --- |
| <b>미리 보기</b> *회색 음영* | 입력 미리보기가 회색 음영 이미지로 분할됩니다. |
| <b>스플라인 코드</b> *색상* | 색상 이미지의 RGBA 채널로 인코딩된 입력 스플라인의 좌표: <b>R</b> - X 위치 <b>G</b> - Y 위치 <b>B</b> - Height <b>A</b> - 압축된 데이터: - 기호: 스플라인이 닫힘(네거티브) 또는 열림(포지티브); - 절대값: Thickness + 1. |
| <b>스플라인 데이터</b> *색상* | 색상 이미지의 RGBA 채널로 인코딩된 입력 스플라인의 추가 데이터: <b>R</b> - 탄젠트 X <b>G</b> - 탄젠트 Y <b>B</b> - 탄젠트 Z <b>A</b> - 미사용 |
| <b>스플라인 양</b> *정수* | 입력 스플라인의 수입니다. |

## 출력 커넥터

|  |  |
| --- | --- |
| <b>미리 보기</b> *회색 음영* | 출력 미리 보기가 회색 음영 이미지로 분할됩니다. |
| <b>스플라인 코드</b> *색상* | 색상 이미지의 RGBA 채널로 인코딩된 출력 스플라인의 좌표: <b>R</b> - X 위치 <b>G</b> - Y 위치 <b>B</b> - Height <b>A</b> - 압축된 데이터: - 기호: 스플라인이 닫힘(네거티브) 또는 열림(포지티브); - 절대값: Thickness + 1. |
| <b>스플라인 데이터</b> *색상* | 색상 이미지의 RGBA 채널로 인코딩된 출력 스플라인의 추가 데이터: <b>R</b> - 탄젠트 X <b>G</b> - 탄젠트 Y <b>B</b> - 탄젠트 Z <b>A</b> - 미사용 |
| <b>스플라인 양</b> *정수* | 출력 스플라인의 수입니다. |

## 매개변수

|  |  |
| --- | --- |
| <b>방향 뒤집기</b> *부울* | 스플라인의 방향을 반전합니다. |
| <b>균일 분포</b> *부울* | *True*&#x200B;인 경우 스플라인의 점이 시작부터 끝까지 고르게 분포됩니다. |
| <b>입력 스플라인 추가</b> *부울* | 생성된 스플라인을 <b>스플라인</b> 입력에 연결된 스플라인 목록의 끝에 추가합니다. |
| <b>정사각형이 아닌 수정</b> *부울* | 점의 위치와 Thickness을 조정하여 정사각형이 아닌 해상도에서 스플라인 모양을 유지합니다. 이는 또한 균일한 분포에도 영향을 미친다. |
| <b>Smoothness</b> *부동* | 스플라인으로 형성된 *호의 범위*&#x200B;를 조정합니다. 여기서 1은 스플라인의 전체 길이를 아치형으로 만들고 0은 스플라인이 완전히 직선이 되도록 합니다. 호는 지점 <b>p3</b>에서 스플라인을 따라 끝까지 진행됩니다. |

+++높이

|  |  |
| --- | --- |
| <b>시작 Height</b> *부동* | 값이 낮을수록 위치가 더 낮거나 더 깊은 <b>p1</b> 지점의 Height을 조정합니다.  이는 <b>p1</b>에서의 스플라인 Height에 영향을 줍니다. |
| <b>최종 Height</b> *부동* | 값이 낮을수록 위치가 더 낮거나 더 깊은 <b>p3</b> 지점의 Height을 조정합니다.  이는 <b>p3</b>에서의 스플라인 Thickness에 영향을 줍니다. |
| <b>자동 접선 Height</b> *부울* | 값이 낮을수록 위치가 더 낮거나 더 깊은 <b>p3</b> 지점의 Height을 조정합니다.  이는 <b>p3</b>에서의 스플라인 Thickness에 영향을 줍니다. |
| <b>접선 Height</b> *부동* | <b>p2</b> 지점으로 제어되는 접선에 의해 제어되는 Height을 조정합니다.  이는 <b>p1</b>에서 멀어져 <b>p3</b>으로 이동할 때 스플라인을 따라 Height에 영향을 줍니다.   *참고:* 이 매개 변수는 <b>자동 접선 Height</b>이 &#39;False&#39;로 설정된 경우에만 사용할 수 있습니다. |


+++

+++두께

|  |  |
| --- | --- |
| <b>시작 Thickness</b> *부동* | <b>p1</b> 지점의 Thickness을 조정합니다. 이는 <b>p1</b>에서의 스플라인 Thickness에 영향을 줍니다.   *참고:* Thickness은 특정 스플라인 노드에서 사용됩니다. |
| <b>최종 Thickness</b> *부동* | <b>p3</b> 지점의 Thickness을 조정합니다. 이는 <b>p3</b>에서의 스플라인 Thickness에 영향을 줍니다.   *참고:* Thickness은 특정 스플라인 노드에서 사용됩니다. |
| <b>자동 접선 Thickness</b> *부울* | <b>시작 Thickness</b>에서 <b>끝 Thickness</b>(으)로 선형으로 보간되도록 스플라인 접선의 Thickness을 자동으로 설정합니다.   *참고:* Thickness은 특정 스플라인 노드에서 사용됩니다. |
| <b>접선 Thickness</b> *부동* | <b>p2</b> 지점으로 제어되는 접선에 의해 제어되는 Thickness을 조정합니다.  이는 <b>p1</b>에서 멀어져 <b>p3</b>으로 이동할 때 스플라인을 따라 Thickness에 영향을 줍니다.   *참고:* Thickness은 특정 스플라인 노드에서 사용됩니다.  *참고 2:* 이 매개 변수는 <b>자동 접선 Thickness</b>이 &#39;False&#39;로 설정된 경우에만 사용할 수 있습니다. |


+++

+++포인트 좌표

|  |  |
| --- | --- |
| <b>p1</b> *Float2* | 텍스처 공간에서 <b>p1</b> 지점의 위치를 설정합니다. |
| <b>p2</b> *Float2* | 텍스처 공간에서 <b>p2</b> 지점의 위치를 설정합니다.  <b>p2</b> 지점은 <b>p1</b> 및 <b>p3</b> 지점 중 *접선*&#x200B;을 제어합니다. |
| <b>p3</b> *Float2* | 텍스처 공간에서 <b>p3</b> 지점의 위치를 설정합니다. |


+++

+++미리보기

|  |  |
| --- | --- |
| <b>접선 표시</b> *부울* | <b>미리 보기</b> 출력에서 <b>p1</b> 지점 &#39;out&#39; 접선과 <b>p3</b> 지점 &#39;in&#39; 접선을 표시합니다.스플라인의 방향을 반전합니다. |
| <b>방향 도우미 표시</b> *부울* | <b>미리 보기</b> 출력에서 스플라인의 시작 부분에 점을 표시하고 끝 부분에 화살표를 표시합니다. |
| <b>Thickness 봉투 표시</b> *부울* | 스플라인 Thickness 모서리에 추가 선을 표시합니다. |
| <b>세그먼트 양</b> *정수* | <b>미리 보기</b> 출력에서 스플라인 시각화를 그리는 데 사용되는 세그먼트 수를 조정합니다.  값이 높을수록 선이 더 매끄러워집니다. |
| <b>Thickness(px)</b> *부동* | <b>미리 보기</b> 출력에서 스플라인 시각화의 픽셀 단위로 Thickness을 조정합니다. |


+++

## 예

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![스플라인(2차): 예제 1](../../../../../../assets/spline-quadratic-example-1.png "스플라인(2차): 예제 1"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![스플라인(2차): 예제 2](../../../../../../assets/spline-quadratic-example-2.png "스플라인(2차): 예제 2"){zoomable="yes"}

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![스플라인(2차): 데모](../../../../../../assets/spline-quadratic-demo.gif "스플라인(2차): 데모"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">



</td>
</tr>
</table>
