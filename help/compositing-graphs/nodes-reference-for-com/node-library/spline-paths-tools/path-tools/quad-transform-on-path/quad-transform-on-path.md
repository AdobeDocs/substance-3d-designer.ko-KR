---
helpx_url: "https://helpx.adobe.com/kr/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/spline-paths-tools/path-tools/quad-transform-on-path.html"
breadcrumb-title: ''
description: 경로 노드에서 4중 변환을 사용하여 경로 곡선을 따라 요소에 2차 변환을 적용합니다.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Spline  Path Tools > Path Tools > Quad Transform on Path
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 패스 상의 4중 변형
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '182'
ht-degree: 2%

---


# 패스 상의 4중 변형

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![노드 아이콘](quad-transform-on-path.resources/quad-transform-on-paths-icon.png "노드 아이콘")

<b>인:</b> 스플라인 및 패스 도구 > 패스 도구

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 설명

4개의 핸들을 사용하여 패스를 변형합니다.

</td>
</tr>
</table>

<a name="inputs"></a>

## 입력

|  |  |
|:---|:---|
| <b>경로</b> <i>색상</i> | 인코딩된 세그먼트 경로 목록입니다. 이 입력을 [패스에 마스크](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/mask-to-paths/mask-to-paths.md) 또는 다른 *패스* 처리 노드에 연결합니다. |

<a name="outputs"></a>

## 출력

|  |  |
|:---|:---|
| <b>경로</b> <i>색상</i> | 변형된 패스. [패스 미리 보기](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/preview-paths/preview-paths.md)를 사용하여 결과가 어떻게 나타나는지 파악하거나 다른 패스 처리 노드를 사용하거나 [스플라인으로 패스](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/paths-to-spline/paths-to-spline.md)에 입력하여 스플라인으로 추가로 처리할 수 있습니다. |

<a name="parameters"></a>

## 매개변수

|  |  |
|:---|:---|
| <b>p00</b> <i>Float2</i> | 왼쪽 상단 핸들의 위치입니다. |
| <b>p01</b> <i>Float2</i> | 오른쪽 위 핸들의 위치입니다. |
| <b>p02</b> <i>Float2</i> | 왼쪽 아래 핸들의 위치입니다. |
| <b>p03</b> <i>Float2</i> | 오른쪽 아래 핸들의 위치입니다. |

## 예

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="quad-transform-on-path.resources/PathsPolygon_Variant1.jpg" alt="PathsPolygon_Variant1">
      <br><i>이전</i>
    </td>
    <td>
      <img src="quad-transform-on-path.resources/QuadTransformOnPaths-Variant1-After.jpg" alt="QuadTransformOnPaths-Variant1-After">
      <br><i>이후</i>
    </td>
  </tr>
</table>

</td>
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="quad-transform-on-path.resources/PathsPolygon_Variant1.jpg" alt="PathsPolygon_Variant1">
      <br><i>이전</i>
    </td>
    <td>
      <img src="quad-transform-on-path.resources/QuadTransformOnPaths-Variant2-After.jpg" alt="QuadTransformOnPaths-Variant2-After">
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

![노드 예 1](quad-transform-on-path.resources/QuadTransformOnPaths-Demo2.gif "노드 예 1")

</td>
<td style="border: 0;" valign="top">

![노드 예 2](quad-transform-on-path.resources/QuadTransformOnPaths-Demo1.gif "노드 예 2")

</td>
</tr>
</table>
