---
helpx_url: "https://helpx.adobe.com/kr/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/spline-paths-tools/spline-tools/spline-circle.html"
breadcrumb-title: ''
description: 스플라인 원형 노드(Spline Circle node)를 사용하여 원형 패턴 및 모양을 생성하기 위한 원형 스플라인을 생성할 수 있습니다.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Spline  Path Tools > Spline Tools > Spline Circle
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 스플라인 원
user-guide-description: ''
user-guide-title: ''
source-git-commit: 5b9c9d12e2ccd76f75ec2a74815f9c68c43c06a2
workflow-type: tm+mt
source-wordcount: '671'
ht-degree: 0%

---


# 스플라인 원

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![노드 아이콘](../../../../../../assets/spline-circle-icon.png "노드 아이콘")

<b>인:</b> 스플라인 및 패스 도구 > 자유 곡선 도구

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 설명

원 모양으로 단일 스플라인을 생성합니다.

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

<b>원 반경</b> *부동*\
텍스처 공간에서 원의 반경을 조정합니다.

<b>원 사전 회전</b> *부동*\
[크기]를 적용하기 전에 기본 원에 회전을 적용합니다.

<b>원 크기</b> *Float2*\
원의 가로 크기(X) 및 세로 크기(Y)를 조정합니다.

<b>순환 후 회전</b> *부동*\
[크기]를 적용한 후 기본 원에 회전을 적용합니다.

<b>원 위치</b> *Float2*\
텍스처 공간에서 원의 중심 위치를 설정합니다.

<b>시작 Thickness</b> *부동*&#x200B;원의 시작점 Thickness을 조정합니다.\
이 Thickness은 스플라인을 따라 끝 Thickness으로 보간됩니다.\
참고: Thickness은 특정 스플라인 노드에서 사용됩니다.

<b>최종 Thickness</b> *부동*&#x200B;원의 끝점 Thickness을 조정합니다.\
이 Thickness은 스플라인을 따라 시작 Thickness으로 보간됩니다.\
참고: Thickness은 특정 스플라인 노드에서 사용됩니다.

<b>시작 Height</b> *부동*&#x200B;값이 낮을수록 위치가 낮거나 깊은 원의 시작점 Height을 조정합니다.\
이 Height은 스플라인을 따라 끝 Height으로 보간됩니다.

<b>최종 Height</b> *부동*&#x200B;값이 낮을수록 위치가 낮거나 깊은 원의 끝점 Height을 조정합니다.\
이 Height은 시작 Height에서 스플라인을 따라 보간됩니다.

<b>자르기</b> *Float2*&#x200B;원을 따라 스플라인의 시작점과 끝점을 오프셋합니다.\
이러한 값은 정규화됩니다.

<b>나선형</b> *부동*&#x200B;원의 시작점을 반지름에서 중심으로 바꿉니다.\
중심으로부터의 거리는 스플라인을 따라 스플라인의 끝까지 보간됩니다.\
이 값은 정규화됩니다.

<b>나선형 회전</b> *부동*&#x200B;중앙 주위의 나선이 만드는 회전 수를 정의합니다.

<b>나선형 전원</b> *부동*&#x200B;나선을 그리는 데 사용되는 중심으로부터의 거리에 힘 곡선을 적용합니다.\
값이 1보다 크면 나선의 더 큰 부분이 중심에 가깝게 유지됨을 의미합니다.

<b>방향 뒤집기</b> *부울*\
스플라인의 방향을 반전합니다.

<b>균일 배포</b> *부울*\
True이면 스플라인의 점이 시작부터 끝까지 일정한 간격을 유지합니다.

<b>입력 스플라인 추가</b> *부울*\
생성된 스플라인을 <b>스플라인</b> 입력에 연결된 스플라인 목록의 끝에 추가합니다.

<b>정사각형이 아닌 교정&#x200B;</b>*부울*&#x200B;점의 위치와 Thickness을 조정하여 정사각형이 아닌 해상도에서 스플라인 모양을 유지합니다.\
이는 또한 균일한 분포에도 영향을 미친다.

+++미리보기
<b>방향 도우미 표시</b> *부울*&#x200B;미리 보기 출력에서 스플라인의 시작 부분에 점을 표시하고 끝 부분에 화살표를 표시합니다.

<b>Thickness 봉투 표시</b> *부울*\
스플라인 Thickness 모서리에 추가 선을 표시합니다.

<b>세그먼트 양</b> *정수*&#x200B;미리 보기 출력에서 스플라인 시각화를 그리는 데 사용되는 세그먼트 수를 조정합니다.\
값이 높을수록 선이 더 매끄러워집니다.

<b>Thickness(px)</b> *부동*&#x200B;미리 보기 출력에서 스플라인 시각화의 픽셀 단위로 Thickness을 조정합니다.

+++

## 예

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![노드 예 1](../../../../../../assets/SplineCircle-Variant1.jpg "노드 예 1")

</td>
<td style="border: 0;" valign="top">

![노드 예 2](../../../../../../assets/SplineCircle-Demo.gif "노드 예 2")

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![예 3](../../../../../../assets/SplineCircle-Variant2.jpg "예 3")

</td>
<td style="border: 0;" valign="top">

![예 4](../../../../../../assets/SplineCircle-Variant3.jpg "예 4")

</td>
</tr>
</table>
