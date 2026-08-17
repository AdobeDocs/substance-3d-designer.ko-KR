---
helpx_url: "https://helpx.adobe.com/kr/substance-3d-designer/function-graphs/nodes-reference-for-function-graphs/atomic-function-nodes/control-nodes.html"
breadcrumb-title: ''
description: Substance 3D Designer 함수 그래프의 제어 노드에 액세스하여 플로우 및 실행 논리를 제어합니다.
helpx_creative_field: ""
helpx_description: Designer > Function graphs > Nodes reference for function graphs > Control
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 제어
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '558'
ht-degree: 1%

---


# 제어 노드

이 페이지에서는 *실행 흐름*&#x200B;을 제어하는 [함수 그래프](../../../../function-graphs/the-function-graph/the-function-graph.md)의 노드를 설명합니다.

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![If...Else 노드](https://helpx.adobe.com/content/dam/substance-3d-designer/function-graphs/nodes/atomic-function-nodes/control/IfElse_Node.jpg "If...Else 노드")

</td>
<td width="100.00%" style="border: 0;" valign="top">

## If...Else

프로그래밍 언어와 마찬가지로 If... Else 노드에서는 미리 정의된 조건에 따라 결과를 필터링할 수 있습니다.

</td>
</tr>
</table>

이 노드는 [개의 논리 노드](../../../../function-graphs/nodes-reference-for-fun/atomic-function-nodes/logical-nodes/logical-nodes.md) 및 [비교 노드](../../../../function-graphs/nodes-reference-for-fun/atomic-function-nodes/comparison-nodes/comparison-nodes.md)와 함께 사용되므로 확인할 조건을 작성할 수 있습니다.

+++입력 커넥터
<b>조건</b> *부울*\
노드의 출력을 제어하는 조건입니다.

<b>If</b> *변수 형식*&#x200B;노드에서 <b>조건</b>이(가) *True*&#x200B;인 경우 출력하는 값입니다.

<b>Else</b> *가변 유형*&#x200B;노드에서 출력하는 값(<b>조건</b>이 *거짓*&#x200B;인 경우).

+++

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![시퀀스 노드](https://helpx.adobe.com/content/dam/substance-3d-designer/function-graphs/nodes/atomic-function-nodes/control/Sequence_Node.jpg "시퀀스 노드")

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 시퀀스

그래프의 일부가 다른 부분보다 먼저 계산되도록 합니다.

</td>
</tr>
</table>

이는 변수가 생성, 읽기 및 업데이트되는 상태를 제어하는 데 매우 중요합니다.

이 설명서의 [시퀀스 노드 설정/사용](../../../../function-graphs/fxmaps/using-functions-in-fxmaps/using-the-set-sequence/using-the-set-sequence-nodes.md) 페이지에서 시퀀스 노드에 대해 자세히 알아볼 수 있습니다.

+++입력 커넥터
<b>내부</b> *변수 형식*\
먼저 계산되어야 하는 그래프의 부분입니다

<b>마지막</b> *변수 형식*\
마지막으로 계산되어야 하는 그래프의 부분입니다.

+++

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![전체 루프 노드](https://helpx.adobe.com/content/dam/substance-3d-designer/function-graphs/nodes/atomic-function-nodes/control/WhileLoop-Node.jpg "전체 루프 노드")

</td>
<td width="100.00%" style="border: 0;" valign="top">

## While 루프

<b>Init</b> 분기를 한 번 실행한 다음 <b>종료 코드</b>를 반복합니다. <b>종료 코드</b>까지 <b>루프 본문</b>이 분기됩니다. branch가 *True*&#x200B;을(를) 반환합니다.

루프가 완료되면 노드는 <b>루프 본문</b>의 마지막 반복 결과를 출력합니다.

</td>
</tr>
</table>

루프에 암시적 최대 반복 횟수가 있습니다. 이 최대 반복 횟수를 -1로 설정하면 사용하지 않도록 설정할 수 있습니다.

변수는 이터레이션 간에 해당 값을 유지하며 종료 조건(종료 조건)에서 액세스할 수 있습니다.\
즉, 반복할 때마다 인덱스 값에 추가하고 종료 조건에서 해당 값을 확인하여 필요한 루프 수를 제어할 수 있습니다.

>[!IMPORTANT]
>
> <b>종료 코드</b>에 연결된 노드 그리고 <b>루프 본문</b> 분기는 그래프의 다른 분기에 연결할 수 없습니다.

+++입력 커넥터
<b>초기화.</b> *변수 형식*\
첫 번째 반복 전에 계산되는 그래프의 부분(즉, 루프의 시작 부분)입니다.

<b>콘드를 종료합니다.</b> *부울*\
루프가 중지되려면 true여야 하는 조건입니다. 각 반복에 대해 다시 계산됩니다.\
*참고:* 최대 반복 횟수는 여전히 <b>최대 반복 횟수</b> 매개 변수로 제한됩니다.

<b>루프 본문</b> *변수 형식*\
루프에서 이점을 얻는 그래프입니다. 각 반복에 대해 다시 계산됩니다.

+++

+++매개변수
<b>최대. 반복</b> *정수*\
노드에서 수행한 최대 반복 수입니다.\
다음 조건 중 하나가 먼저 충족되면 노드가 반복을 중지합니다. 이 최대 수에 도달하거나 종료 조건이 true 가 됩니다.\
이 최대값은 값을 *-1*(으)로 설정하여 사용하지 않도록 설정할 수 있습니다. 이 시점에서 종료 조건만 이터레이션을 중지할 수 있습니다.

&#39;최대&#39;를 설정하는 중입니다. iteration&#39; to -1을 사용하면 추적 및 업데이트를 유지하는 카운터가 하나 줄어들기 때문에 작은 루프에서 성능이 향상됩니다.

그러나 Designer이 응답하지 않을 수 있는 <b>무한 루프</b>를 만들 수 있으므로 노드가 어떻게 구성되는지 유의하십시오.

+++

While Loop 노드에 대한 다음 튜토리얼을 참조하십시오.
