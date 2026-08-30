---
helpx_url: "https://helpx.adobe.com/kr/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/spline-paths-tools/path-tools/preview-paths.html"
breadcrumb-title: ''
description: 경로 미리보기 노드를 사용하여 디버깅 및 확인을 위해 2D 뷰에서 경로 데이터를 시각화할 수 있습니다.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Spline  Path Tools > Path Tools > Preview Paths
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 패스 미리 보기
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '169'
ht-degree: 2%

---


# 패스 미리 보기

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![노드 아이콘](preview-paths.resources/preview-paths-icon.png "노드 아이콘")

<b>인:</b> 스플라인 및 패스 도구 > 패스 도구

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 설명

지정된 배경 위에 패스의 선분과 정점을 추적합니다. 패스당 하나의 임의의 색상입니다.

[패스에 마스크 적용](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/mask-to-paths/mask-to-paths.md)의 <b>미리 보기</b> 출력과 비슷한 결과를 얻을 수 있지만 더 많은 옵션이 제공됩니다.

</td>
</tr>
</table>

<a name="inputs"></a>

## 입력

|  |  |
|:---|:---|
| <b>배경</b> <i>색상</i> | 배경 이미지 위에 패스 표시 또한 렌더링 크기를 제어합니다. |
| <b>경로</b> <i>색상</i> | 인코딩된 세그먼트 경로 목록입니다. 이 입력을 [패스에 마스크](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/mask-to-paths/mask-to-paths.md) 또는 다른 패스 처리 노드에 연결합니다. |

<a name="parameters"></a>

## 매개변수

|  |  |
|:---|:---|
| <b>모퉁이 표시</b> <i>부울</i> | 모퉁이(더하기 혼합)로 표시된 각 정점에 정사각형을 표시합니다. |
| <b>정점 표시</b> <i>부울</i> | 각 정점에 원형 모양을 표시합니다(추가 혼합). 모퉁이는 여전히 정사각형으로 표시됩니다. |
| <b>세그먼트 Thickness(px)</b> <i>부동</i> | 렌더링된 선분의 Thickness을 픽셀 단위로 조정합니다. |

## 예

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![노드 예 1](preview-paths.resources/PathsToSpline-Variant2-Before_1.jpg "노드 예 1")

</td>
<td style="border: 0;" valign="top">

![노드 예 2](preview-paths.resources/PathsToSpline-Variant1-Before_1.jpg "노드 예 2")

</td>
</tr>
</table>
