---
helpx_url: "https://helpx.adobe.com/kr/substance-3d-designer/substance-compositing-graphs/creating-a-substance-compositing-graph/graph-instances-sub-graphs.html"
breadcrumb-title: ''
description: 그래프 인스턴스 및 하위 그래프를 사용하여 재사용 가능한 그래프 구성 요소 및 모듈식 재질 워크플로우를 생성합니다.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Creating a Substance compositing graph > Graph instances and subgraphs
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 그래프 인스턴스 및 하위 그래프
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '601'
ht-degree: 0%

---


# 그래프 인스턴스 및 하위 그래프

![](graph-instances-sub-graphs.resources/graph-instances-sub-graphs-01.png)

그래프 인스턴스는 <b>다른 그래프를 참조</b>하는 노드입니다. 호스트 그래프에서 인스턴스 노드가 참조하는 그래프를 호스트 그래프의 <b>하위 그래프</b>이라고 할 수 있다.

인스턴스를 사용하면 서로 다른 여러 패키지에서 하나 이상의 그래프에서 그래프를 여러 번 재사용할 수 있습니다.

## 그래프 인스턴스를 사용해야 하는 이유는 무엇입니까?

<b>그래프를 여러 하위 그래프로 분할</b>하면 *훨씬* 더 효율적으로<b> 작업할 수 있습니다.</b>

Designer에서 노드 체인을 복제할 때마다 해당 체인을 하위 그래프으로 분할하여 재사용하거나 업데이트할 수 있습니다.

>[!NOTE]
>
> *사용자 지정* 필터에 대한 하위 그래프의 간단한 설정을 보여 주는 프로젝트 파일은 이 설명서의 [샘플 Substance 그래프](../../../compositing-graphs/sample-compositing-graphs/sample-substance-compositing-graphs.md) 섹션에서 확인할 수 있습니다.

### 그래프 인스턴스를 어떻게 만듭니까?

그래프 A를 탐색기에서 다른 그래프 B로 드래그하여 그래프 A를 참조하는 <b>인스턴스 노드</b>를 만듭니다.

노드를 선택하고 컨텍스트 메뉴에서 &#39;선택 항목에서 그래프 만들기&#39;를 사용하여 노드를 새 그래프로 빠르게 분할할 수 있습니다. 그러면 새 그래프의 식별자를 설정하라는 메시지가 표시되며, 이 식별자는 고유해야 합니다.

선택한 노드가 그래프의 다른 노드에 연결된 경우 이러한 연결을 하위 그래프로 전달하려면 새 그래프에 [입력](../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/input/input.md) 및 [출력](../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/output/output.md) 노드도 만들어야 합니다.

또한 원래 노드를 새 그래프를 참조하는 인스턴스 노드로 바꾸는 작업은 나중에 수동으로 수행해야 합니다.

마지막으로 공유 가능한 SBSAR 파일에 프로젝트를 게시할 때 하위 그래프를 사용자에게 노출할지 여부를 결정해야 합니다. [그래프의 속성](../../../compositing-graphs/graph-parameters/graph-parameters.md)에서 &#39;SBSAR에 노출됨&#39; 매개 변수를 참조하십시오.

### 상속과 관련된 단어

하위 그래프를 사용하는 또 다른 이점은 하위 그래프의 각 인스턴스가 사용 중인 컨텍스트에 <b>맞게</b> 조정할 수 있다는 것입니다. 즉, 동일한 그래프의 두 인스턴스가 서로 다른 출력 해상도, 비트 심도 및 타일링 모드를 가질 수 있습니다.

이는 그래프 작업의 <b>기본 개념</b>이며, 인스턴스를 사용하여 더 진행할 준비가 되면 Substance 그래프의 [상속](../../../compositing-graphs/inheritance-compositing/inheritance-in-substance-compositing-graphs.md)에 대해 자세히 알아보는 것이 좋습니다.

그래프 인스턴스 및 하위 그래프 개념은 Substance 함수 그래프에도 적용되지만, 해당 페이지에서 설명한 대로 상속은 Substance 그래프에만 적용됩니다.

### 내 그래프 인스턴스를 노드 라이브러리에 추가할 수 있습니까?

<b>예, </b>할 수 있지만 특정 설정이 필요합니다. 이 설명서의 [사용자 지정 콘텐츠 및 필터 관리](../../../interface/the-library/managing-custom-content/managing-custom-content-and-filters.md) 페이지에서 자세히 알아보십시오.

### 그래프 인스턴스의 소스 그래프를 검사할 수 있습니까?

![(틱)](graph-instances-sub-graphs.resources/check.svg) 예, **Substance 3D 파일(SBS)**&#x200B;에서 로드된 그래프 인스턴스의 경우 *전용*&#x200B;입니다. 이러한 인스턴스 노드에는 *진한 빨강* 레이블이 있습니다.\
노드를 마우스 오른쪽 단추로 클릭하여 상황별 메뉴를 열고 **참조 열기** 옵션을 선택합니다.

>[!NOTE]
>
> 소스 그래프를 검사하는 동안 [환경 설정](../../../interface/preferences-window/preferences-window.md)의 **그래프** 섹션에서 **컨텍스트 편집** 옵션이 *선택*&#x200B;된 경우 인스턴스 그래프의 입력 데이터를 사용할 수 있습니다.

![(빼기)](graph-instances-sub-graphs.resources/forbidden.svg) **Substance 3D 에셋(SBSAR)** 인스턴스에서 로드된 그래프를 검사하는 것은 *불가능합니다*. 해당 그래프는 이미 컴파일되었습니다. **탐색기** 패널에서만 에셋을 로드하여 노출된 그래프 목록과 해당 매개 변수를 검사할 수 있습니다. 이러한 인스턴스 노드에는 *녹색* 레이블이 있습니다.\
노드를 마우스 오른쪽 단추로 클릭하여 상황별 메뉴를 열고 **패키지 로드** 옵션을 선택합니다.

>[!NOTE]
>
> **Atomic nodes**
> 
> *Atomic* 노드는 Substance 엔진의 코드를 통해 직접 구현되며 그래프의 *아니* 인스턴스이므로 atomic이라는 이름이 [Substance 그래프](../../../compositing-graphs/substance-compositing-graphs.md)의 다른 노드를 *모두*&#x200B;에 대해 *가장 작은 빌딩 블록*&#x200B;입니다.
