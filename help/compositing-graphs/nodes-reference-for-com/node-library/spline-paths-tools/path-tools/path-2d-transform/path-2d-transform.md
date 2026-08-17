---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/spline-paths-tools/path-tools/path-2d-transform.html"
breadcrumb-title: ''
description: '[패스 2D 변형] 노드를 사용하면 평행 이동, 회전 및 비율 조정 작업을 통해 패스를 변형할 수 있습니다.'
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Spline  Path Tools > Path Tools > Path 2D Transform
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 패스 2D 변형
user-guide-description: ''
user-guide-title: ''
source-git-commit: 27326c60e0247617a8f57554a68c9663934cd2bc
workflow-type: tm+mt
source-wordcount: '237'
ht-degree: 1%

---


# 패스 2D 변형

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![노드 아이콘](../../../../../../assets/path-2d-transform-icon.png "노드 아이콘")

<b>인:</b> 스플라인 및 패스 도구 > 패스 도구

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 설명

기즈모를 사용하여 패스를 변형합니다.

</td>
</tr>
</table>

## 입력 커넥터

<b>경로</b> *색상*\
인코딩된 세그먼트 경로 목록입니다. 이 입력을 [패스에 마스크](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/mask-to-paths/mask-to-paths.md) 또는 다른 패스 처리 노드에 연결합니다.

## 출력 커넥터

<b>경로</b> *색상*\
변형된 패스. [패스 미리 보기](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/preview-paths/preview-paths.md)를 사용하여 결과가 어떻게 나타나는지 파악하거나 다른 패스 처리 노드를 사용하거나 [스플라인으로 패스](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/paths-to-spline/paths-to-spline.md)에 입력하여 스플라인으로 추가로 처리할 수 있습니다.

## 매개변수

<b>매트릭스 변환</b> *부동 소수점4*\
스플라인에 적용된 변형 행렬 다음과 같이 세 가지 행렬 매개 변수 편집 모드를 사용할 수 있습니다.\
*- 변형 기즈모:* 스플라인 2D 변형 노드를 선택하면 [2D 보기](../../../../../../interface/2d-view/2d-view.md)에 표시된 기즈모의 핸들을 조정합니다.\
*- 회전/늘이기:* 스플라인의 회전 및 늘이기를 개별적으로 제어합니다. 값은 항상 현재 변환에 상대적으로 적용됩니다. 예를 들어, 50% 너비를 두 번 적용하면 25% 너비가 생성됩니다.\
*- 행렬 값:* <b>행렬 값 편집</b> 단추를 클릭하여 행렬의 원시 숫자 값을 직접 입력합니다.

<b>오프셋</b> *부동 소수점2*\
X(가로) 및 Y(세로)의 스플라인에 위치 오프셋을 적용합니다.

## 예

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="../../../../../../assets/PathsPolygon_Variant1.jpg" alt="PathsPolygon_Variant1">
      <br><i>이전</i>
    </td>
    <td>
      <img src="../../../../../../assets/Paths2DTransform-Variant1.jpg" alt="Paths2DTransform-Variant1">
      <br><i>이후</i>
    </td>
  </tr>
</table>

</td>
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="../../../../../../assets/PathsPolygon_Variant1.jpg" alt="PathsPolygon_Variant1">
      <br><i>이전</i>
    </td>
    <td>
      <img src="../../../../../../assets/Paths2DTransform-Variant2.jpg" alt="Paths2DTransform-Variant2">
      <br><i>이후</i>
    </td>
  </tr>
</table>

</td>
</tr>
</table>
