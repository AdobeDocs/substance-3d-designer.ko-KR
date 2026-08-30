---
helpx_url: "https://helpx.adobe.com/kr/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/spline-paths-tools/spline-tools/uv-mapper-color.html"
breadcrumb-title: ''
description: UV 매퍼 색상 노드를 사용하여 프로시저 텍스처 생성을 위해 스플라인을 따라 색상 텍스처를 매핑할 수 있습니다.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Spline  Path Tools > Spline Tools > UV Mapper Color
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: UV 매퍼 색상
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '176'
ht-degree: 2%

---


# UV 매퍼 색상

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![노드 아이콘](uv-mapper-color.resources/uv-mapper-color-icon.png "노드 아이콘")

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

<a name="inputs"></a>

## 입력

|  |  |
|:---|:---|
| <b>UV</b> <i>색상</i> | 색상 이미지의 빨강(U) 및 녹색(V) 채널로 인코딩된 이미지 좌표입니다. |
| <b>입력</b> <i>색상</i> | UV 입력에 제공된 좌표에 매핑해야 하는 색상 이미지입니다. |

<a name="outputs"></a>

## 출력

|  |  |
|:---|:---|
| <b>출력</b> <i>색상</i> | 입력 UV 좌표를 사용하여 입력 이미지를 색상 이미지로 매핑한 결과입니다. |

<a name="parameters"></a>

## 매개변수

|  |  |
|:---|:---|
| <b>배경색</b> <i>Float4</i> | 출력 이미지의 배경색입니다.<br>UV가 정의되지 않은 이미지 영역에서 배경이 표시됩니다(예: (0, 0, 0, 0)). |

## 예

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="uv-mapper-color.resources/UVMapper-Variant1-Before.jpg" alt="UVMapper-Variant1-Before">
      <br><i>이전</i>
    </td>
    <td>
      <img src="uv-mapper-color.resources/UVMapper-Variant1-After.jpg" alt="UVMapper-Variant1-After">
      <br><i>이후</i>
    </td>
  </tr>
</table>

</td>
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="uv-mapper-color.resources/UVMapper-Variant2-Before.jpg" alt="UVMapper-Variant2-Before">
      <br><i>이전</i>
    </td>
    <td>
      <img src="uv-mapper-color.resources/UVMapperColor-Variant2-After.jpg" alt="UVMapperColor-Variant2-After">
      <br><i>이후</i>
    </td>
  </tr>
</table>

</td>
</tr>
</table>

![그래프의 노드](uv-mapper-color.resources/UVMapperColor-Graph.jpg "그래프의 노드")
