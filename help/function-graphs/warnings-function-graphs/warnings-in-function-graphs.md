---
helpx_url: "https://helpx.adobe.com/kr/substance-3d-designer/function-graphs/warnings-in-function-graphs.html"
breadcrumb-title: ''
description: Substance 3D Designer 함수 그래프의 경고를 이해하고 일반적인 문제를 해결하는 방법을 알아보십시오.
helpx_creative_field: ""
helpx_description: Designer > Function graphs > Warnings in function graphs
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 함수 그래프의 경고
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '450'
ht-degree: 0%

---


# 함수 그래프의 경고

이 페이지에는 Substance 3D Designer에서 [함수 그래프](../../function-graphs/function-graphs.md)로 트리거될 수 있는 경고 및 오류 메시지가 나열되어 있으며 각각에 대한 일반적인 문제 해결 단계를 제공합니다.

[탐색기](../../interface/the-explorer-window/the-explorer-window.md) 패널의 그래프 리소스에 대한 경고 아이콘의 도구 설명뿐만 아니라 그래프가 로드된 경우 [그래프 보기](../../interface/the-graph-view/the-graph-view.md)의 왼쪽 아래 모서리에 경고가 표시됩니다.\
함수가 [Substance 그래프](../../compositing-graphs/substance-compositing-graphs.md)의 *매개 변수*&#x200B;에 적용되면 모든 경고로 인해 &quot;*해당 매개 변수에 대해 [x] 매개 변수의 함수에 일부 오류*&quot;가 발생합니다.

## ![(오류)](warnings-in-function-graphs.resources/error.svg) 출력 노드가 정의되지 않았습니다.

함수에 정의된 출력 노드가 없습니다.

<table>
<tr style="border: 0;">
<td width="58.30%" style="border: 0;" valign="top">

**![(틱)](warnings-in-function-graphs.resources/check.svg) 솔루션**

그래프에서 이 함수의 예상 유형과 일치하는 유형의 값을 출력하는 노드를 선택한 다음 RMB를 클릭하고 컨텍스트 메뉴에서 **출력 노드로 설정** 옵션을 선택합니다.\
함수 그래프의 출력 노드에 *주황색* 색상이 지정됩니다.

>[!NOTE]
>
> 함수에 원하는 출력 값 형식이 있는 경우 [그래프 보기](../../interface/the-graph-view/the-graph-view.md)의 왼쪽 아래 모서리에 있는 메모를 통해 해당 형식을 알 수 있습니다.

</td>
<td width="41.60%" style="border: 0;" valign="top">

![](warnings-in-function-graphs.resources/warnings-in-function-graphs-01.gif)

</td>
</tr>
</table>

### ![(오류)](warnings-in-function-graphs.resources/error.svg) 현재 출력 노드가 *x* 형식의 값을 반환합니다.

함수의 출력 노드는 해당 함수의 예상 출력 값 형식과 일치하지 않는 값을 반환합니다.

<table>
<tr style="border: 0;">
<td width="58.30%" style="border: 0;" valign="top">

**![(틱)](warnings-in-function-graphs.resources/check.svg) 솔루션**

그래프에서 이 함수의 예상 유형과 일치하는 유형의 값을 출력하는 노드를 선택한 다음 RMB를 클릭하고 컨텍스트 메뉴에서 **출력 노드로 설정** 옵션을 선택합니다.\
함수 그래프의 출력 노드에 *주황색* 색상이 지정됩니다.

>[!NOTE]
>
> 함수에 원하는 출력 값 형식이 있는 경우 [그래프 보기](../../interface/the-graph-view/the-graph-view.md)의 왼쪽 아래 모서리에 있는 메모를 통해 해당 형식을 알 수 있습니다.

</td>
<td width="41.60%" style="border: 0;" valign="top">

![](warnings-in-function-graphs.resources/warnings-in-function-graphs-02.gif)

</td>
</tr>
</table>

### ![(오류)](warnings-in-function-graphs.resources/error.svg) 일부 Get 노드에 변수 이름이 없습니다.

하나 이상의 [Get](../../function-graphs/nodes-reference-for-fun/atomic-function-nodes/get-nodes/get-nodes.md) 노드에 <b>Get...</b> 속성이 비어 있으므로 변수를 참조하지 않습니다.

<table>
<tr style="border: 0;">
<td width="58.30%" style="border: 0;" valign="top">

**![(틱)](warnings-in-function-graphs.resources/check.svg) 솔루션**

함수 범위&#x200B;*에서 사용할 수 있는*&#x200B;변수의 이름과 일치하는 문자열을 Get 노드의 **Get...** 속성에 입력하여 이 경고를 발생시킵니다.

>[!NOTE]
>
> 입력 문자열은 *노드에 표시*&#x200B;되므로 값이 빈 노드를 쉽게 찾을 수 있습니다.

</td>
<td width="41.60%" style="border: 0;" valign="top">

![](warnings-in-function-graphs.resources/warnings-in-function-graphs-03.gif)

</td>
</tr>
</table>

### ![(오류)](warnings-in-function-graphs.resources/error.svg) 일부 집합 노드에 변수 이름이 없습니다.

하나 이상의 [Set](../../function-graphs/fxmaps/using-functions-in-fxmaps/using-the-set-sequence/using-the-set-sequence-nodes.md) 노드에 해당 **Set** 속성이 비어 있으므로 변수를 참조하지 않습니다.

<table>
<tr style="border: 0;">
<td width="58.30%" style="border: 0;" valign="top">

**![(틱)](warnings-in-function-graphs.resources/check.svg) 솔루션**

이 경고를 발생시키는 Set 노드의 **Set** 속성에 문자열을 입력합니다.

>[!NOTE]
>
> 입력 문자열은 *노드에 표시*&#x200B;되므로 값이 빈 노드를 쉽게 찾을 수 있습니다.

>[!NOTE]
>
> 문자열이 함수의 범위에서 사용할 수 있는 모든 변수와 *일치하지* 않으면 해당 범위 내에서 *새 변수가 만들어지고* 문자열 이름을 따서 명명됩니다.

</td>
<td width="41.60%" style="border: 0;" valign="top">

![](warnings-in-function-graphs.resources/warnings-in-function-graphs-04.gif)

</td>
</tr>
</table>
