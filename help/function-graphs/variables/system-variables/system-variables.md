---
helpx_url: "https://helpx.adobe.com/kr/substance-3d-designer/function-graphs/variables/system-variables.html"
breadcrumb-title: ''
description: 고급 워크플로우를 위해 Substance 3D Designer 함수 그래프에서 사용할 수 있는 내장 시스템 변수에 대해 알아봅니다.
helpx_creative_field: ""
helpx_description: Designer > Function graphs > Variables > Built-in variables
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 기본 제공 변수
user-guide-description: ''
user-guide-title: ''
source-git-commit: c002fea6f396f09ccb3218bd290db812d8367dc4
workflow-type: tm+mt
source-wordcount: '549'
ht-degree: 3%

---


# 기본 제공 변수

[Substance 함수 그래프](../../../function-graphs/function-graphs.md)에서 기본 제공 변수를 사용하여 특정 값에 액세스할 수 있습니다. 항상 `$`(달러) 기호로 시작합니다.

일부 변수는 특정 컨텍스트에서만 사용할 수 있습니다.

<b>모든 노드</b>

시스템 변수

| 이름 | 유형 | 용도 |
| --- | --- | --- |
| $size | 실수2 | 현재 노드의 크기를 픽셀 단위로 반환합니다.   *Relative to...* [상속 메서드](../../../compositing-graphs/inheritance-compositing/inheritance-in-substance-compositing-graphs.md)(으)로 설정된 [출력 크기](../../../compositing-graphs/output-size/output-size.md) 매개 변수에 사용되는 경우 *상속된 값*&#x200B;을 반환합니다. |
| $sizelog2 | 실수2 | 위와 같이, 그러나 크기가 2의 제곱 값으로 반환됩니다(예: 2048\*2048 이미지의 경우 `$sizelog2`이(가) 11을 반환합니다).   *Relative to...* [상속 메서드](../../../compositing-graphs/inheritance-compositing/inheritance-in-substance-compositing-graphs.md)(으)로 설정된 [출력 크기](../../../compositing-graphs/output-size/output-size.md) 매개 변수에 사용되는 경우 *상속된 값*&#x200B;을 반환합니다. |
| $pixelratio | 정수 | 현재 노드 픽셀 비율에 해당하는 정수 값을 반환합니다(상속되거나 절대적인 값). 0: 스트레치 1: 정사각형 |
| $tiling | 정수 | 현재 노드 타일링 모드(상속 또는 절대)에 해당하는 정수 값을 반환합니다. 0: 타일링 없음 1: 수평 타일링 2: 수직 타일링 3: H 및 V 타일링 |
| $physicalsize | 실수3 | [그래프의](../../../compositing-graphs/graph-parameters/graph-parameters.md) <b>물리적 크기</b> 속성 값을 반환합니다. |
| $uvtile | 정수2 | UDIM 워크플로우를 사용할 때 이 변수는 U와 V의 현재 udim 인덱스를 반환합니다.   예를 들어, 타일(1003)의 경우 (2, 0), 타일(1118)의 경우 (7, 11)... |

<b>FX-Map</b>

시스템 변수

| 이름 | 유형 | 용도 |
| --- | --- | --- |
| $pos | 실수2 | 패턴의 출생 위치를 반환합니다. 원점(0, 0)은 이미지의 왼쪽 상단 모서리에 있습니다. |
| $깊이 | 부동 | [FX-Map](../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/fx-map/fx-map.md) 노드의 옥타브(레벨) 번호를 반환합니다. 이를 통해 노드는 쿼드트리에서 어떤 레벨을 나타내는지에 따라 그 동작을 수정할 수 있다. |
| $deptthpow2 | 부동 | 위와 같이, 그러나 2의 승수 역수를 옥타브(레벨) 숫자의 거듭제곱으로 올림합니다(예: 1/(2^옥타브)). 몇 가지 일반적인 계산에 유용한 도우미 값입니다. |
| $number | 부동 | 그려진 패턴의 번호를 반환합니다. 각 반복 단계에서 해당 동작을 수정하기 위해 [반복](../../../function-graphs/fxmaps/using-functions-in-fxmaps/iterate-and-number-var/iterate-and-number-variable.md) 노드를 제어하는 동적 함수 그래프에서 이러한 기능에 액세스할 수 있습니다.   `$number`은(는) 1이 아닌 0부터 계산됩니다.   반복 노드 체인을 사용하는 경우 `$number` 변수는 함수 매개 변수가 사용되기 전에 연결된 마지막 반복 노드에서 반복 번호를 반환합니다. 여러 반복 노드에서 반복 번호를 검색하려면 [Set](../../../function-graphs/fxmaps/using-functions-in-fxmaps/using-the-set-sequence/using-the-set-sequence-nodes.md) 노드를 통해 &quot;사용자 지정 변수&quot;를 사용해야 합니다. |

<b>픽셀 프로세서</b>

시스템 변수

| 이름 | 유형 | 용도 |
| --- | --- | --- |
| $pos | 실수2 | 계산되고 있는 픽셀의 위치를 반환합니다. |

<b>전역</b>

시스템 변수

| 이름 | 유형 | 용도 |
| --- | --- | --- |
| $time | 부동 | 이 변수는 Substance 엔진 시작 이후 시간을 초 단위로 반환합니다. 이것은 경과시간에 따라 결과가 변해야 하는 그래프에 사용될 수 있다.  **참고:** 현재 Designer에서 이 값을 변경할 수 있는 방법은 없지만, Substance 엔진을 통합하는 애플리케이션은 이를 활용할 수 있습니다(예: 애니메이션의 경우 [Substance Player](https://helpx.adobe.com/substance-3d-player/home.html), [역동적인 획](https://experienceleague.adobe.com/ko/docs/substance-3d-painter/using/painting/dynamic-strokes/creating-custom-dynamic-strokes)의 경우 [Substance 3D Painter](https://experienceleague.adobe.com/ko/docs/substance-3d-painter/using/home)). |
| $normalformat | 정수 | 현재 환경에서 사용되는 일반 형식(예: DirectX 또는 OpenGL)입니다.  **참고:** 이 변수는 Designer에서 영향을 주지 않으며 Substance 엔진을 통합하는 다른 응용 프로그램에서 사용될 수 있습니다. |
