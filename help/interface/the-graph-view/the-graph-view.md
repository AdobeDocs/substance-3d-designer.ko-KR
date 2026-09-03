---
helpx_url: "https://helpx.adobe.com/kr/substance-3d-designer/interface/the-graph-view.html"
breadcrumb-title: ''
description: Substance 3D Designer에서 그래프 보기를 사용하여 노드 기반의 재질 그래프를 만들고 편집하는 방법을 알아봅니다.
helpx_creative_field: ""
helpx_description: Designer > Interface > Graph view
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 그래프 보기
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '3558'
ht-degree: 0%

---


# 그래프 보기

이 페이지에는 Substance 3D Designer의 그래프 보기 도크가 표시됩니다.

그래프 보기는 그래프를 작성하고 편집할 수 있는 [Substance 3D Designer](https://www.adobe.com/kr/products/substance3d-designer.html)의 기본 창입니다. 그래프 보기에는 두 개의 기본 영역이 있습니다. 즉, 맨 위에 도구 모음이 있어 특정 기능에 빠르게 액세스할 수 있으며 실제 그래프 영역에는 노드가 배치됩니다.

그래프 보기는 모든 그래프 유형에 사용되지만 주로 도구 모음 영역에서 [Substance 그래프](../../compositing-graphs/substance-compositing-graphs.md), [함수 그래프](../../function-graphs/function-graphs.md) 및 [FX-맵 그래프](../../function-graphs/fxmaps/fxmaps.md)가 약간 다릅니다.

## 뷰포트 탐색

다음 동작을 사용하여 그래프를 탐색할 수 있습니다.

* <b>이동:</b>MMB/Ctrl+RMB
* <b>확대/축소:</b> 마우스 휠/Alt + RMB

트랙패드 사용(macOS 전용)

* <b>이동: </b>두 손가락 스와이프
* <b>확대/축소:</b> Cmd를 누른 상태에서 두 손가락 핀치/두 손가락 스와이프

>[!NOTE]
>
> 확대/축소 방향
> 
> 각 확대/축소 방법은 다른 방법과 함께 반전됩니다.
> 
> * 그래프 보기를 더 가까이 *당기기* 마우스 휠을 올립니다.
> * Alt+RMB를 누르고 그래프 보기를 위로 *밀어내기* 드래그합니다.
> 
> [환경 설정](../../interface/preferences-window/preferences-window.md)에서 확대/축소 방향을 반전할 수 있습니다.

![뷰포트 탐색](the-graph-view.resources/the-graph-view-01.gif "뷰포트 탐색")

F 키를 사용하여 선택한 노드에 대해 <b>포커스</b>를 설정하거나, 선택한 항목이 없는 경우 전체 그래프를 사용합니다.

탐색은 <b>탐색 핀 </b>과 F2 키를 사용하여 수행할 수도 있습니다. 아래 [그래프 항목](#graph-items)을 참조하세요.[.](../../interface/the-graph-view/graph-items/graph-items.md)

## 객체 이동

개체(예: 노드 또는 그래프 항목)에서 LMB를 클릭한 다음 커서를 누르고 드래그하여 그래프 주위의 <b>노드를 이동</b>합니다. 개체를 두 개 이상 선택할 경우 선택한 모든 개체가 커서 아래에 있는 개체와 함께 이동됩니다.

개체를 이동하는 동안 커서 <b>이(가) 그래프 보기의 테두리</b>에 도달하면 커서 방향으로 보기가 패닝됩니다. 커서가 테두리에서 더 멀리 이동하므로 팬 속도가 더 빠릅니다.\
이는 그래프 뷰 테두리의 그리기 선택 상자에도 적용됩니다.

기본적으로 개체는 이동할 때 <b>격자에 물립니다</b>. 개체를 이동하는 동안 Ctrl 키(Windows)/⌘(macOS)를 누르고 있으면 해당 스냅을 사용할 수 없습니다.

## 그래프 항목

그래프를 구성하고 탐색하는 데 도움이 되는 몇 가지 도우미 개체를 사용할 수 있습니다. 특히 복잡한 노드 네트워크로 확장되어 읽기 어려울 수 있는 경우 유용합니다.

<b>점 노드</b>를 사용하면 연결 경로를 변경하고 병합할 수 있으며, <b>포털</b>로 사용하여 길고 다루기 어려운 연결을 숨길 수 있습니다.

<b>프레임</b>을 사용하면 표시된 제목과 색상 코딩으로 노드를 그룹화할 수 있습니다.

<b>주석</b>을 사용하면 노드 또는 노드 그룹의 목적을 추적하고 다른 유용한 주석을 만들 수 있습니다.

<b>탐색 핀</b>을 사용하면 그래프의 관심 지점으로 빠르게 이동할 수 있습니다.

>[!NOTE]
>
> 이 설명서의 [그래프 항목](../../interface/the-graph-view/graph-items/graph-items.md) 섹션에서 자세히 알아보십시오.

## 그래프 컨텍스트 메뉴

그래프의 빈 공간에서 RMB를 클릭하면 상황별 메뉴가 나타나고 다음 옵션이 포함될 수 있습니다.

<b>노드 추가:</b> [노드] 메뉴를 열어 그래프에 노드를 추가합니다.

<b>주석 추가:</b> 부모로 지정되지 않은 [주석](../../interface/the-graph-view/graph-items/graph-items.md) 그래프 개체를 추가합니다.

<b>프레임 추가:</b> [프레임](../../interface/the-graph-view/graph-items/graph-items.md) 그래프 개체를 추가합니다.

<b>핀 추가:</b> [핀](../../interface/the-graph-view/graph-items/graph-items.md) 그래프 개체를 추가합니다.

<b>점 노드 추가:</b> [점](../../interface/the-graph-view/graph-items/graph-items.md) 노드 추가;

<b>3D 보기에서 출력 보기:</b> 용도를 일치시켜 모든 그래프의 출력을 [3D 보기](../../interface/3d-view/3d-view.md)의 자료에 할당합니다. 아래의 [3D 보기와 상호 작용](#interacting-with-the-3d-view)을 참조하십시오.

<b>3D 보기에서 출력 재설정 및 보기:</b> [3D 보기에서 재질을 재설정하고](../../interface/3d-view/3d-view.md)의 사용을 일치시켜 모든 그래프의 출력을 해당 재질에 할당합니다. 아래의 [3D 보기와 상호 작용](#interacting-with-the-3d-view)을 참조하십시오.

<b>2D 보기에서 출력 보기:</b> 그래프의 출력 중 하나를 [2D 보기](../../interface/2d-view/2d-view.md)에 표시합니다. 아래의 [2D 보기와 상호 작용](#interacting-with-the-2d-view)을 참조하세요.

<b>노드 축소판 계산:</b> [이미지 캐시](../../interface/preferences-window/preferences-window.md)에 저장될 그래프의 모든 노드의 결과 계산을 트리거하고 첫 번째 출력을 축소판으로 사용합니다.

<b>노드 축소판 지우기:</b> 그래프에 있는 모든 노드의 결과를 포함하는 [이미지 캐시](../../interface/preferences-window/preferences-window.md)를 지우고, 노드의 축소판을 지웁니다.

<b>패키지 저장:</b> 이 그래프가 포함된 패키지를 저장합니다.

<b>붙여넣기:</b> 업스트림 연결을 포함하여 현재 클립보드에 복사된 노드를 커서의 위치에 붙여넣습니다. 커서가 그래프 뷰 뷰포트에 없으면 노드는 뷰포트의 중심에 배치됩니다.

<b>링크 없이 붙여넣기:</b> 업스트림 연결을 제외하고 클립보드에 현재 복사된 노드를 커서 위치에 붙여넣습니다. 커서가 그래프 뷰 뷰포트에 없으면 노드는 뷰포트의 중심에 배치됩니다.

<b>모두 선택:</b> 그래프에서 모든 노드를 선택합니다.

<b>이전 핀:</b> 그래프에서 이전 [핀](../../interface/the-graph-view/graph-items/graph-items.md) 개체로 이동합니다.

<b>다음 핀:</b> 그래프에서 다음 [핀](../../interface/the-graph-view/graph-items/graph-items.md) 개체로 이동합니다.

<b>선택 영역 복사:</b> 선택한 노드, 연결 및 매개 변수 값을 클립보드에 복사합니다.

<b>선택 항목 삭제:</b> 선택한 노드를 삭제합니다.

<b>삭제 및 다시 연결:</b> 선택한 노드를 삭제하고 가능한 경우 업스트림 노드에서 다운스트림 노드로의 직접 연결로 바꿉니다.

<b>선택 항목 복제:</b> 동일한 그래프에서 선택한 노드를 복제합니다(예: 업스트림 연결 포함). 커서가 있는 위치에 해당 노드를 복제합니다. 커서가 그래프 뷰 뷰포트에 없으면 노드는 뷰포트의 중심에 배치됩니다.

<b>링크 없이 선택 항목 복제:</b> 동일한 그래프에서 선택한 노드를 복제합니다(업스트림 연결 제외). 커서의 위치에서 노드를 복제합니다. 커서가 그래프 뷰 뷰포트에 없으면 노드는 뷰포트의 중심에 배치됩니다.

<b>업스트림 노드 선택:</b> 선택한 노드의 업스트림 노드를 모두 선택합니다.

<b>다운스트림 노드 선택:</b> 선택한 노드의 다운스트림 노드를 모두 선택합니다.

<b>링크 바꾸기\*:</b> 선택한 입력 및 출력 커넥터 쌍 사이의 연결을 바꿉니다.

<b>노드/선택 비활성화:</b> 선택한 노드가 스트림 결과에 영향을 주지 않도록 노드를 비활성화합니다. 아래의 <b>노드 비활성화</b>를 참조하십시오.

<b>\*:</b> 선택 항목에 두 개의 링크가 있거나 두 개의 노드가 동일한 세 번째 노드의 입력에 연결된 세 개의 노드만 사용할 수 있습니다.

## 노드 작업

그래프는 주로 데이터를 수집, 생성 및 수정한 다음 그래프의 결과로 출력할 수 있는 노드에 대한 그릇입니다. 노드를 사용하려면 다음과 같은 개념과 작업이 필요합니다.

### 노드 생성 및 관리

그래프 유형에 관계없이 5가지 방법으로 그래프에 노드를 배치할 수 있습니다.

* 노드 도구 모음의 아이콘을 클릭하거나 드래그합니다(아래 참조). [Atomic nodes](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/atomic-nodes.md)만 이 방법으로 배치할 수 있습니다.
* 그래프의 빈 영역을 마우스 오른쪽 단추로 클릭하고 <b>노드 추가</b>를 선택합니다. [Atomic nodes](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/atomic-nodes.md)만 이 방법으로 배치할 수 있습니다.
* 축소판을 라이브러리 보기에서 그래프 보기로 드래그 이 메서드는 [노드 인스턴스](../../compositing-graphs/nodes-reference-for-com/node-library/node-library.md)를 포함한 모든 유형의 노드에 대해 작동합니다.
* <b>스페이스바</b>를 눌러 <b>노드 메뉴</b>에 액세스합니다. 아래를 참조하십시오.
* 노드에 매핑된 키보드 단축키 사용 매핑은 [환경 설정 창](../../interface/preferences-window/preferences-window.md)에서 수행됩니다.

![노드 배치](the-graph-view.resources/the-graph-view-02.gif "노드 배치")

다른 노드가 선택되어 있을 때 노드가 배치되면 Designer은 새 노드를 이전 노드에 자동으로 연결하려고 시도합니다.\
이 자동 연결은 항상 새 노드 *이전 노드*&#x200B;를 플로우에 배치합니다.

노드 제거는 손실된 링크를 처리할 방법에 따라 두 가지 방법으로 수행할 수 있습니다.

* 노드를 선택하고 Delete 키를 누르거나 마우스 오른쪽 단추를 클릭하고 <b>선택 영역 삭제</b>를 선택합니다. 이렇게 하면 기존의 모든 연결이 끊어지고 기능이 손상될 수 있습니다.
* 노드를 선택하고 백스페이스를 누르거나 마우스 오른쪽 단추를 클릭하고 <b>삭제 및 다시 연결</b>을 선택합니다. 이렇게 하면 가능한 경우 링크가 유지되어 끊어진 기능이 방지됩니다.

<table>
<tr style="border: 0;">
<td width="100.00%" style="border: 0;" valign="top">

### 노드 메뉴

그래프 보기에서 <b>스페이스바</b>를 누르면 [노드] 메뉴가 표시됩니다.

이 메뉴는 검색 인터페이스를 통해 [라이브러리](../../interface/the-library/the-library.md)의 모든 노드에 액세스할 수 있으며 즐겨 찾는 노드가 목록의 맨 위에 표시되도록 합니다.

화살표 키를 사용하여 검색 결과를 확인할 수 있습니다. *루프*&#x200B;가 나열되므로 첫 번째 항목에 &#39;위쪽&#39; 화살표 키를 사용하면 마지막 항목으로 이동합니다.

검색어가 *유사 항목*&#x200B;이므로 검색 용어에서 작은 차이를 용서합니다. 예: &#39;색상&#39; 대 &#39;색상&#39;, &#39;표준화&#39; 대 &#39;표준화&#39; 등.

그래프에서 *단일* 노드를 선택하거나 노드 커넥터를 끌어 노드 메뉴를 만들면 검색 결과가 출력 유형에 따라 자동으로 *필터링*&#x200B;됩니다.\
예를 들어, Grayscale 유형의 [기본 입력](../../compositing-graphs/inheritance-compositing/inheritance-in-substance-compositing-graphs.md)이 있는 노드만 Grayscale 유형의 출력에 나열됩니다.

</td>
<td width="33.33%" style="border: 0;" valign="top">

![그래프 보기: 노드 메뉴](the-graph-view.resources/the-graph-view-03.png "그래프 보기: 노드 메뉴")

</td>
</tr>
</table>

### 노드 선택

하나 이상의 노드를 선택하여 복사하거나 삭제하거나 그래프 주위로 이동할 수 있습니다.

*단일* 노드를 선택하려면 노드에 커서를 놓고 LMB를 클릭합니다.

*다중* 노드를 선택하려면 다음과 같은 방법을 사용할 수 있습니다.

* <b>하나씩:</b> Ctrl 키를 누른 채 노드에서 LMB를 클릭합니다. 선택되지 않은 노드는 선택 항목에 *추가*&#x200B;되고, 선택한 노드는 선택 항목에서 *제거*&#x200B;됩니다.
* <b>선택 상자:</b> 그래프의 빈 공간에서 LMB를 클릭하고 *커서를 누른 상태에서 드래그*&#x200B;하여 선택 상자를 그립니다. LMB를 해제할 때 상자에 *적어도 부분적으로 포함된* 노드가 선택됩니다.
* <b>업스트림:</b> 노드에서 RMB를 클릭하고 <b>업스트림 노드 선택</b> 옵션을 선택합니다. 노드의 *입력*&#x200B;에 연결된 스트림의 일부인 노드와 모든 노드가 선택됩니다.
* <b>다운스트림:</b> 노드에서 RMB를 클릭하고 <b>다운스트림 노드 선택</b> 옵션을 선택합니다. 노드의 *출력*&#x200B;에 연결된 스트림의 일부인 노드와 모든 노드가 선택됩니다.

![노드 선택](the-graph-view.resources/the-graph-view-04.gif "노드 선택")

### 노드 컨텍스트 메뉴

노드에서 RMB를 클릭하면 상황별 메뉴가 나타나고 다음 옵션이 포함될 수 있습니다.

<b>2D 보기에서 출력 보기:</b> 노드의 출력 중 하나를 [2D 보기](../../interface/2d-view/2d-view.md)에 표시합니다. 아래의 [2D 보기와 상호 작용](#interacting-with-the-2d-view)을 참조하세요.

<b>3D 보기에서 보기</b>: 사용을 일치시켜 모든 노드의 출력을 [3D 보기](../../interface/3d-view/3d-view.md)의 자료에 할당합니다. 아래의 [3D 보기와 상호 작용](#interacting-with-the-3d-view)을 참조하십시오.

<b>3D 보기에서 보기 재설정:</b> [3D 보기에서 재질을 재설정하고](../../interface/3d-view/3d-view.md)의 사용을 일치시켜 해당 재질에 모든 노드의 출력을 할당합니다. 아래의 [3D 보기와 상호 작용](#interacting-with-the-3d-view)을 참조하십시오.

<b>3D 보기에서 출력 보기\*:</b> 사용을 일치시켜 [3D 보기](../../interface/3d-view/3d-view.md)의 자료에 특정 노드 출력을 할당합니다.

<b>주석 추가:</b> [주석](../../interface/the-graph-view/graph-items/graph-items.md) 그래프 개체를 만들고 이 노드에 부모로 지정합니다.

<b>프레임 추가:</b> [프레임](../../interface/the-graph-view/graph-items/graph-items.md) 그래프 개체를 만들고 선택한 노드에 맞춥니다.

<b>정보를 클립보드에 복사:</b> 노드의 고유 식별자(UID)를 클립보드에 복사합니다.

<b>노출 매개 변수:</b> 이 노드에 대한 [노드 매개 변수 노출](../../compositing-graphs/manage-parameters/exposing-a-parameter/exposing-a-parameter.md) 대화 상자를 표시합니다.

<b>만들기\*:</b> 이 노드의 각 입력 및/또는 출력에 대한 입력 및/또는 출력 노드를 만듭니다.

<b>참조 열기\*:</b> 이 노드에서 참조하는 [그래프](../../compositing-graphs/creating-compositing-gra/graph-instances-sub-gra/graph-instances-sub-graphs.md)를 별도의 [그래프 보기] 탭으로 로드합니다.

<b>컨텍스트에서 참조 열기\*\*:</b> 현재 그래프의 컨텍스트에서 이 노드에서 참조하는 [그래프](../../compositing-graphs/creating-compositing-gra/graph-instances-sub-gra/graph-instances-sub-graphs.md)를 기존 [그래프 보기] 탭에 탐색 경로로 로드합니다.

<b>선택 영역에서 그래프 만들기:</b> 선택한 노드를 새 그래프로 복사;

<b>선택 영역 복사:</b> 선택한 노드, 연결 및 매개 변수 값을 클립보드에 복사합니다.

<b>선택 항목 삭제:</b> 선택한 노드를 삭제합니다.

<b>삭제 및 다시 연결:</b> 선택한 노드를 삭제하고 가능한 경우 업스트림 노드에서 다운스트림 노드로의 직접 연결로 바꿉니다.

<b>선택 항목 복제:</b> 업스트림 연결을 포함하여 동일한 그래프에서 선택한 노드를 복제합니다.

<b>링크 없이 선택 항목 복제:</b> 업스트림 연결을 제외한 동일한 그래프에서 선택한 노드를 복제합니다.

<b>업스트림 노드 선택:</b> 선택한 노드의 업스트림 노드를 모두 선택합니다.

<b>다운스트림 노드 선택:</b> 선택한 노드의 다운스트림 노드를 모두 선택합니다.

<b>링크 바꾸기\*\*\*:</b> 선택한 입력 및 출력 커넥터 쌍 간의 연결을 바꿉니다.

<b>노드/선택 비활성화:</b> 노드 또는 선택한 노드를 비활성화하여 스트림 결과에 영향을 주지 않도록 합니다. 아래의 <b>노드 비활성화</b>를 참조하십시오.

<b>\*</b>: [그래프 인스턴스](../../compositing-graphs/creating-compositing-gra/graph-instances-sub-gra/graph-instances-sub-graphs.md) 노드에만 사용할 수 있습니다.\
<b>\*\*:</b> [그래프 인스턴스](../../compositing-graphs/creating-compositing-gra/graph-instances-sub-gra/graph-instances-sub-graphs.md) 노드 및 [환경 설정](../../interface/preferences-window/preferences-window.md)에서 <b>직접 편집 사용</b> 옵션을 선택한 경우에만 사용할 수 있습니다.\
<b>\*\*\*:</b> 선택 항목에 두 개의 링크가 있거나 두 개의 노드가 동일한 세 번째 노드의 입력에 연결된 세 개의 노드만 사용할 수 있습니다.

>[!IMPORTANT]
>
> 커서를 노드 위에 *놓을 때* RMB *을 클릭하면* 이러한 상황에 맞는 메뉴 옵션 중 일부는 그래프에서 다른 노드가 현재 *선택*&#x200B;되었는지 여부에 관계없이 *해당* 노드를 대상으로 합니다.
> 
> 따라서 일관성 있게 예측 가능한 결과를 얻으려면 컨텍스트 메뉴 동작을 사용하여 실제로 대상으로 지정하려는 선택 영역의 일부인 노드 위에 항상 커서를 놓는 것이 좋습니다.

### 노드 연결

노드 A의 *출력 커넥터*&#x200B;를 다른 노드 B의 *입력 커넥터*&#x200B;에 연결할 수 있으며, 이로 인해 노드 B는 계산을 수행하기 위해 A가 출력한 데이터를 사용합니다.

>[!NOTE]
>
> 노드의 모든 커넥터가 반드시 연결되어 있어야 하는 것은 *아닙니다*. 커넥터를 비워 두면 다음과 같은 결과가 발생합니다.
> 
> * *입력* 커넥터의 경우: 노드가 해당 입력에 설정된 기본값으로 되돌아갑니다.
> * *출력* 커넥터의 경우: 그래프를 계산할 때 데이터가 무시되고 삭제됩니다.

![노드 연결](the-graph-view.resources/the-graph-view-05.gif "노드 연결")

각 커넥터에서 *임의의 순서*&#x200B;로 LMB를 클릭하여 새 링크를 <b>생성</b>할 수 있습니다.\
또한 노드 A를 선택한 상태에서 노드 B를 만들면 노드 A의 *첫 번째 출력*&#x200B;이 자동으로 노드 B의 *기본 입력*&#x200B;에 연결됩니다.

*기존* 링크에 대해 다음 작업을 수행할 수 있습니다.

<b>삭제:</b> 링크에 LMB를 클릭하고 *삭제*<b>, </b>를 누르거나 링크가 있는 연결을 Alt+클릭하여 링크를 삭제합니다. Alt 키를 누른 채 클릭하면 해당 연결의 모든 링크가 삭제됩니다.

<b>복제:</b> Ctrl 키를 누른 상태에서 연결선의 LMB를 클릭하고 커서를 드래그하여 링크를 복제합니다. 링크를 연결하려면 다른 커넥터의 LMB 를 클릭합니다.

<b>이동:</b> Shift 키를 누른 상태에서 연결선의 LMB를 클릭하고 커서를 드래그하여 연결선에서 다른 연결선으로 링크를 가져와 이동할 수 있습니다. 링크를 연결하려면 다른 커넥터의 LMB 를 클릭합니다.

### 노드 사용 안 함

>[!NOTE]
>
> 이는 [Substance 그래프](../../compositing-graphs/substance-compositing-graphs.md)에만 적용됩니다.

그래프에 *효과 없음*&#x200B;이 되도록 노드를 사용하지 않도록 설정할 수 있지만 연결을 끊거나 삭제할 필요는 없습니다.

비활성화된 노드에는 다음과 같은 동작이 있습니다.

* 썸네일 대신 ![](the-graph-view.resources/the-graph-view-06.png) <b>비활성화</b> 배지&#x200B;*,**점선 윤곽선* 및 내부 *라우팅* 링크와 함께 표시됩니다.
* 노드는 *기본 입력*&#x200B;에서 받은 데이터를 출력합니다.
* 비활성화된 노드는 함께 *연결*&#x200B;될 수 있습니다.
* 해당 속성 및 연결이 *수정되지 않음*;
* 사용 안 함 상태는 *저장됨*&#x200B;이며 세션 간에 유지됩니다.
* SBSAR에 게시할 때 결과 파일은 *노드 비활성화 상태(즉, 표시되는 항목)를 고려합니다*.

<b>Shift+D</b> 키 입력을 사용하거나 그래프를 마우스 오른쪽 단추로 클릭하고 상황별 메뉴에서 <b>노드 사용 안 함/선택 사용 안 함</b> 항목을 선택하여 노드 또는 선택한 노드 그룹을 사용하지 않도록 설정할 수 있습니다.

>[!IMPORTANT]
>
> 다음 조건과 일치하는 노드만 비활성화할 수 있습니다.
> 
> * 노드에 *한 개의 입력*&#x200B;이 있습니다.
> * 노드에 *한 개의 출력*&#x200B;만 있습니다.
> * 기본 입력과 출력의 *유형*&#x200B;은 *일치*&#x200B;해야 합니다(예: 회색 음영과 회색 음영, 색상과 색상).
> * 선택한 모든 노드에는 *동일한 상태*&#x200B;가 있어야 합니다. 즉, 모든 노드를 사용하도록 설정해야 하며, 사용 가능하도록 동일한 규칙이 적용됩니다.

![노드 비활성화](the-graph-view.resources/the-graph-view-07.gif "노드 비활성화"){width="512px"}

## 2D 뷰와 상호 작용

>[!NOTE]
>
> 이는 [Substance 그래프](../../compositing-graphs/substance-compositing-graphs.md)에만 적용됩니다.

노드 출력을 [2D 보기](../../interface/2d-view/2d-view.md)에 표시하려면 노드에서 LMB를 두 번 클릭하거나 노드에서 RMB를 클릭하고 상황에 맞는 메뉴에서 [2D 보기에서 출력 보기](#interacting-with-the-2d-view) 옵션을 선택합니다. 노드에 둘 이상의 출력이 있는 경우 하위 메뉴에서 원하는 출력을 선택합니다.

[그래프 보기](https://substance3d.adobe.com/)의 빈 영역에서 RMB를 클릭하고 컨텍스트 메뉴에서 [2D 보기에서 출력 보기](#interacting-with-the-2d-view) 옵션을 선택하여 2D 보기에서 그래프 출력을 표시할 수 있습니다. 그래프에 출력이 두 개 이상 있는 경우 하위 메뉴에서 원하는 출력을 선택합니다.

## 3D 뷰와 상호 작용

>[!NOTE]
>
> 이는 [Substance 그래프](../../compositing-graphs/substance-compositing-graphs.md)에만 적용됩니다.

[3D 보기](../../interface/3d-view/3d-view.md)에서 노드 출력을 적용하려면 노드에서 RMB를 클릭하고 상황에 맞는 메뉴에서 <b>3D 보기에서 보기</b> 옵션을 선택합니다. 노드에 둘 이상의 출력이 있는 경우 하위 메뉴에서 원하는 출력을 선택합니다. 그런 다음 3D 뷰에서 현재 사용되는 셰이더의 대상 채널을 선택합니다.

(*[Substance 그래프](../../compositing-graphs/substance-compositing-graphs.md)만*) 그래프 보기의 빈 영역에서 RMB를 클릭하고 컨텍스트 메뉴에서 <b>3D 보기에서 출력 보기</b> 옵션을 선택하여 3D 보기에서 모든 그래프 출력을 적용할 수 있습니다. 그래프에 하나 이상의 [출력](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/output/output.md) 노드가 있고 [올바르게 설정](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/output/output.md)되었는지 확인하십시오.

## 도구 모음

>[!NOTE]
>
> 전체 목록은 [Substance 그래프](../../compositing-graphs/substance-compositing-graphs.md)에만 적용됩니다. 다른 그래프 유형에는 이러한 옵션 중 *제한된 집합*&#x200B;이 있습니다.

### 그래프 도구

기본 도구 모음은 모든 그래프 유형에서 찾을 수 있으며 일반 기능을 제공할 뿐만 아니라 다른 도구 모음의 가시성을 위해 토글합니다. 다음 함수를 찾을 수 있습니다.

![](the-graph-view.resources/the-graph-view-08.png) <b>초점 선택</b>(F)\
선택 영역에 포커스 보기, 또는 선택 영역이 비어 있는 경우 전체 장면

![](the-graph-view.resources/the-graph-view-09.png) <b>확대/축소 재설정</b>(Z)\
현재 확대/축소 레벨을 기본 상태로 되돌리고 그래프 가운데에 보기를 배치합니다. 확대 또는 축소를 의미할 수 있습니다.

![](the-graph-view.resources/the-graph-view-10.png) <b>그래프 내보내기 보기\
</b>전체 그래프를 1:1 해상도로 이미지로 내보냅니다. 전체 그래프의 스크린샷을 공유하는 데 유용합니다.

![](the-graph-view.resources/the-graph-view-11.png) <b>노드 정보\
</b>*- 커넥터 이름 표시:* 노드에 있는 각 개별 커넥터의 이름 표시를 전환합니다.\
*- 노드 배지 표시:* 모든 노드에서 노드 배지를 토글합니다.\
*- 노드 크기 표시:* 노드 해상도 표시를 토글합니다([Substance 그래프](../../compositing-graphs/substance-compositing-graphs.md)만 해당).\
*- 표시 타이밍:* 각 노드의 밀리초 타이밍 표시를 토글합니다([Substance 그래프](../../compositing-graphs/substance-compositing-graphs.md)만).\
*- 축소할 때 텍스트 크기 제한:* [그래프 항목](../../interface/the-graph-view/graph-items/graph-items.md)의 텍스트를 확대/축소 임계값을 초과하는 일정한 화면 크기로 유지하므로 축소할 때 텍스트가 명확하게 표시됩니다.

![](the-graph-view.resources/the-graph-view-12.png)<b> 노드 찾기 도구</b>(Ctrl+F)\
도구가 그래프에서 노드, 노출된 매개 변수 및 기타 변수를 찾을 수 있도록 합니다. [전용 페이지](../../interface/the-graph-view/node-finder/node-finder.md)에서 자세히 알아보세요.

![](the-graph-view.resources/the-graph-view-13.png) <b>하이라이트 플로우\
</b>현재 선택한 노드 앞이나 뒤에 연결된 노드를 강조 표시합니다. 복잡한 노드 경로를 추적하는 데 유용합니다.

![](the-graph-view.resources/the-graph-view-14.png) <b>노드 팔레트\
</b>노드 도구 모음을 표시하거나 숨깁니다(아래 참조).

![](the-graph-view.resources/the-graph-view-15.png) <b>직사각형 링크\
</b>노드 간에 둥근 또는 직사각형 모양의 링크 사이를 전환합니다. [FX-Maps](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/fx-map/fx-map.md)에 사용할 수 없습니다.

![](the-graph-view.resources/the-graph-view-16.png) <b>노드 정렬 도구\
</b>그래프에서 선택한 노드를 정렬할 수 있는 도구를 사용할 수 있습니다. [전용 페이지](../../interface/the-graph-view/node-alignment-tools/node-alignment-tools.md)에서 자세히 알아보세요.

[Substance 그래프](../../compositing-graphs/substance-compositing-graphs.md)에서만:

![](the-graph-view.resources/the-graph-view-17.png) <b>부모 크기\
</b>부모 해상도 컨트롤 설정을 표시하거나 숨깁니다(아래 참조).

![](the-graph-view.resources/the-graph-view-18.png) <b>링크 만들기 모드</b> (1, 2, 3)\
노드 커넥터를 개별적으로 또는 일괄적으로 연결하려면 표준(1), 재질(2) 및 컴팩트 재질(3) 링크 생성 모드 중에서 선택합니다. [전용 페이지](../../interface/the-graph-view/link-creation-modes/link-creation-modes.md)에서 자세히 알아보세요.

![](the-graph-view.resources/the-graph-view-19.png) <b>시간 컨트롤\
</b>모든 노드를 다시 설정하고 모든 시간을 다시 설정할 수 있습니다.

![](the-graph-view.resources/the-graph-view-20.png) <b>도구\
</b>*- 정리:* [출력](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/output/output.md) 노드에 연결되지 않은 스트림의 일부인 모든 노드를 제거합니다.\
*- 출력 내보내기:* [비트맵 내보내기 인터페이스](../../compositing-graphs/exporting-bitmaps/exporting-bitmaps.md)를 엽니다.\
*- 출력 다시 내보내기:* 이전 내보내기 작업을 다시 수행합니다.\
*- PSD 내보내기 도구:* [PSD 내보내기 도구](../../compositing-graphs/exporting-psd-files/exporting-psd-files.md) 인터페이스를 엽니다.

![](the-graph-view.resources/the-graph-view-21.png) <b>노드 이미지 캐시\
</b>노드 이미지 캐시 표시를 토글합니다(아래 참조).

![](the-graph-view.resources/the-graph-view-22.jpg) 사용하지 않는 노드 제거\
</b>사용하지 않는 노드를 제거하기 위한 옵션을 그래프로 표시합니다(아래 참조).

### 노드 팔레트

노드 도구 모음은 그래프 유형에 따라 다릅니다.

[![노드 팔레트](the-graph-view.resources/the-graph-view-23.png)](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/atomic-nodes.md)<br>
<b>[Substance 그래프](../../compositing-graphs/substance-compositing-graphs.md):</b> [원자 노드](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/atomic-nodes.md) 및 [그래프 항목](../../interface/the-graph-view/graph-items/graph-items.md)을 참조하세요.


![그래프 항목 팔레트](the-graph-view.resources/the-graph-view-24.png "그래프 항목 팔레트")<br>
<b>[Substance 함수 그래프](../../function-graphs/function-graphs.md):</b> [그래프 항목](../../interface/the-graph-view/graph-items/graph-items.md)을 참조하세요.


![FX-맵 팔레트](the-graph-view.resources/the-graph-view-25.png "FX-맵 팔레트")<br>
<b>[FX-지도 그래프](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/fx-map/fx-map.md):</b> [그래프 항목 보기](../../interface/the-graph-view/graph-items/graph-items.md)

### 마스터 크기

![부모 크기 도구 모음](the-graph-view.resources/the-graph-view-26.png "부모 크기 도구 모음")

이 도구 모음은 [Substance 그래프](../../compositing-graphs/substance-compositing-graphs.md)에서만 사용할 수 있으며 그래프의 *부모*&#x200B;에 대한 [출력 크기](../../compositing-graphs/output-size/output-size.md)를 설정합니다. 이는 *부모에 대한 상대* [상속 메서드](../../compositing-graphs/inheritance-compositing/inheritance-in-substance-compositing-graphs.md)를 사용하는 경우 그래프의 출력 크기에 영향을 줍니다.

가로 및 세로 크기는 기본적으로 연결되어 있지만 정사각형이 아닌 텍스처의 경우 *연결 해제*&#x200B;가 될 수 있습니다. 값을 기본값인 256 x 256으로 다시 설정할 수도 있습니다.

### 노드 이미지 캐시

![노드 이미지 캐시 설정](the-graph-view.resources/the-graph-view-27.png "노드 이미지 캐시 설정")

[Substance 그래프](../../compositing-graphs/substance-compositing-graphs.md)에서 노드를 계산할 때 캐시 사용을 전환합니다.

노드가 계산되면 해당 출력 이미지가 메모리(예: 캐시)에 저장되므로 이 노드가 변경의 영향을 받지 않는 경우 그래프를 다시 계산할 때 *다시 사용*&#x200B;할 수 있습니다. 즉, 실제로 변경되는 그래프의 부분만 다시 계산됩니다.

이 캐시의 메모리 저장소 제한은 <b>메모리</b> 섹션 아래의 [환경 설정](../../interface/preferences-window/preferences-window.md)의 <b>일반</b> 섹션에서 변경할 수 있습니다.

이 옵션을 활성화하면 Designer의 메모리 사용량이 크게 증가하는 대신 그래프 계산의 전체 응답성이 크게 향상됩니다.

### 사용하지 않는 노드 제거

![사용하지 않는 노드 제거 드롭다운 메뉴](the-graph-view.resources/the-graph-view-28.jpg "사용하지 않는 노드 제거 드롭다운 메뉴")

그래프에서 반복하고 작업을 시도할 때 최종 결과에 영향을 주지 않는 일부 노드가 뒤에 표시될 수 있습니다. 이렇게 하면 모든 노드가 그래프 렌더링의 첫 번째 단계에서 평가되므로 낭비적인 계산뿐만 아니라 잡동사니도 추가됩니다.

![](the-graph-view.resources/the-graph-view-22.jpg) 사용하지 않는 노드 제거</b> 도구는 *출력* 노드에서 끝나는 스트림의 *일부가 아닌* 모든 노드를 삭제합니다. *입력* 노드를 삭제하면 이 그래프를 참조하는 [인스턴스 노드](../../compositing-graphs/creating-compositing-gra/graph-instances-sub-gra/graph-instances-sub-graphs.md)의 인터페이스가 변경되므로 예외는 입력노드입니다.

![사용하지 않는 노드 제거](the-graph-view.resources/the-graph-view-29.gif "사용하지 않는 노드 제거")

첫 번째 옵션은 *현재* 그래프에만 클리닝을 적용합니다.

현재 그래프가 [Substance 그래프](../../compositing-graphs/substance-compositing-graphs.md)인 경우 두 번째 옵션을 사용할 수 있습니다. 이 옵션을 사용하면 정리 프로세스에 *모든 노드 매개 변수 함수를 포함할 수 있습니다*. 즉, 노드 매개 변수 값을 제어하는 [함수 그래프](../../function-graphs/function-graphs.md)에 사용되지 않은 노드가 있으면 해당 그래프도 같은 규칙을 따라 정리됩니다.

정리가 완료되면 보고서 대화 상자가 표시됩니다. 로그에 `GraphCleaner` 태그가 지정되었으므로 <b>콘솔</b>에서 더 많은 세부 정보를 찾을 수 있습니다. 이러한 로그에는 그래프 및 매개 변수 함수당 제거된 노드 수가 포함됩니다.

*단일* 작업으로 영향을 받는 모든 그래프에서 지우기를 실행 취소할 수 있습니다.
