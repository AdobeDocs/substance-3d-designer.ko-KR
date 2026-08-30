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
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '235'
ht-degree: 2%

---


# 패스 2D 변형

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![노드 아이콘](path-2d-transform.resources/path-2d-transform-icon.png "노드 아이콘")

<b>인:</b> 스플라인 및 패스 도구 > 패스 도구

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 설명

기즈모를 사용하여 패스를 변형합니다.

</td>
</tr>
</table>

<a name="inputs"></a>

## 입력

|  |  |
|:---|:---|
| <b>경로</b> <i>색상</i> | 인코딩된 세그먼트 경로 목록입니다. 이 입력을 [패스에 마스크](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/mask-to-paths/mask-to-paths.md) 또는 다른 패스 처리 노드에 연결합니다. |

<a name="outputs"></a>

## 출력

|  |  |
|:---|:---|
| <b>경로</b> <i>색상</i> | 변형된 패스. [패스 미리 보기](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/preview-paths/preview-paths.md)를 사용하여 결과가 어떻게 나타나는지 파악하거나 다른 패스 처리 노드를 사용하거나 [스플라인으로 패스](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/paths-to-spline/paths-to-spline.md)에 입력하여 스플라인으로 추가로 처리할 수 있습니다. |

<a name="parameters"></a>

## 매개변수

|  |  |
|:---|:---|
| <b>매트릭스 변환</b> <i>Float4</i> | 스플라인에 적용된 변형 행렬 다음 세 가지 모드의 행렬 매개 변수를 편집할 수 있습니다.<br>*- 변형 기즈모:* 스플라인 2}2D 보기에 표시된 기즈모의 핸들을 수정합니다.](../../../../../../interface/2d-view/2d-view.md) d 노드를 선택할 때 스플라인 4- 노드를 선택합니다.{Rotation/control: 개별 스플라인의 회전 및 회전 제어&#x200B;*. [<br>*&#x200B;값은 항상 현재 변환에 상대적으로 적용됩니다. 예를 들어 50% 너비를 두 번 적용하면 25% 너비가 됩니다.<br>*- 행렬 값:* <b>행렬 값 편집</b> 버튼을 클릭하여 행렬의 원시 숫자 값을 직접 입력합니다. |
| <b>오프셋</b> <i>Float2</i> | X(가로) 및 Y(세로)의 스플라인에 위치 오프셋을 적용합니다. |

## 예

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="path-2d-transform.resources/PathsPolygon_Variant1.jpg" alt="PathsPolygon_Variant1">
      <br><i>이전</i>
    </td>
    <td>
      <img src="path-2d-transform.resources/Paths2DTransform-Variant1.jpg" alt="Paths2DTransform-Variant1">
      <br><i>이후</i>
    </td>
  </tr>
</table>

</td>
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="path-2d-transform.resources/PathsPolygon_Variant1.jpg" alt="PathsPolygon_Variant1">
      <br><i>이전</i>
    </td>
    <td>
      <img src="path-2d-transform.resources/Paths2DTransform-Variant2.jpg" alt="Paths2DTransform-Variant2">
      <br><i>이후</i>
    </td>
  </tr>
</table>

</td>
</tr>
</table>
