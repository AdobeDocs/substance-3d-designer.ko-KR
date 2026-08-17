---
helpx_url: "https://helpx.adobe.com/kr/substance-3d-designer/substance-compositing-graphs/substance-compositing-graph-key-concepts.html"
breadcrumb-title: ''
description: 노드, 연결 및 작업 과정 기초를 포함하여 Substance 합성 그래프의 주요 개념에 대해 알아보십시오.
helpx_creative_field: ""
helpx_description: Designer > Substance graphs > Substance graph key concepts
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Substance 그래프 주요 개념
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '883'
ht-degree: 1%

---


# Substance 그래프 주요 개념

이 페이지에는 Substance 3D Designer에서 Substance 그래프를 사용하여 작업하기 위해 이해해야 할 중요한 개념이 나열되어 있습니다.

## 하위 그래프/게시

[그래프 게시](https://helpx.adobe.com/kr/substance-3d/unlisted/documentation/sddoc/publishing-sbsar-file-200574380.html) 또는 하위 그래프 만들기 작업은 두 가지 매우 유사하고 추상적인 개념입니다. 즉, 모든 그래프 또는 노드 네트워크를 함께 &quot;패키지화&quot;하여 재사용 가능한 독립형 리소스로 변환할 수 있습니다. [하위 그래프](../../compositing-graphs/creating-compositing-gra/graph-instances-sub-gra/graph-instances-sub-graphs.md)를 만드는 작업은 대부분 응용 프로그램 내에서 이루어지며, 특정 콘텐츠를 효율적이고 스마트한 작업 과정에서 재사용할 수 있도록 합니다. 이렇게 하면 노드 집합이 반복해서 중복되지 않습니다. 게시에는 [Substance 3D 에셋(SBSAR)](https://helpx.adobe.com/kr/substance-3d/unlisted/documentation/sddoc/publishing-sbsar-file-200574380.html) 형식으로 내보내는 추가 단계가 포함되어 있어 언리얼 엔진용 재질을 만드는 경우처럼 응용 프로그램 외부에서 노드 네트워크 그래프를 사용할 수 있습니다.

입력, 출력 및 노출 매개 변수는 그래프가 하위 그래프 또는 게시된 Substance 3D 에셋으로 사용되면 그래프와 계속 상호 작용할 수 있는 유일한 방법이므로 이 개념에 매우 중요합니다. 그 이유는 다음과 같습니다.

* 출력이 없으면 그래프가 <b>아무것도 생성하지 않고,</b> 데이터가 전혀 생성되지 않습니다.
* 노출된 매개 변수가 없다는 것은 그래프 <b>을(를) 사용자 지정할 수 없음을 의미합니다</b>. 효과의 강도, 혼합되는 이미지의 불투명도, 특정 영역의 색상 등을 설정할 수는 없습니다.
* 입력이 없으면 효과를 생성하기 위한 구운 메시 맵, 흐림 효과를 수행하기 위한 입력 이미지 또는 이미지의 특정 영역을 격리하기 위한 사용자 정의 마스크 등</b>을(를) 사용하여 <b>개의 자체 이미지 데이터로 그래프의 결과를 사용자 정의할 수 없는 경우가 있습니다.

## 입력 및 출력

[출력](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/output/output.md)은 단일 2D 결과를 생성하는 노드입니다. 그래프의 끝점이자 종착점입니다. 완성된 결과입니다. 출력에 연결된 데이터만 Designer 외부로 내보내거나 다른 그래프에서 사용할 수 있습니다.

출력에 대해 알아야 할 몇 가지 사항은 다음과 같습니다.

* 원하는 만큼 많은 출력을 가질 수 있지만 <b>하나 이상의 출력</b>이 있어야 합니다.
* 출력은 폭 또는 높이가 최대 8,192px인 <b>모든 해상도</b>일 수 있으며, 색상 또는 회색 음영<b>일 수 있고</b>일 수 있으며 지원되는 모든 파일 유형으로 내보낼 수 있습니다.
* 출력은 <b>고유하게 이름 지정</b>될 수 있으며 이를 식별하도록 지정해야 합니다. 내보내는 데 도움이 됩니다.
* 노드의 오른쪽에 있는 모든 커넥터는 실제로 출력입니다(&quot;자세한 정보는 하위 그래프 참조).

[입력](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/input/input.md)은(는) 출력과 비슷합니다. 사용자 또는 다른 사용자가 자신의 데이터를 연결할 수 있는 빈 열린 슬롯입니다. 이 기능을 사용하면 입력 이미지를 수정하는 필터(예: 흐림 효과 또는 대비 조정)와 같이 사용자가 정의한 외부 이미지 데이터에 그래프를 생성할 수 있습니다.

다음은 입력에 대해 알아야 할 몇 가지 사항입니다.

* 입력은 완전히 <b>선택 사항</b>이므로 필요한 경우에만 추가해야 합니다. 최소 또는 최대 금액이 없습니다.
* 입력은 회색 음영이나 색상인 경우뿐만 아니라 사용자가 정의하는 해상도 설정(일반적으로 그래프에 연결됨)을 가집니다. 연결된 모든 항목이 이와 일치하도록 변환됩니다.
* 하드 드라이브의 비트맵 파일, 기타 그래프, Painter 또는 Alchemist의 레이어 등을 입력할 수 있습니다.
* 모든 노드의 왼쪽에 있는 모든 커넥터는 입력입니다(&quot;자세한 정보는 하위 그래프 참조).

## 상속

이미지 및 값이 노드에서 다른 이미지로 전달되면 이러한 이미지 중 일부 *특성*(즉, <b>기본 매개 변수</b>)은 그래프 전체에서 해상도, 정밀도(즉, 비트 심도), 타일링 및 임의 시드와 같이 *전파*&#x200B;됩니다.

이 전파는 각 노드가 이러한 특성에 적용되는 [상속 메서드](../../compositing-graphs/inheritance-compositing/inheritance-in-substance-compositing-graphs.md)에 의해 정의됩니다. 실제로 노드는 다른 노드 또는 해당 노드가 있는 그래프에서 *특성을 상속*&#x200B;할 수 있습니다.\
상속 메서드는 다음과 같습니다.

* *부모에 대한 상대*
* *입력 기준*
* *절대* - 예: 상속 없음

상속은 추상적이고 관리하기 까다로울 수 있으므로 자세히 설명하는 [전용 페이지](../../compositing-graphs/inheritance-compositing/inheritance-in-substance-compositing-graphs.md)를 살펴보는 것이 좋습니다.

## 매개 변수 노출

매개변수를 표시하는 것은 매우 심도 있는 개념이지만 그래프에서 노드의 특정 속성을 선택하고 전용 UI 컨트롤 요소를 만드는 것으로 요약할 수 있습니다. 이는 그래프를 하위 그래프로 사용하거나 아카이브로 게시하는 경우 쉽게 사용할 수 있습니다. 더 이상 노드를 빠르고 쉽게 선택하고 해당 속성을 조정할 수 없으므로 이 특정 그래프와 관련된 모든 속성을 그룹화하는 다른 기본 제어판을 생성하는 것이 목표입니다.

다음은 노출 매개 변수에 대해 알아야 할 몇 가지 사항입니다.

* 노출 매개 변수 <b>컨트롤을 노드에서 그래프</b>(으)로 이동하며 기본적으로 계층 구조에서 한 수준 위로 이동합니다.
* 따라서 노출된 매개 변수는 더 이상 그래프에서만 변경할 수 없으며 노드에서 변경할 수 없습니다.
* 표시되는 매개 변수는 이름, 레이블, 값, UI 편집기 유형을 사용하여 완전히 사용자 지정할 수 있으며 특정 조건에 따라 숨겨지고 표시될 수도 있습니다.

매개 변수를 노출하는 것은 초보자에게 추상적이고 어려운 개념입니다.[이 항목에 대한 더 많은 전담 설명서가 있습니다](../../compositing-graphs/manage-parameters/exposing-a-parameter/exposing-a-parameter.md). 그러나 노출 매개 변수를 다루기 전에 소프트웨어의 다른 기본 측면을 충분히 익히는 것이 좋습니다.
