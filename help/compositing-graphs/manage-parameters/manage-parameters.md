---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/manage-parameters.html"
breadcrumb-title: ''
description: 더 나은 워크플로우 구성을 위해 Substance 합성 그래프에서 매개변수를 관리하고 구성하는 방법을 알아봅니다.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Manage parameters
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 파라미터 관리
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '709'
ht-degree: 3%

---


# 파라미터 관리

매개 변수를 직접 조정하는 것 이외의 다른 방법으로 제어해야 하는 경우 Designer에서는 다음과 같은 몇 가지 유용한 동작을 제공합니다.

* 노드의 모든 매개 변수 값을 [복사하여 붙여넣기](#copy-paste-parameters)
* 나중에 다시 사용할 수 있도록 노드의 값 또는 모든 매개 변수를 [사전 설정 파일](../../compositing-graphs/manage-parameters/parameter-presets/parameter-presets.md)에 저장합니다.
* 노드의 [매개 변수를 노출](../../compositing-graphs/manage-parameters/exposing-a-parameter/exposing-a-parameter.md)하여 액세스 가능하게 만들고 함께 연결합니다
* 다른 매개 변수의 값에 따라 [매개 변수 숨기기 또는 표시](../../compositing-graphs/visible-control-vis/visible-if-control-visibility-of-inputs-outputs-and-parameters.md)
* [Substance 함수 그래프](../../function-graphs/function-graphs.md)를 사용하여 매개 변수 값을 계산하십시오.

## 매개 변수 작업

매개변수 관리에 사용할 수 있는 도구는 다음 위치에서 사용할 수 있습니다.

### 전역 작업

<table>
<tr style="border: 0;">
<td width="100.00%" style="border: 0;" valign="top">

노드의 속성이 속성 도크에 표시되면 다음 섹션 헤더의 &#39;<b>매개 변수 관리</b>&#39; 메뉴를 사용하여 노드 매개 변수를 전체적으로 관리할 수 있습니다.

* [atomic nodes](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/atomic-nodes.md)의 경우: 특정 매개 변수
* [인스턴스 노드](../../compositing-graphs/creating-compositing-gra/graph-instances-sub-gra/graph-instances-sub-graphs.md)의 경우: 인스턴스 매개 변수

</td>
<td width="33.33%" style="border: 0;" valign="top">

![속성의 전역 &#39;매개 변수 관리&#39; 메뉴](../../assets/manage-parameters-menu-global.png "속성의 전역 &#39;매개 변수 관리&#39; 메뉴"){zoomable="yes"}

</td>
</tr>
</table>

이 메뉴의 작업은 해당 섹션에 나열된 매개 변수 *모두*&#x200B;에 영향을 줍니다.

* <b>노출 매개 변수:</b> &#39;일괄 노출 매개 변수&#39; 대화 상자를 엽니다. 노출된 모든 매개 변수에 대해 액션은 새로운 그래프 입력을 만들고 해당 그래프 입력을 사용하여 함수를 자동으로 설정합니다. [이 전용 페이지](../../compositing-graphs/manage-parameters/exposing-a-parameter/exposing-a-parameter.md)에서 매개 변수를 표시하는 방법에 대해 자세히 알아보세요.
* <b>매개 변수 복사:</b> 아래의 [매개 변수 복사 및 붙여넣기](#copy-paste-parameters) 섹션을 참조하세요.
* <b>매개 변수 붙여넣기:</b> 아래의 [매개 변수 복사 및 붙여넣기](../../compositing-graphs/manage-parameters/manage-parameters.md) 섹션을 참조하세요.
* <b>매개 변수를 사전 설정 파일로 저장:</b> [이 전용 페이지](../../compositing-graphs/manage-parameters/parameter-presets/parameter-presets.md)에서 매개 변수 사전 설정에 대해 자세히 알아보세요.
* <b>사전 설정 파일에서 매개 변수 적용:</b> [이 전용 페이지](../../compositing-graphs/manage-parameters/parameter-presets/parameter-presets.md)의 매개 변수 사전 설정에 대해 자세히 알아보세요.
* <b>모두 재설정:</b> 모든 매개 변수를 해당 기본값 및 범위로 재설정합니다. 함수가 매개 변수에 적용된 경우, 해당 함수는 무시됩니다.

>[!NOTE]
>
> 일부 원자성 노드에 대해서는 일부 작업을 사용할 수 없습니다. 아래의 [Atomic nodes limitations](#atomic-nodes-limitations)을(를) 참조하십시오.

### 단일 매개 변수 작업

<table>
<tr style="border: 0;">
<td width="100.00%" style="border: 0;" valign="top">

*단일* 매개 변수를 관리하려면 매개 변수 레이블 반대쪽에 있는 &#39;<b>함수 관리</b>&#39; 메뉴를 사용하십시오.

</td>
<td width="33.33%" style="border: 0;" valign="top">

![속성의 로컬 &#39;매개 변수 관리&#39; 메뉴](../../assets/manage-parameters-menu.png "속성의 로컬 &#39;매개 변수 관리&#39; 메뉴"){zoomable="yes"}

</td>
</tr>
</table>

다음 세 가지 방법으로 해당 매개 변수에 [Substance 함수 그래프](../../function-graphs/the-function-graph/the-function-graph.md)를 적용할 수 있습니다.

* <b>새 그래프 입력으로 표시:</b> 새 그래프 입력을 만들고 해당 그래프 입력을 사용하여 함수를 자동으로 설정합니다. [이 전용 페이지](../../compositing-graphs/manage-parameters/exposing-a-parameter/exposing-a-parameter.md)에서 매개 변수를 표시하는 방법에 대해 자세히 알아보세요.
* <b>빈 함수:</b> 함수를 처음부터 작성하세요.
* <b>상수 값:</b> 매개 변수의 현재 값으로 설정된 [상수 값 노드](../../function-graphs/nodes-reference-for-fun/atomic-function-nodes/constant-nodes/constant-nodes.md)에서 시작하는 함수를 편집합니다.
* <b>재설정:</b> 매개 변수를 기본값 및 범위로 재설정합니다. 함수가 매개 변수에 적용된 경우, 해당 함수는 기각됩니다.

>[!NOTE]
>
> 복사/붙여넣기 및 사전 설정 파일 작업은 모든 매개 변수에 대해 전역 작업이므로 단일 매개 변수에는 사용할 수 없습니다.

### 노드 컨텍스트 메뉴

<table>
<tr style="border: 0;">
<td width="100.00%" style="border: 0;" valign="top">

위에 나열된 *전역* 메뉴의 일부 매개 변수 작업은 노드 컨텍스트 메뉴에서 사용할 수 있습니다. 노드에서 RMB를 클릭하고 &#39;매개 변수 관리&#39;로 이동하여 액세스하십시오.

복사/붙여넣기 작업은 이 메뉴에서 사용할 수 없습니다. 위에서 설명한 대로 노드 속성에서 이러한 속성을 찾을 수 있습니다.

이 메뉴에는 원자성 노드에 대해 아래 나열된 것과 동일한 제한 사항이 적용됩니다.

</td>
<td width="50.00%" style="border: 0;" valign="top">

노드 컨텍스트 메뉴의 ![&#39;매개 변수 관리&#39; 메뉴](../../assets/manage-parameters-node-menu.png " 노드 컨텍스트 메뉴의 &#39;매개 변수 관리&#39; 메뉴"){zoomable="yes"}

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

## 매개 변수 복사 및 붙여넣기

소스 노드에 대한 모든 매개변수 값을 복사하여 대상 노드에 붙여넣을 수 있습니다. 소스 및 대상 노드의 매개 변수는 <b>해당 식별자와 유형을 모두 기준으로 일치</b>됩니다.

예를 들어, 식별자가 &#39;scale&#39;이고 형식이 &#39;Float&#39;인 &#39;Scale&#39; 매개 변수는 해당 식별자가 &#39;scale&#39;이기도 하고 해당 형식이 &#39;Float&#39;이기도 한 경우 다른 매개 변수 &#39;Shape Scale&#39;에 복사하여 붙여넣을 수 있습니다.

이 기능은 [매개 변수 사전 설정 파일](../../compositing-graphs/manage-parameters/parameter-presets/parameter-presets.md)을 사용하는 것과 같은 방식으로 작동합니다. 실제로 클립보드에 복사된 데이터는 SBSPRS 사전 설정 파일에 저장된 데이터와 동일하며, 텍스트 편집기에 붙여 검토 및 편집할 수 있습니다.

</td>
<td style="border: 0;" valign="top">

![매개 변수 복사 및 붙여넣기](../../assets/copy-paste-parameters.gif "매개 변수 복사 및 붙여넣기"){zoomable="yes"}

</td>
</tr>
</table>

## Atomic node 제한 사항

특정 구현 및 컨트롤로 인해 일부 [atomic nodes](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/atomic-nodes.md)에서 일부 기능을 사용할 수 없습니다.

이 작업...

* [매개 변수 복사/붙여넣기](#copy-paste-parameters)
* [사전 설정 파일 저장/적용](../../compositing-graphs/manage-parameters/parameter-presets/parameter-presets.md)

...이러한 atomic node에는 사용할 수 없습니다.

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

[비트맵](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/bitmap/bitmap.md)

[곡선](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/curve/curve.md)

[거리](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/distance/distance.md)

[FX-Map](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/fx-map/fx-map.md)

[그래디언트(동적)](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/gradient-dynamic/gradient-dynamic.md)

</td>
<td style="border: 0;" valign="top">

[그레이디언트 맵](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/gradient-map/gradient-map.md)

[색상 입력](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/input/input.md)

[회색 음영 입력](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/input/input.md)

[값 입력](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/input/input.md)

[출력](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/output/output.md)

</td>
<td style="border: 0;" valign="top">

[픽셀 프로세서](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/pixel-processor/pixel-processor.md)

[SVG](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/svg/svg.md)

[텍스트](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/text/text.md)

[균일 색상](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/uniform-color/uniform-color.md)

[값 프로세서](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/value-processor/value-processor.md)

</td>
<td style="border: 0;" valign="top">



</td>
</tr>
</table>
