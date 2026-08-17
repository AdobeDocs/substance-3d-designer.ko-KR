---
helpx_url: "https://helpx.adobe.com/kr/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/spline-paths-tools/working-with-path-and-spline-tools.html"
breadcrumb-title: ''
description: 패스와 자유 곡선 도구를 사용하여 그래프에 절차 패턴과 유기적인 모양을 만드는 방법을 살펴보세요.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Spline  Path Tools > Working with Path  Spline tools
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 패스 자유 곡선 도구 작업
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '1544'
ht-degree: 0%

---


# 패스 및 자유 곡선 도구 작업

패스 및 스플라인 도구 세트 는 이미지를 그리고 매핑하고 산란 하는 데 사용되는 해상도에 관계없이 모양과 곡선을 제작하고 편집할 수 있는 노드 컬렉션입니다.

## 개요

### 패스와 스플라인이란 무엇입니까?

<b>패스</b>는 직선으로 연결된 일련의 점입니다.

<b>스플라인</b>은 제어점과 해당 점의 접선에 의해 궤도 모양이 형성되는 매끄러운 곡선입니다.\
또한 각 점은 이미지의 매핑, 뒤틀기 및 산포를 제어하는 데 사용되는 스플라인의 Height 및 Thickness 특성을 제어합니다.

각각 닫힌 모양이나 열린 모양을 만들 수 있습니다.

<table>
<tr style="border: 0;">
<td width="100.00%" style="border: 0;" valign="top">

### 노드 출력

노드는 경로와 스플라인을 나타내는 <b>인코딩된 데이터</b>를 포함하는 이미지를 출력합니다.

예를 들어 오른쪽 이미지는 [패스 다각형](../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/paths-polygon/paths-polygon.md) 노드에서 출력한 이미지를 나타냅니다.

</td>
<td width="33.33%" style="border: 0;" valign="top">

![패스 다각형 출력](../../../../../assets/PathsPolygon_Data.jpg "패스 다각형 출력")

</td>
</tr>
</table>

따라서 해당 이미지가 생성하는 이미지는 그래픽 요소로 직접 사용할 수 없습니다. 이러한 효과는 도구 세트의 다른 노드에서 처리해야 하므로 그래픽 결과로 변환한 다음 Substance 그래프에 사용할 수 있는 나머지 노드와 함께 사용할 수 있습니다.

패스 및 스플라인을 사용하여 작업할 때 전용 [패스 미리 보기](../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/preview-paths/preview-paths.md) 노드를 사용한 경로 및 전용 <b>미리 보기</b> 출력을 사용한 이미지에 매핑된 해당 개체를 미리 볼 수 있습니다.

<table>
<tr style="border: 0;">
<td width="100.00%" style="border: 0;" valign="top">

### 2D 보기 상호 작용

도구 집합의 노드 중 상당수는 컨트롤 기즈모를 사용하여 [2D 보기](../../../../../interface/2d-view/2d-view.md)에서 직접 편집할 수 있는 기능을 제공합니다. 이러한 기즈모에는 위치 기즈모와 변환 행렬이 포함된다.

예를 들어 [스플라인(큐빅)](../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/spline-tools/spline-cubic/spline-cubic.md) 또는 [스플라인(폴리 쿼드라틱)](../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/spline-tools/spline-poly-quadratic/spline-poly-quadratic.md)과 같은 스플라인 생성 노드를 사용하면 스플라인의 제어점을 이동할 수 있습니다. 패스의 경우 [패스의 쿼드 변환](../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/quad-transform-on-path/quad-transform-on-path.md)을 선택하면 유사한 컨트롤이 있습니다.

</td>
<td width="33.33%" style="border: 0;" valign="top">

![2D 보기의 스플라인 큐빅](../../../../../assets/SplineCubic-Demo.gif "2D 보기의 스플라인 큐빅")

</td>
</tr>
</table>

### 성능

경로 및 자유 곡선 도구는 도구 세트를 사용하여 작업할 때 최고의 성능과 응답성을 보장하기 위한 몇 가지 설정을 염두에 두어야 할 만큼 많은 계산이 필요합니다.

1. 이 도구 집합은 GPU에서 훨씬 빠르게 실행되는 <b>Substance 엔진</b> 기능을 광범위하게 사용합니다. 따라서 시스템에 대한 엔진의 GPU 버전을 사용하십시오. <b>Direct3D</b>(Windows) 또는 <b>OpenGL</b>(macOS).\
   <b>F9</b> 키를 누르거나 기본 메뉴 막대에서 <b>도구 > 엔진 전환...</b>으로 이동하여 엔진을 전환할 수 있습니다.
1. 그런 다음 [환경 설정](../../../../../interface/preferences-window/preferences-window.md)의 <b>그래프</b> 섹션에서 <b>컨텍스트 편집</b>을 해제하는 것이 좋습니다(<b>편집 > 환경 설정... 이동).이 창에 액세스하려면 주 메뉴 표시줄의 </b>.\
   직접 편집을 사용하면 호스트 그래프의 컨텍스트에서 인스턴스 노드를 열 수 있습니다. 이 방법은 매우 편리하지만 도구 세트의 이미지 캐시에 필요한 계산이 기하급수적으로 증가하는 부작용이 있습니다.

이 두 가지 설정 중 하나를 권장 상태로 변경하면 성능이 크게 향상됩니다.

![라이브러리의 경로 도구](../../../../../assets/PathsTools.jpg "라이브러리의 경로 도구")

## 경로 도구

### 패스 생성

[패스 다각형](../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/paths-polygon/paths-polygon.md)은 지정한 반경과 면 수의 다각형 모양으로 패스를 생성합니다.

또는 [패스에 마스크 적용](../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/mask-to-paths/mask-to-paths.md) 노드를 사용하여 회색 음영 이미지에서 패스를 추출할 수 있습니다.\
이는 현재 복잡한 모양을 만드는 유일한 방법이며 [Substance 그래프 노드](../../../../../compositing-graphs/nodes-reference-for-com/nodes-reference-for-substance-compositing-graphs.md)의 전체 라이브러리를 활용하여 패스로 변환될 모양을 만들 수 있습니다.

![경로 생성 노드](../../../../../assets/Paths_Generation.jpg "경로 생성 노드"){width="600px"}

### 패스 편집

[패스 2D 변형](../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/path-2d-transform/path-2d-transform.md), [패스 뒤틀기](../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/paths-warp/paths-warp.md) 및 [패스 상의 4중 변형](../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/quad-transform-on-path/quad-transform-on-path.md)을 사용하면 패스 모양을 편집할 수 있습니다.

[패스 선택](../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/paths-select/paths-select.md) 노드를 사용하여 인덱스 또는 길이별로 패스를 선택하여 원하지 않는 패스를 제거할 수도 있습니다.

[패스 정점 프로세서](../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/paths-vertex-processor/paths-vertex-processor.md) 노드를 사용하여 패스의 각 지점에서 보다 복잡한 처리를 수행할 수 있습니다. 더 가벼운 조정을 위해 [간단한 버전](../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/paths-vertex-processor-1/paths-vertex-processor-simple.md)이(가) 있습니다.

<table>
<tr style="border: 0;">
<td width="100.00%" style="border: 0;" valign="top">

### 패스 미리 보기 노드

전용 [미리 보기 경로](../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/preview-paths/preview-paths.md) 노드를 사용하여 패스 노드의 결과를 미리 봅니다.\
이 노드에는 출력이 없습니다. 노드에서 LMB를 두 번 클릭하여 [2D 보기](../../../../../interface/2d-view/2d-view.md)에 미리 보기를 표시합니다.

미리 보기에서 개별 패스의 고유한 색상을 사용하여 각 패스를 쉽게 구분할 수 있습니다.

</td>
<td width="33.33%" style="border: 0;" valign="top">

![미리 보기 경로 노드](../../../../../assets/PreviewPaths_Node.jpg "미리 보기 경로 노드")

</td>
</tr>
</table>

### 패스를 스플라인으로

[스플라인으로 패스](../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/paths-to-spline/paths-to-spline.md) 노드를 사용하여 패스를 스플라인으로 변환하면 패스가 있는 스플라인 전용 전체 도구 세트를 활용할 수 있습니다.

스플라인은 곡선이므로 패스의 선명도를 유지할 수 없다는 점을 명심하십시오. 패스를 스플라인으로 변환할 때 모양이 약간 매끄러워질 수 있습니다.

패스를 통해 스플라인 도구 세트를 활용하는 데 매우 유용한 조합은 다음과 같습니다.

<b>마스크 > 패스에 마스크 > 스플라인에 패스</b>

![스플라인 경로](../../../../../assets/Spline_PathToSpline.jpg "스플라인 경로")

### 경로 형식 사양

패스 노드는 컬러 이미지로 인코딩된 패스의 데이터를 출력하기 때문에 미리 보기 패스 노드가 필요합니다.\
이 인코딩은 [경로 형식 사양](../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/paths-format-spe/paths-format-specifications.md) 페이지에 설명된 사양을 따릅니다.

이 사양을 사용하여 이 형식을 사용하여 고유한 노드를 만들고 [패스 정점 프로세서](../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/paths-vertex-processor/paths-vertex-processor.md) 노드를 최대한 활용할 수 있습니다.

![라이브러리의 자유 곡선 도구](../../../../../assets/SplineTools.jpg "라이브러리의 자유 곡선 도구")

## 자유 곡선 도구

### 스플라인 생성

스플라인은 [스플라인 원](../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/spline-tools/spline-circle/spline-circle.md), [스플라인(큐빅)](../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/spline-tools/spline-cubic/spline-cubic.md) 또는 [스플라인(폴리 쿼드라틱)](../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/spline-tools/spline-poly-quadratic/spline-poly-quadratic.md)과 같은 노드를 사용하여 생성할 수 있습니다. 이러한 노드를 사용하면 노드에 따라 서로 다른 컨트롤을 사용하여 임의 궤적의 스플라인을 그릴 수 있습니다.

또는 [스플라인으로 패스](../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/paths-to-spline/paths-to-spline.md) 노드를 사용하여 패스에서 스플라인을 추출할 수 있습니다.\
스플라인은 곡선이므로 패스의 선명도를 유지할 수 없다는 점을 명심하십시오. 패스를 스플라인으로 변환할 때 모양이 약간 매끄러워질 수 있습니다.

패스를 통해 스플라인 도구 세트를 활용하는 데 매우 유용한 조합은 다음과 같습니다.

<b>마스크 > 패스에 마스크 > 스플라인에 패스</b>

스플라인을 사용하면 더 많은 스플라인을 생성할 수 있습니다. 예를 들어 [스플라인 브리지(2개의 스플라인)](../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/spline-tools/spline-bridge-2-splines/spline-bridge-2-splines.md) 및 [스플라인 브리지(목록)](../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/spline-tools/spline-bridge-list/spline-bridge-list.md)는 순서대로 스플라인 목록을 가로지르는 스플라인을 생성합니다.

### 스플라인 편집

[스플라인 2D 변형](../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/spline-tools/spline-2d-transform/spline-2d-transform.md) 및 [스플라인 뒤틀기](../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/spline-tools/spline-warp/spline-warp.md)를 사용하면 스플라인의 모양을 편집할 수 있습니다.

또한 인덱스로 패스를 선택하고 [스플라인 선택](../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/spline-tools/spline-select/spline-select.md) 노드를 사용하여 스플라인을 트리밍하여 원하지 않는 스플라인을 제거할 수 있습니다.

궤적 외에도 스플라인의 Height 및 Thickness 속성은 [스플라인 샘플 Height](../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/spline-tools/spline-sample-height/spline-sample-height.md) 및 [스플라인 샘플 Thickness](../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/spline-tools/spline-sample-thickness/spline-sample-thickness.md)을 사용하여 팩트 이후에 조정할 수 있습니다.

마지막으로 [스플라인 병합 목록](../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/spline-tools/spline-merge-list/spline-merge-list.md) 노드를 사용하여 개별 스플라인을 단일 스플라인으로 병합할 수 있습니다.

### 스플라인 추가

스플라인을 만들고 편집할 때 여러 개의 스플라인을 함께 결합해야 해당 스플라인을 동시에 조정하거나 사용할 수 있습니다.

스플라인은 <b>순서가 지정된 목록</b>으로 저장되고 처리된다는 점에 유의해야 합니다.

스플라인 결합은 [스플라인 추가](../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/spline-tools/spline-append/spline-append.md) 노드를 사용하여 수행됩니다. 추가는 주문받은 개체 끝에 무엇인가를 추가하는 행위이다. 실제로 노드는 첫 번째 세트의 끝에 두 번째 세트를 추가하여 두 스플라인 목록을 결합합니다.

따라서 스플라인을 함께 첨부하는 순서를 고려하는 것이 매우 중요합니다.

이는 [스플라인 브리지(목록)](../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/spline-tools/spline-bridge-list/spline-bridge-list.md), [스플라인 브리지 매퍼](../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/spline-tools/spline-bridge-mapper-gra/spline-bridge-mapper-grayscale.md) 및 [스플라인 병합 목록](../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/spline-tools/spline-merge-list/spline-merge-list.md)과 같이 스플라인을 함께 결합해야 하는 노드에 영향을 줍니다.

![링크 만들기 모드로 스플라인 추가](../../../../../assets/LinkCreationMode_Splines.gif "링크 만들기 모드로 스플라인 추가")

### 스플라인 입력 및 출력

스플라인은 커넥터 그룹을 사용하여 한 노드에서 다른 노드로 전달됩니다.

* <b>스플라인 좌표&#x200B;</b>*색상*&#x200B;색상 이미지의 RGBA 채널로 인코딩된 입력 스플라인의 점 좌표입니다.
* <b>스플라인 데이터&#x200B;</b>*색상*&#x200B;색상 이미지의 RGBA 채널로 인코딩된 입력 스플라인의 추가 데이터입니다.
* <b>스플라인 양&#x200B;</b>*정수*&#x200B;입력 스플라인의 수입니다.

소스 노드의 각 출력 커넥터는 대상 노드에서 일치하는 이름의 입력 커넥터에 연결되어야 합니다.

이러한 연결을 더 빠르게 하려면 <b>재질</b> 또는 <b>압축 재질</b>을 사용할 수 있습니다 [링크 만들기 모드](../../../../../interface/the-graph-view/link-creation-modes/link-creation-modes.md). 이렇게 하면 한 번의 작업으로 세 개의 스플라인 커넥터를 연결할 수 있습니다.

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

### 출력 미리 보기

대부분의 노드는 이미지의 스플라인을 렌더링하는 <b>미리 보기</b> 출력을 제공하므로 해당 궤적 및 속성이 무엇인지 알 수 있습니다.

<b>미리 보기</b> 그룹의 매개 변수를 사용하여 노드 매개 변수에서 이 미리 보기를 변경할 수 있습니다.

</td>
<td style="border: 0;" valign="top">

![스플라인 노드에서 출력 미리 보기](../../../../../assets/Spline_PreviewOutput.jpg "스플라인 노드에서 출력 미리 보기")

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td width="100.00%" style="border: 0;" valign="top">

### 세그먼트로 렌더링

스플라인은 내재된 해상도가 없는 커브이며, 이는 무한히 크기를 늘리거나 줄일 수 있음을 의미하며, 데이터를 저장하는 데 사용되는 정밀도만 정확하게 나타내는 데 한계가 있습니다.

스플라인을 픽셀로 그리기 위해 도구 세트는 스플라인을 스플라인의 궤적을 따라 그려지는 선 또는 세그먼트로 단순화합니다.

</td>
<td width="33.33%" style="border: 0;" valign="top">

![선분으로 렌더링된 스플라인](../../../../../assets/Spline_Segments.jpg "선분으로 렌더링된 스플라인")

</td>
</tr>
</table>

따라서 이미지에서 스플라인을 그리는 데 사용되는 선분의 수가 너무 낮아 부드러운 곡선을 그릴 수 없거나 너무 높아 대상 해상도에 낭비될 수 있으므로 주의해야 합니다.

이미지에 스플라인을 그리는 노드에는 해당 세그먼트 양을 제어할 수 있는 <b>세그먼트 양</b> 매개 변수가 있습니다. 값이 높을수록 성능이 저하되어 곡선이 더 매끄러워집니다.

### 스플라인에서 이미지 만들기

스플라인의 작성 및 편집이 완료되면 해당 스플라인을 사용하여 나머지 Substance 그래프 노드를 활용할 수 있는 이미지를 생성할 수 있습니다.

그래픽을 생성하는 스플라인을 사용하는 방법에는 크게 세 가지가 있습니다.

* [스플라인 렌더링](../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/spline-tools/spline-render/spline-render.md) 또는 [스플라인 채우기](../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/spline-tools/spline-fill/spline-fill.md) 노드와 함께 해당 모양 및 속성을 사용하여 스플라인을 렌더링합니다.
* [스플라인 매퍼](../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/spline-tools/spline-mapper-grayscale/spline-mapper-grayscale.md), [스플라인 브릿지 매퍼](../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/spline-tools/spline-bridge-mapper-gra/spline-bridge-mapper-grayscale.md) 및 [스플라인 플로우 매퍼](../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/spline-tools/spline-flow-mapper/spline-flow-mapper.md)와 같은 매핑 노드를 사용하여 스플라인을 따라 이미지를 매핑합니다.
* [스플라인 상의 산란](../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/spline-tools/scatter-spline-grayscale/scatter-on-spline-grayscale.md) 노드를 사용하여 스플라인을 따라 패턴 산란
