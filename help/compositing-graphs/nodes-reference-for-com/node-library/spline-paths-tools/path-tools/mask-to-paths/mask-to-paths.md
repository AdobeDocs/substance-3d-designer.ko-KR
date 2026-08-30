---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/spline-paths-tools/path-tools/mask-to-paths.html"
breadcrumb-title: ''
description: 마스크-패스 노드를 사용하면 마스크 텍스처를 패스 데이터로 변환하여 패스를 계속 생성할 수 있습니다.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Spline  Path Tools > Path Tools > Mask to Paths
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 패스에 마스크 적용
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '1113'
ht-degree: 0%

---


# 패스에 마스크 적용

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![노드 아이콘](mask-to-paths.resources/mask-to-paths-icon.png "노드 아이콘")

<b>인:</b> 스플라인 및 패스 도구 > 패스 도구

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 설명

회색 음영 입력 패턴 <b>마스크</b>를 출력 <b>패스</b>로 인코딩된 패스 세그먼트 목록으로 변환합니다.

생성된 패스의 시작 위치와 목록에서 해당 순서를 제어할 수 있습니다.

생성된 경로는 전용 노드(예: [경로 2D}경로](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/path-2d-transform/path-2d-transform.md), {2 변환 경로](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/paths-warp/paths-warp.md), [스플라인 경로](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/paths-to-spline/paths-to-spline.md) 노드를 사용하여 스플라인으로 변환되어 모양을 매핑하거나 산란으로 지정할 수 있습니다.[

</td>
</tr>
</table>

>[!NOTE]
>
> 경로를 인코딩하는 데 사용되는 방법은 [경로 형식 사양](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/paths-format-spe/paths-format-specifications.md) 페이지에 설명되어 있습니다.

<a name="inputs"></a>

## 입력

|  |  |
|:---|:---|
| <b>마스크</b> <i>회색 음영</i> | 패스 목록으로 변환해야 하는 입력 패턴입니다. |

<a name="outputs"></a>

## 출력

|  |  |
|:---|:---|
| <b>미리 보기</b> <i>색상</i> | 매개 변수의 효과를 시각화하는 데 도움이 되도록 마스크 위에 합성된 미리 보기입니다. |
| <b>경로</b> <i>색상</i> | 색상 이미지로 인코딩되는 경로의 목록입니다. 각 경로는 인코딩된 세그먼트 목록을 설명합니다.<br>결과는 다른 패스 처리 노드를 사용하여 처리하거나 [스플라인으로 패스](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/paths-to-spline/paths-to-spline.md) 노드로 보내 스플라인으로 추가로 처리할 수 있습니다. |

<a name="parameters"></a>

## 매개변수

|  |  |
|:---|:---|
| <b>마스크 매끄럽게</b> <i>부동</i> | 입력 마스크에 매끄러움을 적용합니다.<br>입력 패턴의 가장자리가 매우 선명하여 일반적으로 아티팩트가 발생할 때 유용합니다. |
| <b>마스크 임계값</b> <i>부동</i> | 모양의 외부(값 &lt; 마스크 임계값)와 내부(값 > 마스크 임계값)를 구분하는 데 사용되는 <b>마스크</b>의 회색 음영 값입니다. |
| <b>데시메이트 경로</b> <i>부동</i> | 암묵적으로 생성될 선분의 양을 제어합니다.<br>높은 양의 데시메이션은 둥근 모양을 다소 다각형으로 만들지만 데시메이션은 픽셀별로 거의 하나의 선분을 생성하지 않습니다.<br>적절한 양은 직선에 대한 중간 지점을 많이 만들지 않고도 직선과 곡선 모두의 모양에 더 잘 맞춥니다. |
| <b>열린 경로 닫기</b> <i>부울</i> | 열린 패스의 시작 정점과 끝 정점 사이에 선분을 만듭니다.<br>이 옵션을 사용하지 않으면 패턴을 가로지르는 원치 않는 선이 예기치 않은 방식으로 수정될 수 있지만 경로가 더 이상 닫히지 않을 수 있습니다. |
| <b>모퉁이 임계값</b> <i>부동</i> | 경로들로 인코딩된 각각의 정점은 그것이 하드(즉, 코너) 또는 스무드인지를 표시하는 플래그를 보유할 수 있다.<br>이 매개 변수를 사용하면 인접한 선분 사이의 각도에 따라 더 많거나 더 적은 모퉁이를 표시할 수 있습니다.<br><i>참고:</i> 이 &#39;모퉁이&#39; 플래그는 현재 기존 노드에서 지원되지 않지만 [패스 정점 프로세서](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/paths-vertex-processor/paths-vertex-processor.md) 노드에서 사용할 수 있습니다. [미리 보기 경로](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/preview-paths/preview-paths.md) 노드를 사용하여 모퉁이를 시각화할 수도 있습니다. |
| <b>경로 시작 모드</b> <i>정수</i> | 마스크에서 모양 주위에 생성된 각 패스의 시작이 될 정점을 선택하는 방법입니다.<br>이는 여러 스플라인 노드가 스플라인의 시작과 끝을 사용하므로 전용 노드를 사용하여 생성된 <b>패스를 스플라인으로 변환</b>할 때 상당한 영향을 미칩니다.<br>*- 가장 예리한 정점:* 이전 정점과 다음 정점이 가장 낮은 각도를 이루는 정점&#x200B;<br>*- 지정된 방향의 극단에 있는 정점:* 지정된 방향의 마지막 정점&#x200B;<br>*- 지정된 위치에 가장 가까운 정점<br>** 사용자 정의 시작 함수:* 사용자 정의 함수를 사용하여 각 패스의 시작으로 사용할 정점을 선택합니다<br> |
| <b>시작 방향</b> <i>부동</i> | 시작 정점을 선택하는 데 사용되는 방향을 설명하는 각도입니다. 각 패스에 대해 이 방향의 마지막 정점이 선택됩니다.<br>값은 X-왼쪽 방향 벡터를 회전하는 데 사용되는 *회전수*&#x200B;입니다. 0은 방향 벡터(-1, 0)를 설정하고 0.25(90도)는 방향 벡터((0, 1)를 설정합니다.<br><i>참고:</i> 이 매개 변수는 <b>경로 시작 모드</b>가 &#39;지정된 방향의 최단 정점&#39;으로 설정된 경우에 사용할 수 있습니다. |
| <b>시작 대상 위치</b> <i>Float2</i> | 시작 정점을 선택하는 데 사용된 이미지의 위치입니다.<br>각 패스에 대해 선택한 <b>패스 시작 모드</b>에 따라 이 위치에 가장 가깝거나 가장 먼 정점이 선택됩니다.<br><i>참고:</i> 이 매개 변수는 <b>패스 시작 모드</b>가 &#39;지정한 위치에 가장 가까운 정점&#39; 또는 &#39;지정한 위치에서 가장 먼 정점&#39;으로 설정되어 있을 때 사용할 수 있습니다 |
| <b>시작 함수</b> <i>부동</i> | 시작 정점을 선택하는 데 사용되는 함수입니다. Float 값을 반환합니다.<br>각 정점에 대해 함수가 실행되고 함수가 *가장 높은 결과*&#x200B;를 반환하는 정점이 선택됩니다.<br>사용 가능한 변수:<br>*-* vertex.cornerness(부동)*:* 모서리가 될 후보인 정점의 점수&#x200B;<br>*-* vertex.pos(부동2)*:* 이미지 공간의 정점 위치<br><i>참고:</i> 이 매개 변수는 경로 시작 모드가 &#39;지정된 위치에 가장 가까운 정점&#39; 또는 &#39;사용자 지정 시작 함수&#39;로 설정된 경우에 사용할 수 있습니다. |
| <b>주문 모드</b> <i>정수</i> | 생성된 경로 순서 지정 방법입니다.<br>경로 위치 또는 크기 *테두리 상자*(Bbox)를 경로 순서 지정 기준으로 사용할 수 있습니다.<br>이는 여러 스플라인 노드가 스플라인의 순서를 사용하므로 전용 노드를 사용하여 생성된 <b>경로를 스플라인으로 변환할 때 큰 영향을 미칩니다</b>.<br>*- 레거시(고속):* 성능이 크게 향상된 이 노드의 이전 버전에서 사용된 메서드&#x200B;<br>*- 방향을 따라 Bbox 중심 위치별:* 경로는 Bbox 중심 위치에 따라 지정된 방향을 따라 처음부터 마지막 위치까지 순서가 지정됩니다&#x200B;<br>*- 방향을 따라 Bbox Bbox 왼쪽 위 위치별:* 경로는 왼쪽 위 위치에 따라 정렬됩니다. 지정된 방향을 따라 Bbox의 첫 번째부터 마지막 번째까지 모퉁이&#x200B;<br>*- Bbox 크기 기준 - 가장 큰 경로에서 가장 작은 경로* Bbox 크기에 따라 정렬됩니다. 가장 큰 경로에서 가장 작은 경로&#x200B;<br>*- Bbox 크기 기준 - 가장 작은 경로에서 가장 큰 경로* Bbox 크기에 따라 정렬됩니다. 가장 작은 경로에서 가장 큰 경로&#x200B;<br>*- 사용자 지정 정렬 함수:* 사용자 지정 함수를 사용하여 경로를 정렬합니다. |
| <b>순서 지정 방향</b> <i>부동</i> | 패스를 처음 시작부터 끝까지 해당 방향을 따라 정렬하는 데 사용되는 방향을 설명하는 각도입니다.<br>값은 X 왼쪽 방향 벡터를 회전하는 데 사용되는 *회전 수*&#x200B;입니다. 즉, 0은 (-1, 0)의 방향 벡터를 설정하고, 0.25(90도)는 (0, 1)의 방향 벡터를 설정한다. |
| <b>순서 지정 함수</b> <i>부동</i> | 경로 순서를 지정하는 데 사용되는 함수입니다. Float 값을 반환합니다.이 함수 값에 따라 <br>경로가 *오름차순*&#x200B;으로 정렬됩니다. 즉, 각 Path에 대한 함수의 결과는 Paths를 정렬하는 데 사용되는 *정렬 키*&#x200B;입니다.<br>사용 가능한 변수:<br>* bbox.center(부동2): Path Bbox의 가운데 위치<br>* bbox.topleft(부동2): Path Bbox의 왼쪽 상단 모서리 위치<br>* bbox.size(부동2): Path Bbox의 크기(X: width, Y: Height) |

## 예

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="mask-to-paths.resources/MaskToPaths-Variant2-Before.jpg" alt="MaskToPaths-Variant2-Before">
      <br><i>이전</i>
    </td>
    <td>
      <img src="mask-to-paths.resources/MaskToPaths-Variant2-After.jpg" alt="MaskToPaths-Variant2-After">
      <br><i>이후</i>
    </td>
  </tr>
</table>

</td>
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="mask-to-paths.resources/MaskToPaths-Variant1-Before.jpg" alt="MaskToPaths-Variant1-Before">
      <br><i>이전</i>
    </td>
    <td>
      <img src="mask-to-paths.resources/MaskToPaths-Variant1-After.jpg" alt="MaskToPaths-Variant1-After">
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

![노드 예 2](mask-to-paths.resources/MaskToPaths-Demo2.gif "노드 예 2"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![노드 예 1](mask-to-paths.resources/MaskToPaths-Demo1.gif "노드 예 1"){zoomable="yes"}

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![노드 예 3: 시작 모드](mask-to-paths.resources/MaskToPaths-Demo3.gif "노드 예 3: 시작 모드"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![노드 예 3: 순서 지정 모드](mask-to-paths.resources/MaskToPaths-Demo4.gif "노드 예 3: 순서 지정 모드"){zoomable="yes"}

</td>
</tr>
</table>
