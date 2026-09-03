---
helpx_url: "https://helpx.adobe.com/kr/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/spline-paths-tools/path-tools/paths-warp.html"
breadcrumb-title: ''
description: 경로 뒤틀기 노드를 사용하면 곡선 및 유기적인 패턴을 만들기 위해 경로 곡선을 따라 텍스처를 뒤틀 수 있습니다.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Spline  Path Tools > Path Tools > Paths Warp
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 패스 뒤틀기
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '215'
ht-degree: 2%

---


# 패스 뒤틀기

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![노드 아이콘](paths-warp.resources/paths-warp-01.png "노드 아이콘")

<b>인:</b> 스플라인 및 패스 도구 > 패스 도구

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 설명

<b>그레이디언트 입력</b>에 따라 입력 경로를 변형합니다. ([뒤틀기](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/warp/warp.md) 노드와 같은 효과)

</td>
</tr>
</table>

<a name="inputs"></a>

## 입력

|  |  |
|:---|:---|
| <b>경로</b> <i>색상</i> | 인코딩된 세그먼트 경로 목록입니다. 이 입력을 [패스에 마스크](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/mask-to-paths/mask-to-paths.md) 또는 다른 패스 처리 노드에 연결합니다. |
| <b>그라디언트 입력</b> <i>회색 음영</i> | 뒤틀기의 양과 방향을 모두 제어하는 Height 같은 입력입니다. ([뒤틀기](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/warp/warp.md) 노드와 같은 효과) |

<a name="outputs"></a>

## 출력

|  |  |
|:---|:---|
| <b>경로</b> <i>색상</i> | 변형된 경로입니다. [패스 미리 보기](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/preview-paths/preview-paths.md)를 사용하여 결과가 어떻게 나타나는지 파악하거나 다른 패스 처리 노드를 사용하거나 [스플라인으로 패스](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/paths-to-spline/paths-to-spline.md)에 입력하여 스플라인으로 추가로 처리할 수 있습니다. |

<a name="parameters"></a>

## 매개변수

|  |  |
|:---|:---|
| <b>강도</b> <i>부동</i> | <b>강도</b> 매개 변수는 뒤틀기의 강도를 설정합니다. |
| <b>단계 수</b> <i>정수</i> | 더 높은 값을 사용하여 작은 단위로 입력 패스를 뒤틀려면 선택합니다.<br>이것은 특히 높은 <b>강도</b> 값을 사용할 때 경로가 스스로 교차하지 못하도록 할 수 있습니다. |

## 예

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="paths-warp.resources/paths-warp-02.jpg" alt="PathsToSpline-Variant2-Before">
      <br><i>이전</i>
    </td>
    <td>
      <img src="paths-warp.resources/paths-warp-03.jpg" alt="PathsWarp-Variant1-After">
      <br><i>이후</i>
    </td>
  </tr>
</table>

</td>
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="paths-warp.resources/paths-warp-02.jpg" alt="PathsToSpline-Variant2-Before">
      <br><i>이전</i>
    </td>
    <td>
      <img src="paths-warp.resources/paths-warp-04.jpg" alt="PathsWarp-Variant2-After">
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

![노드 예 1](paths-warp.resources/paths-warp-05.gif "노드 예 1")

</td>
<td style="border: 0;" valign="top">



</td>
</tr>
</table>
