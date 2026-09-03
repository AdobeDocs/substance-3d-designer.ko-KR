---
helpx_url: "https://helpx.adobe.com/kr/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/spline-paths-tools/spline-tools/uv-mapper-grayscale.html"
breadcrumb-title: ''
description: UV 매퍼 회색 음영 노드를 사용하여 프로시저 텍스처 생성을 위해 스플라인을 따라 회색 음영 텍스처를 매핑할 수 있습니다.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Spline  Path Tools > Spline Tools > UV Mapper Grayscale
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: UV 매퍼 회색 음영
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '142'
ht-degree: 2%

---


# UV 매퍼 회색 음영

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![노드 아이콘](uv-mapper-grayscale.resources/uv-mapper-grayscale-01.png "노드 아이콘")

<b>인:</b> 스플라인 및 패스 도구 > 자유 곡선 도구

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 설명

UV 입력에 제공된 좌표를 사용하여 입력 회색 음영 이미지를 매핑합니다.

</td>
</tr>
</table>

>[!NOTE]
>
> [UV 매퍼 색상](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/spline-tools/uv-mapper-color/uv-mapper-color.md)도 참조하세요.

<a name="inputs"></a>

## 입력

|  |  |
|:---|:---|
| <b>UV</b> <i>색상</i> | 색상 이미지의 빨강(U) 및 녹색(V) 채널로 인코딩된 이미지 좌표입니다. |
| <b>입력</b> <i>색상</i> | UV 입력에 제공된 좌표에 매핑해야 하는 회색 음영 이미지입니다. |

<a name="outputs"></a>

## 출력

|  |  |
|:---|:---|
| <b>출력</b> <i>색상</i> | 입력 UV 좌표를 사용하여 입력 이미지를 회색 음영 이미지로 매핑한 결과입니다. |

## 예

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="uv-mapper-grayscale.resources/uv-mapper-grayscale-02.jpg" alt="UVMapper-Variant1-Before">
      <br><i>이전</i>
    </td>
    <td>
      <img src="uv-mapper-grayscale.resources/uv-mapper-grayscale-03.jpg" alt="UVMapperGrayscale-Variant1-After">
      <br><i>이후</i>
    </td>
  </tr>
</table>

</td>
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="uv-mapper-grayscale.resources/uv-mapper-grayscale-04.jpg" alt="UVMapper-Variant2-Before">
      <br><i>이전</i>
    </td>
    <td>
      <img src="uv-mapper-grayscale.resources/uv-mapper-grayscale-05.jpg" alt="UVMapper-Variant2-After">
      <br><i>이후</i>
    </td>
  </tr>
</table>

</td>
</tr>
</table>

![노드 예 1](uv-mapper-grayscale.resources/uv-mapper-grayscale-06.jpg "노드 예 1")
