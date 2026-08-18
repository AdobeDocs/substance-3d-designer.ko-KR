---
helpx_url: "https://helpx.adobe.com/kr/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/spline-paths-tools/spline-tools/uv-mapper-color.html"
breadcrumb-title: ''
description: UV 매퍼 색상 노드를 사용하여 절차 텍스처 생성을 위해 스플라인을 따라 색상 텍스처를 매핑할 수 있습니다.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Spline  Path Tools > Spline Tools > UV Mapper Color
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: UV 매퍼 색상
user-guide-description: ''
user-guide-title: ''
source-git-commit: 27326c60e0247617a8f57554a68c9663934cd2bc
workflow-type: tm+mt
source-wordcount: '174'
ht-degree: 1%

---


# UV 매퍼 색상

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![노드 아이콘](../../../../../../assets/uv-mapper-color-icon.png "노드 아이콘")

<b>인:</b> 스플라인 및 패스 도구 > 자유 곡선 도구

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 설명

UV 입력에 제공된 좌표를 사용하여 입력 색상 이미지를 매핑합니다.

</td>
</tr>
</table>

>[!NOTE]
>
> [UV 매퍼 회색 음영](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/spline-tools/uv-mapper-grayscale/uv-mapper-grayscale.md)도 참조하세요.

## 입력 커넥터

<b>UV</b> *색상*&#x200B;색상 이미지의 빨강(U) 및 녹색(V) 채널로 인코딩된 이미지 좌표

<b>입력</b> *색상* UV 입력에 제공된 좌표에 매핑할 색상 이미지입니다.

## 출력 커넥터

<b>출력</b> *색상*&#x200B;입력 UV 좌표를 사용하여 입력 이미지를 색상 이미지로 매핑한 결과입니다.

## 매개변수

<b>배경색</b> *Float4*&#x200B;출력 이미지의 배경색입니다.\
배경은 UV가 정의되지 않은 이미지 영역(예: 값이 (0, 0, 0, 0))에 표시됩니다.

## 예

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="../../../../../../assets/UVMapper-Variant1-Before.jpg" alt="UVMapper-Variant1-Before">
      <br><i>이전</i>
    </td>
    <td>
      <img src="../../../../../../assets/UVMapper-Variant1-After.jpg" alt="UVMapper-Variant1-After">
      <br><i>이후</i>
    </td>
  </tr>
</table>

</td>
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="../../../../../../assets/UVMapper-Variant2-Before.jpg" alt="UVMapper-Variant2-Before">
      <br><i>이전</i>
    </td>
    <td>
      <img src="../../../../../../assets/UVMapperColor-Variant2-After.jpg" alt="UVMapperColor-Variant2-After">
      <br><i>이후</i>
    </td>
  </tr>
</table>

</td>
</tr>
</table>

![그래프의 노드](../../../../../../assets/UVMapperColor-Graph.jpg "그래프의 노드")

</td>
<td style="border: 0;" valign="top">



</td>
<td style="border: 0;" valign="top">



</td>
</tr>
</table>
