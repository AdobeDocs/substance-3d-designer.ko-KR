---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/warnings-in-substance-compositing-graphs.html"
breadcrumb-title: ''
description: Substance 합성 그래프의 경고를 이해하고 일반적인 문제 및 오류를 해결하는 방법을 알아보십시오.
helpx_creative_field: ""
helpx_description: Designer > Substance graphs > Warnings in Substance graphs
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Substance 그래프의 경고
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '700'
ht-degree: 1%

---


# Substance 그래프의 경고

이 페이지에는 Substance 3D Designer에서 [Substance 그래프](../../compositing-graphs/substance-compositing-graphs.md)로 트리거될 수 있는 경고 및 오류 메시지가 나열되며 각각에 대한 일반적인 문제 해결 단계를 제공합니다.

[탐색기](../../interface/the-explorer-window/the-explorer-window.md) 패널의 그래프 리소스에 대한 경고 아이콘의 도구 설명뿐만 아니라 그래프가 로드된 경우 [그래프 보기](../../interface/the-graph-view/the-graph-view.md)의 왼쪽 아래 모서리에 경고가 표시됩니다.

## ![(오류)](warnings-in-substance-compositing-graphs.resources/error.svg) 출력 노드가 정의되지 않았습니다.

그래프에 [출력](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/output/output.md) 노드가 없습니다.

**![(틱)](warnings-in-substance-compositing-graphs.resources/check.svg) 솔루션**

그래프에 하나 이상의 [출력](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/output/output.md) 노드를 추가하고 스트림에 있는 마지막 노드의 출력을 그래프에 연결합니다.

>[!NOTE]
>
> [새 그래프](../creating-compositing-gra/creating-a-substance-compositing-graph.md) 대화 상자를 통해 사용할 수 있는 그래프 템플릿에는 사용할 준비가 된 사전 설정 출력 노드가 있습니다.

![&#39;출력 노드가 정의되지 않음&#39; 경고 수정](warnings-in-substance-compositing-graphs.resources/warnings-in-substance-compositing-graphs-01.gif "&#39;출력 노드가 정의되지 않음&#39; 경고 수정"){width="512px"}

### ![(오류)](warnings-in-substance-compositing-graphs.resources/error.svg) *[x]* 매개 변수의 함수에 몇 가지 경고가 있습니다.

지정한 노드의 지정한 매개 변수에 적용된 [함수 그래프](../../function-graphs/function-graphs.md)에 하나 이상의 경고가 있습니다.\
노드 매개 변수는 노드 레이블 뒤에 있는 Node[Parameter] 템플릿 뒤에 대괄호 사이에 지정됩니다.

E.g. 균일 색상[출력 색상], 픽셀 프로세서[픽셀당 함수]

**![(틱)](warnings-in-substance-compositing-graphs.resources/check.svg) 솔루션**

[그래프 보기](../../interface/the-graph-view/the-graph-view.md)에서 레이블 및 경고 배지로 경고를 보내는 노드를 찾은 다음 해당 노드를 선택하여 [속성](../../interface/properties/properties.md) 패널에 해당 속성을 표시합니다. 경고를 발생시키는 매개 변수를 찾아 **함수 편집** 단추를 클릭하여 해당 함수를 엽니다.

그런 다음 그래프 보기의 왼쪽 하단에 나열된 경고를 평가하고 문제를 해결합니다. 함수 그래프에서 보고된 경고를 해결하려면 [함수 그래프의 경고](../../function-graphs/warnings-function-graphs/warnings-in-function-graphs.md) 페이지를 참조할 수 있습니다.

![Fix &#39;Parameter function has some warnings&#39; warning](warnings-in-substance-compositing-graphs.resources/warnings-in-substance-compositing-graphs-02.gif "Fix &#39;Parameter function has some warnings&#39; warning")

### ![(오류)](warnings-in-substance-compositing-graphs.resources/error.svg) 참조된 데이터에 몇 가지 경고가 있습니다

노드에서 참조하는 리소스에 하나 이상의 경고가 있습니다. 다음은 리소스를 참조하는 몇 가지 노드입니다.

* [그래프 인스턴스](../../compositing-graphs/creating-compositing-gra/graph-instances-sub-gra/graph-instances-sub-graphs.md) 노드가 그래프를 참조합니다.
* [비트맵](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/bitmap/bitmap.md) 노드가 [비트맵 리소스](../../resources/bitmap-resource/bitmap-resource.md)를 참조합니다.
* [SVG](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/svg/svg.md) 노드가 [SVG 리소스](../../resources/vector-graphics-svg-res/vector-graphics-svg-resource.md)를 참조합니다.
* [텍스트](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/text/text.md) 노드가 [글꼴 리소스](../../resources/font-resource/font-resource.md)를 참조합니다.

**![(틱)](warnings-in-substance-compositing-graphs.resources/check.svg) 솔루션**

[탐색기](../../interface/the-explorer-window/the-explorer-window.md) 패널에서 참조된 리소스를 찾고 리소스에서 발생한 모든 경고를 해결합니다.

* 그래프의 경우 이 페이지의 다른 항목을 참조하십시오
* 다른 유형의 리소스는 [종속성 경고](../../resources/warnings-from-dep/warnings-from-dependencies.md) 페이지를 참조하십시오

![Fix &#39;Referenced data has some warnings&#39; warning](warnings-in-substance-compositing-graphs.resources/warnings-in-substance-compositing-graphs-03.gif "Fix &#39;Referenced data has some warnings&#39; warning")

### ![(오류)](warnings-in-substance-compositing-graphs.resources/error.svg) 참조 리소스를 찾을 수 없습니다.

노드에서 참조하는 리소스를 [Substance 3D](https://www.adobe.com/products/substance3d/3d-augmented-reality.html) 파일(SBS)에 저장된 경로에서 찾을 수 없습니다. 다음은 리소스를 참조하는 몇 가지 노드입니다.

* [그래프 인스턴스](../../compositing-graphs/creating-compositing-gra/graph-instances-sub-gra/graph-instances-sub-graphs.md) 노드가 그래프를 참조합니다.
* [비트맵](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/bitmap/bitmap.md) 노드가 [비트맵 리소스](../../resources/bitmap-resource/bitmap-resource.md)를 참조합니다.
* [SVG](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/svg/svg.md) 노드가 [SVG 리소스](../../resources/vector-graphics-svg-res/vector-graphics-svg-resource.md)를 참조합니다.
* [텍스트](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/text/text.md) 노드가 [글꼴 리소스](../../resources/font-resource/font-resource.md)를 참조합니다.

**![(틱)](warnings-in-substance-compositing-graphs.resources/check.svg) 솔루션**

[그래프 인스턴스](../../compositing-graphs/creating-compositing-gra/graph-instances-sub-gra/graph-instances-sub-graphs.md) 노드의 경우

원본 그래프가 **Package** 특성에 저장된 경로에 있는 패키지에 있는지 확인하십시오.\
그렇지 않으면 인스턴스 노드를 삭제하고 유효한 패키지를 참조하는 인스턴스 노드로 대체합니다. 또는 인스턴스 노드에서 참조하는 패키지와 그래프를 다시 만든 다음 [탐색기](../../interface/the-explorer-window/the-explorer-window.md) 패널에서 RMB를 클릭하고 컨텍스트 메뉴에서 **다시 로드** 옵션을 선택하여 호스트 패키지를 다시 로드할 수 있습니다.

[비트맵](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/bitmap/bitmap.md), [SVG](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/svg/svg.md) 또는 [텍스트](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/text/text.md) 노드의 경우

참조된 리소스는 [탐색기] 패널에서 찾아서 **파일 경로** 특성에 저장된 위치에 있는지 확인합니다.\
그렇지 않으면 탐색기에서 리소스 항목에 대해 RMB를 클릭하고 컨텍스트 메뉴에서 **재배치...** 옵션을 선택하여 해당 리소스에 대해 유효한 새 대상 파일을 설정합니다.

![&#39;참조 리소스를 찾을 수 없습니다&#39; 경고 수정](warnings-in-substance-compositing-graphs.resources/warnings-in-substance-compositing-graphs-04.gif "&#39;참조 리소스를 찾을 수 없습니다&#39; 경고 수정")

### ![(오류)](warnings-in-substance-compositing-graphs.resources/error.svg) 텍스트 노드에서 잘못된 글꼴을 사용함

[텍스트](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/text/text.md) 노드가 올바르게 로드하거나 구문 분석할 수 없는 글꼴을 참조합니다.

<b>![(틱)](warnings-in-substance-compositing-graphs.resources/check.svg) 솔루션</b>

[Text](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/text/text.md) 노드를 선택하고 해당 <b>Font</b> 속성 값을 기록해 두십시오. 시스템에서 해당 글꼴의 소스 파일을 찾아 *정상*&#x200B;인지 확인합니다(예: 텍스트 편집기와 같은 다른 응용 프로그램에서 사용). 필요한 경우 건강한 글꼴 파일로 글꼴을 대체하거나 텍스트 노드를 다른 글꼴로 전환합니다.
