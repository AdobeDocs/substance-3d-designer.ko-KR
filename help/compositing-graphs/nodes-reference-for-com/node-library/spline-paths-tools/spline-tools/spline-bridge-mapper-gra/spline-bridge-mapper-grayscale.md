---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/spline-paths-tools/spline-tools/spline-bridge-mapper-grayscale.html"
breadcrumb-title: ''
description: 스플라인 브리지 매퍼 회색 음영 노드를 사용하여 회색 음영 매핑을 사용하여 두 스플라인 사이의 텍스처를 연결합니다.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Spline  Path Tools > Spline Tools > Spline Bridge Mapper Grayscale
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 스플라인 브리지 매퍼 회색 음영
user-guide-description: ''
user-guide-title: ''
source-git-commit: 27326c60e0247617a8f57554a68c9663934cd2bc
workflow-type: tm+mt
source-wordcount: '367'
ht-degree: 0%

---


# 스플라인 브리지 매퍼 회색 음영

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![노드 아이콘](../../../../../../assets/spline-bridge-mapper-grayscale-icon.png "노드 아이콘")

<b>인:</b> 스플라인 및 패스 도구 > 자유 곡선 도구

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 설명

이미지가 스플라인을 순서대로 가로지르도록 입력 스플라인 목록에 회색 음영 이미지를 매핑합니다.

</td>
</tr>
</table>

>[!TIP]
>
> 매핑은 목록의 첫 번째 스플라인에서 마지막 스플라인으로 이동하고 목록에 있는 이러한 스플라인의 순서를 엄격하게 따라 중간 스플라인을 가로지릅니다.
> 
> 따라서 사전에 스플라인을 함께 붙이는 순서에 주의해야 합니다.

>[!NOTE]
>
> [스플라인 브리지 매퍼 색상](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/spline-tools/spline-bridge-mapper-col/spline-bridge-mapper-color.md)도 참조하세요.

## 입력 커넥터

<b>스플라인 코드</b> *색상*&#x200B;색상 이미지의 RGBA 채널로 인코딩된 입력 스플라인의 점 좌표:

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

<b>색상 맵&#x200B;</b>*회색 음영*&#x200B;입력 스플라인에 매핑해야 하는 입력 회색 음영 이미지입니다.

## 출력 커넥터

<b>색상</b> *회색 음영*&#x200B;입력 색상 이미지를 스플라인에 회색 음영 이미지로 매핑한 결과.

<b>Height</b> *회색 음영*&#x200B;회색 음영 이미지로 스플라인에 매핑된 스플라인의 Height.

<b>UV</b> *색상*&#x200B;컬러 이미지의 빨강(U) 및 녹색(V) 채널로 인코딩된 매핑된 이미지의 UV(즉, 좌표)입니다.

<b>마스크</b> *회색 음영*&#x200B;스플라인에 걸친 매핑의 마스크입니다.

## 매개변수

<b>세그먼트 양</b> *정수*&#x200B;스플라인은 이미지 좌표가 스플라인을 통과하기 전에 세그먼트로 단순화됩니다.\
선분의 양이 많을수록 커브를 따라 매핑이 더 매끄러워집니다.

<b>UV 스트레치 줄이기</b> *부울*&#x200B;스플라인 사이의 거리가 일정하지 않을 때 늘어나는 것을 최소화하기 위해 하나의 스플라인에서 다음 스플라인으로 이미지 좌표를 보간하는 데 사용되는 방법을 조정합니다.

<b>UV 비율</b> *Float2*&#x200B;이미지 좌표의 비율을 조정합니다. 값이 높을수록 타일이 촘촘하게 배치된 이미지가 더 많아집니다.

<b>UV 회전</b> *부동*&#x200B;가운데를 중심으로 이미지 좌표를 회전합니다.

## 예

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="../../../../../../assets/SplineBridgeMapperGrayscale-Variant1-Before.jpg" alt="SplineBridgeMapperGrayscale-Variant1-Before">
      <br><i>이전</i>
    </td>
    <td>
      <img src="../../../../../../assets/SplineBridgeMapperGrayscale-Variant1-After.jpg" alt="SplineBridgeMapperGrayscale-Variant1-After">
      <br><i>이후</i>
    </td>
  </tr>
</table>

</td>
<td style="border: 0;" valign="top">

![노드 예 2](../../../../../../assets/SplineBridgeMapper-Demo.gif "노드 예 2")

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![노드 예 1](../../../../../../assets/SplineBridgeMapperGrayscale-Variant1-After1.jpg "노드 예 1")

</td>
<td style="border: 0;" valign="top">

![노드 예 2](../../../../../../assets/SplineBridgeMapperGrayscale-Graph.jpg "노드 예 2")

</td>
</tr>
</table>
