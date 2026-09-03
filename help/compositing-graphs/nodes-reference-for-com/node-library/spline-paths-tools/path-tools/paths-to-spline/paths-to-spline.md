---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/spline-paths-tools/path-tools/paths-to-spline.html"
breadcrumb-title: ''
description: 스플라인 기반 노드에 사용할 경로 데이터를 스플라인으로 변환하려면 스플라인 경로 노드를 사용합니다.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Spline  Path Tools > Path Tools > Paths to Spline
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 패스를 스플라인으로
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '251'
ht-degree: 1%

---


# 패스를 스플라인으로

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![노드 아이콘](paths-to-spline.resources/paths-to-spline-01.png "노드 아이콘")

<b>인:</b> 스플라인 및 패스 도구 > 패스 도구

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 설명

패스를 스플라인으로 변환하고, 이 스플라인은 [스플라인 렌더링](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/spline-tools/spline-render/spline-render.md) 노드를 사용하여 시각화하고 [스플라인 노드](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/spline-tools/spline-tools.md)를 사용하여 처리합니다.

</td>
</tr>
</table>

>[!NOTE]
>
> 스플라인은 곡선이므로 패스의 선명도를 유지할 수 없습니다. 패스를 스플라인으로 변환할 때 모양이 약간 매끄러워질 수 있습니다.

>[!TIP]
>
> 이 노드는 [패스에 마스크 적용](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/mask-to-paths/mask-to-paths.md) 노드 뒤에 사용하여 마스크를 스플라인으로 변환하는 체인을 만들 수 있습니다.

<a name="inputs"></a>

## 입력

|  |  |
|:---|:---|
| <b>경로</b> <i>색상</i> | 인코딩된 세그먼트 경로 목록입니다. 이 입력을 [패스에 마스크](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/mask-to-paths/mask-to-paths.md) 또는 다른 패스 처리 노드에 연결합니다. |

<a name="outputs"></a>

## 출력

|  |  |
|:---|:---|
| <b>스플라인 코드</b> <i>색상</i> | 색상 이미지의 RGBA 채널로 인코딩된 입력 스플라인의 좌표:<br><b>R</b> - X 위치<br><b>G</b> - Y 위치<br><b>B</b> - Height<br><b>A</b> - 압축된 데이터:<br> * 기호: 스플라인이 닫힘(네거티브) 또는 열림(포지티브);<br> * 절대값: Thickness + 1. |
| <b>스플라인 데이터</b> <i>색상</i> | <b>색상</b> 이미지의 RGBA 채널로 인코딩된 입력 스플라인의 추가 데이터:<br><b>R</b> - 접선 X<br><b>G</b> - 접선 Y<br><b>B</b> - 미사용<br><b>A</b> - 미사용 |
| <b>스플라인 양</b> <i>정수</i> | 입력 스플라인의 수입니다. |

<a name="parameters"></a>

## 매개변수

|  |  |
|:---|:---|
| <b>스플라인 정밀도</b> <i>정수</i> | 해당 스플라인을 빌드하기 위해 입력된 [패스] 입력의 각 패스에서 샘플링된 정점 수의 밑이 2인 로그(log2)입니다. |

## 예

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="paths-to-spline.resources/paths-to-spline-02.jpg" alt="PathsToSpline-Variant1-Before">
      <br><i>이전</i>
    </td>
    <td>
      <img src="paths-to-spline.resources/paths-to-spline-03.jpg" alt="PathsToSpline-Variant1-After">
      <br><i>이후</i>
    </td>
  </tr>
</table>

</td>
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="paths-to-spline.resources/paths-to-spline-04.jpg" alt="PathsToSpline-Variant2-Before">
      <br><i>이전</i>
    </td>
    <td>
      <img src="paths-to-spline.resources/paths-to-spline-05.jpg" alt="PathsToSpline-Variant2-After">
      <br><i>이후</i>
    </td>
  </tr>
</table>

</td>
</tr>
</table>
