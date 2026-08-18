---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/function-graphs/fxmaps.html"
breadcrumb-title: ''
description: Substance 3D Designer에서 FXMaps를 사용하여 절차 패턴 생성을 위해 텍스처에 함수 그래프를 적용하는 방법을 알아봅니다.
helpx_creative_field: ""
helpx_description: Designer > Function graphs > FXMaps
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: FXMaps
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '799'
ht-degree: 0%

---


# FXMaps

**FX-Map 노드를 통해 절차 이미지를 만들 수 있습니다**. Substance 기술의 가장 강력한 기능 중 하나입니다.

FX-Map은 마코프 체인(Markov Chain)이라고 하는 특별한 유형의 그래프를 나타낸다. 마코프 체인은 이미지를 반복해서 복제하고 세분화하는 간단한 핵심 프로세스를 나타냅니다. 각 단계에서 이미지를 원하는 대로 회전, 변환 및 혼합할 수 있습니다. 그 결과는 단순한 패턴에서 복잡한 소음까지 무엇이든 될 수 있다. FX-Maps는 Substance 3D Designer과 함께 설치된 많은 샘플 Substance의 기반이 됩니다.

## FX-맵 그래프 만들기

FX-Map 그래프를 보려면 [Substance 그래프](../../compositing-graphs/substance-compositing-graphs.md)에 [FX-Map 노드](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/fx-map/fx-map.md)를 추가한 다음 노드를 마우스 오른쪽 단추로 클릭하고 CMD+E(OS X) 또는 CTRL+E(Windows)를 눌러 그래프를 엽니다. 이 FX-맵 그래프는 그래프 패널의 새 탭에 나타납니다. 탭을 클릭하면 이 그래프와 Substance 그래프 사이를 전환할 수 있습니다.

## FX-Maps란 무엇입니까?

FX-Maps의 가장 일반적인 사용은 줄무늬와 벽돌과 같은 반복적인 패턴과 펄린, 브라운, 가우시안 노이즈와 같은 노이즈입니다. 노이즈는 특히 Dirt, Dust, 콘크리트, 석조 표면, 액체 뿌리기 등과 같은 유기적이고 자연스러운 텍스처를 만드는 데 유용합니다.

FX-맵 그래프는 Substance 그래프와 같은 방식으로 작동하지 않습니다. Substance 그래프에서 각 노드는 독립적이며 전체 그래프에서 해당 위치를 알 수 없으며 이미지 데이터의 출처와 위치를 알 수 없습니다.

다음 장에서 세 개의 FX-맵 그래프 노드를 자세히 살펴보겠지만, 간단히 각 FX-맵 노드는 세 가지 작업 중 하나를 제공합니다.

### 쿼드런트

그러면 그래프에서 이 단계의 이미지가 4개의 사분면으로 분할됩니다. 가장 일반적인 노드 유형입니다. Quadrant 노드 체인은 매우 복잡해 보이는 이미지와 복잡한 패턴을 만들 수 있습니다.

실제로 쿼드런트 노드는 쿼드트리 그래프에서 레벨, 즉 **옥타브**&#x200B;를 나타냅니다. FX-맵 그래프는 트리의 각 레벨을 하나의 Quadrant로 나타내어 이 트리 구조를 숨깁니다. 즉, 하나의 Quadrant 노드를 다른 노드에 연결할 때마다 실제로 완전한 트리 레벨이 만들어집니다.

이 &#39;치트&#39; 기법의 이유는 트리의 모든 수준에서 각 노드를 개별적으로 표현할 필요를 제거하기 위해서입니다. 깊이의 4개의 레이어만 지나면 4 x 4 x 4 노드를 사용해야 하는데, 이는 256개의 개별 노드입니다! 대신 각 Quadrant 노드는 트리에서의 레벨을 &quot;인식&quot;하고 그에 따라 이미지를 생성합니다.

이것은 많은 독자들에게 아마도 그다지 의미가 없을 것이지만, 우리는 곧 이것에 대해 훨씬 더 자세히 알아보겠습니다.

### 반복하기

설정된 반복 횟수만큼 왼쪽 커넥터로 전달된 이미지 위에 오른쪽 커넥터로 전달된 이미지를 반복합니다.

이 노드는 각 반복에서 입력 이미지를 어떤 방식으로 이동 또는 회전하기 위해 하나 이상의 동적 함수 그래프와 함께 가장 자주 사용됩니다.

### 전환

이 경우 두 개의 입력이 필요하며 선택기 설정에서 정의한 대로 둘 중 하나를 서로 전환할 수 있습니다. 반복 노드와 마찬가지로 선택기 설정은 대개 동적 함수에 의해 선택됩니다.

## FX-Maps 시스템 변수

FX-Maps는 시스템 변수를 지원합니다. 이러한 변수는 항상 달러 기호(&quot;$&quot;)로 시작하며 다음과 같습니다.

| 이름 | 특이점 | 데이터 유형 | 용도 |
| --- | --- | --- | --- |
| $time | - | float1 | 이 변수는 Substance 렌더링 엔진이 시작된 이후의 시간을 초 단위로 반환합니다.시간에 따라 애니메이션을 적용해야 하는 Substance에 이상적입니다. (E.g. Substance Player을 비롯한 일부 응용 프로그램에서 $time을 사용하는 Substance을 사용하면 타임라인이 사용자 인터페이스에 표시됩니다. |
| $깊이 | - | float1 | FX-Map 노드의 옥타브(레벨) 번호를 반환합니다. 이를 통해 노드는 쿼드트리에서 어떤 레벨을 나타내는지에 따라 그 동작을 수정할 수 있다. |
| $deptthpow2 | - | float1 | 위와 같이, 그러나 2를 옥타브(레벨) 숫자의 거듭제곱으로 반환합니다. 몇 가지 일반적인 계산에 유용한 도우미 값입니다. |
| $number | 노드만 반복 | float1 | 그려진 패턴의 번호를 반환합니다. 각 반복 단계에서 해당 비헤이비어를 수정하기 위해 반복 노드를 제어하는 동적 함수 그래프에서 액세스할 수 있습니다. $number는 1이 아닌 0부터 계산됩니다. |
| $size | - | float2 | 현재 노드의 크기(픽셀)를 반환합니다. |
| $sizelog2 | - | float2 | 위와 같이, 그러나 크기가 2의 제곱 값으로 반환됩니다(예: 2048\*2048 이미지의 경우 $sizelog2가 11을 반환). |
| $pos | 사분면 노드만 | float2 | 패턴의 출생 위치를 반환합니다. 결과는 항상 0과 1 사이의 값입니다. |
