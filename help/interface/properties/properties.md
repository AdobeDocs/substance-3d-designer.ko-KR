---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/interface/properties.html"
breadcrumb-title: ''
description: Substance 3D Designer의 [속성] 패널을 사용하여 노드 속성 및 그래프 매개 변수를 보고 편집합니다.
helpx_creative_field: ""
helpx_description: Designer > Interface > Properties
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 속성
user-guide-description: ''
user-guide-title: ''
source-git-commit: 99e410384cec6569f613bb771db26585887704d8
workflow-type: tm+mt
source-wordcount: '444'
ht-degree: 0%

---


# 속성

이 페이지에는 Substance 3D Designer의 <b>속성 </b> 패널, 레이아웃, 다양한 롤아웃 및 범주와 매개 변수가 표시됩니다. [Substance 그래프](../../compositing-graphs/substance-compositing-graphs.md)의 속성에 중점을 두고 있습니다. [함수 그래프](../../function-graphs/function-graphs.md) 및 [FX-맵 그래프](../../function-graphs/fxmaps/fxmaps.md)에는 레이아웃이 더 단순합니다.

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

## 개요

<b>속성 </b>패널은 [그래프 보기](../../interface/the-graph-view/the-graph-view.md) 및 [탐색기](../the-explorer-window/the-explorer-window.md) 창에서 선택한 내용에 따라 변경되는 상황에 맞는 패널입니다.

</td>
<td style="border: 0;" valign="top">

![속성 도킹](../../assets/image2020-11-9-13-49-48.png "속성 도킹")

</td>
</tr>
</table>

이 기능을 사용하면 선택한 노드 및 리소스의 속성을 [그래프 보기](../../interface/the-graph-view/the-graph-view.md)와 함께 변경할 수 있습니다. 이 기능은 Designer에서 두 번째로 많이 사용되는 UI 패널일 것입니다.

속성 패널은 선택 사항에 따라 몇 가지 다른 롤아웃으로 분할됩니다. 예를 들어, 다음과 같습니다.

* 노드에 대한 <b>기본 매개 변수</b> 및 <b>입력-</b> 또는 <b>특정 매개 변수</b>
* 대부분의 노드 및 패키지에 대한 <b>특성</b> 및 <b>메타데이터</b>

Substance 에코시스템의 주요 기능인 [매개 변수 노출](../../compositing-graphs/manage-parameters/exposing-a-parameter/exposing-a-parameter.md)은 속성 패널을 통해 수행됩니다.

>[!NOTE]
>
> 대부분의 숫자 필드는 *기본 수식*&#x200B;을 입력으로 지원합니다(예: `17+3.5`, `7/3`, `(4+2)*3`). 수식을 확인하려면 *Enter*&#x200B;을(를) 누르면 결과가 필드에 입력됩니다. 공식이 유효하지 않으면 필드가 이전 값으로 되돌아갑니다.\
> [노출 매개 변수](../../compositing-graphs/manage-parameters/exposing-a-parameter/exposing-a-parameter.md) 대화 상자와 같은 응용 프로그램의 다른 부분에 있는 일부 숫자 필드도 이 기능을 지원합니다.

## 노드 및 Substance 그래프

[노드](https://helpx.adobe.com/substance-3d/unlisted/documentation/sddoc/nodes-reference-129368078.html)와 [Substance 그래프](../../compositing-graphs/substance-compositing-graphs.md)에 속성 범주가 약간 겹치며 기능이 비슷합니다.

<b>기본 매개 변수</b> 및 <b>특성</b>은 노드와 그래프 간에 동일합니다.

노드는 <b>특정 매개 변수</b> 또는<b> 인스턴스 매개 변수</b>(해당 매개 변수가 [Atomic nodes](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/atomic-nodes.md) 또는 [인스턴스](../../compositing-graphs/creating-compositing-gra/graph-instances-sub-gra/graph-instances-sub-graphs.md)인지에 따라 다름)와 [Substance 그래프의 값](https://helpx.adobe.com/substance-3d/unlisted/documentation/sddoc/values-in-substance-3d-graphs-180192235.html)을 사용하기 위한 <b>입력 값</b>을 제공합니다.

[입력](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/input/input.md)과 [출력](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/output/output.md)원자성 노드는 가시성을 위해 <b>통합 특성</b> 및 <b>조건</b>을 사용하므로 예외입니다. 이러한 두 속성 집합은 [입력] 및 [출력] 아래의 [그래프] 속성에서 가운데에 액세스할 수도 있습니다.

그래프에는 몇 가지 추가 범주가 있습니다. <b>입력 매개 변수</b>에는 [노출된 매개 변수](../../compositing-graphs/manage-parameters/exposing-a-parameter/exposing-a-parameter.md), <b>입력</b> 및 <b>출력</b>에는 입력 및 출력 노드의 모든 속성이 나열됩니다. [전용 페이지에서 자세히 설명된 모든 그래프 속성을 찾을 수 있습니다.](../../compositing-graphs/graph-parameters/graph-parameters.md)

## 리소스 및 패키지

속성 패널도 [탐색기 창](https://helpx.adobe.com/substance-3d/unlisted/documentation/sddoc/the-explorer-129368147.html)에서 선택 변경 내용에 응답합니다. 빈 영역을 두 번 클릭하는 대신 그래프를 선택하는 다른 방법으로 사용할 수 있으며, 패키지 및 [리소스](../../resources/resources.md)속성을 변경할 수도 있습니다.

패키지에는 **정보**, **특성** 및 **메타데이터** 섹션이 있습니다. [패키지 메타데이터는 전용 페이지에 설명되어 있습니다.](../../package-metadata/package-metadata.md)

리소스에 해당 유형과 관련된 속성이 있습니다. [전용 페이지에 자세히](../../resources/resources.md).
