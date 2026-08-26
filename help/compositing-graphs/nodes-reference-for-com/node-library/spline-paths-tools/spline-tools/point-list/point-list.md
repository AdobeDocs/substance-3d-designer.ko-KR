---
helpx_url: "https://helpx.adobe.com/kr/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/spline-paths-tools/spline-tools/point-list.html"
breadcrumb-title: ''
description: 점 목록 노드 를 사용하여 스플라인 및 패스 생성에 사용할 점 목록을 만들고 관리합니다.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Spline  Path Tools > Spline Tools > Point List
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 포인트 목록
user-guide-description: ''
user-guide-title: ''
source-git-commit: 5b9c9d12e2ccd76f75ec2a74815f9c68c43c06a2
workflow-type: tm+mt
source-wordcount: '430'
ht-degree: 0%

---


# 포인트 목록

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![노드 아이콘](../../../../../../assets/point-list-icon.png "노드 아이콘")

<b>인:</b> 스플라인 및 패스 도구 > 자유 곡선 도구

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 설명

스플라인으로 이동할 점 목록을 생성합니다.

기존 포인트 목록을 <b>포인트</b> 입력에 제공하면 생성된 목록이 입력 목록에 추가됩니다.

</td>
</tr>
</table>

>[!TIP]
>
> 이 노드를 사용하면 스플라인을 만들기 위해 [스플라인(Poly Quadratic)](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/spline-tools/spline-poly-quadratic/spline-poly-quadratic.md) 노드에 점을 제공할 수 있습니다.

>[!IMPORTANT]
>
> <b>포인트 목록</b> 및 <b>포인트 번호</b> 커넥터는 다른 데이터를 사용하기 때문에 <b>스플라인 코드</b>, <b>스플라인 데이터</b> 및 <b>스플라인 양</b> 커넥터와 *호환되지 않음*&#x200B;입니다.

## 입력 커넥터

<b>미리 보기&#x200B;</b>*회색 음영*&#x200B;점을 회색 음영 이미지로 미리 봅니다.

<b>지점 목록 입력</b> *색상*\
색상 이미지의 RGBA 채널로 인코딩된 입력 지점 목록:\
<b>R</b> - X 위치\
<b>G</b> - Y 위치\
<b>B</b> - Height\
<b>A</b> - 압축된 데이터:\
* 정수 부분: Smoothness;\
* 분수 부분: Thickness.

<b>지점 번호 입력</b> *정수*\
입력 포인트 수입니다.

## 출력 커넥터

<b>미리 보기&#x200B;</b>*회색 음영*&#x200B;점을 회색 음영 이미지로 미리 봅니다.

<b>포인트 목록 </b>*색상*\
색상 이미지의 RGBA 채널로 인코딩된 점의 출력 목록은 다음과 같습니다.\
<b>R</b> - X 위치\
<b>G</b> - Y 위치\
<b>B</b> - Height\
<b>A</b> - 압축된 데이터:\
* 정수 부분: Smoothness;\
* 분수 부분: Thickness.

<b>포인트 번호 </b>*정수*\
출력 포인트 수입니다.

## 매개변수

<b>지점 번호</b> *정수*&#x200B;생성된 포인트 수입니다.

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
<b>레이블 표시</b> *부울*\
각 점에 대해 &#39;미리 보기&#39; 출력에서 해당 점 옆에 점의 이름을 표시합니다.

<b>레이블 크기</b> *부동*(&#39;레이블 표시&#39;가 &#39;True&#39;로 설정된 경우 사용 가능)\
텍스처 공간의 각 점에 대한 레이블의 크기입니다. 여기서 0.1은 텍스처 폭의 10분의 1입니다.

<b>포인트 표시</b> *부울*\
&#39;미리 보기&#39; 출력에 포인트를 표시합니다.

<b>포인트 크기</b> *부동*(&#39;Show Points&#39;가 &#39;True&#39;로 설정된 경우 사용 가능)\
텍스처 공간에서 점의 반경입니다. 여기서 0.1은 텍스처 폭의 10분의 1입니다.

+++

## 예

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![노드 예 1](../../../../../../assets/PointList-Variant1.jpg "노드 예 1")

</td>
<td style="border: 0;" valign="top">

![노드 예 2](../../../../../../assets/PointList-Demo1.gif "노드 예 2")

</td>
</tr>
</table>
