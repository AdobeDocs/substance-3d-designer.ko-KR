---
helpx_url: "https://helpx.adobe.com/kr/substance-3d-designer/substance-compositing-graphs/manage-parameters/parameter-presets.html"
breadcrumb-title: ''
description: Substance 3D Designer에서 매개 변수 사전 설정을 만들고 사용하여 매개 변수 구성을 저장하고 적용하는 방법을 알아봅니다.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Exposing a parameter > Parameter presets
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 매개 변수 사전 설정
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '479'
ht-degree: 0%

---


# 매개 변수 사전 설정

[매개 변수 사전 설정]을 통해 사용자는 매개 변수 집합에 대해 미리 구성된 대량의 값을 저장하고 전송할 수 있습니다.이 기능은 여러 가지 시나리오에 도움이 될 수 있으며, 다양한 가능성이 있는 매개 변수가 다량 있는 경우 가장 유용합니다.

사전 설정을 저장하고 불러오는 방법에는 두 가지가 있으며, 두 가지 사용 사례 모두 아래에 자세히 설명되어 있습니다.

![사전 설정 불러오기/저장 드롭다운 메뉴](parameter-presets.resources/parameter-presets-01.gif "사전 설정 불러오기/저장 드롭다운 메뉴"){width="512px"}

## 외부 사전 설정

[외부 사전 설정]에는 \*.SBSPRS 파일인 디스크의 외부 파일이 포함되어 있습니다. 서로 다른 그래프와 노드 간에 전송할 수 있지만 응용 프로그램 내에서만 전송할 수 있습니다. 이것의 주요 목적은 바로 이것입니다: 너무 큰 값을 전송해서 하나씩 복사할 수 없습니다.

외부 사전 설정은 [그래프 인스턴스](../../../compositing-graphs/creating-compositing-gra/graph-instances-sub-gra/graph-instances-sub-graphs.md)의 모든 특정 매개 변수, [원자 노드](../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/atomic-nodes.md)의 대부분의 특정 매개 변수([예외는 노출할 수 없는 매개 변수](../../../compositing-graphs/manage-parameters/exposing-a-parameter/exposing-a-parameter.md)) 및 Substance 그래프의 [매개 변수](../../graph-parameters/graph-parameters.md)매개 변수에 노출된 입력 매개 변수에 사용할 수 있습니다.

이 메뉴를 통해 저장하고 불러올 수 있습니다. 저장된 SBSPRS 파일은 다른 노드 또는 그래프에 로드할 수 있습니다.

>[!NOTE]
>
> 부분 일치도 작동함: 로드된 노드에 없는 SBSPRS에 저장된 매개 변수는 무시됩니다. 즉, [타일 Sampler의 색상 및 회색 음영 버전과 같이 대부분 유사한 노드 간에 속성을 전송할 수 있습니다.](../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/tile-sampler/tile-sampler.md)! 모든 공유 매개 변수가 로드됩니다. 일치는 식별자와 유형에서 발생합니다.

![포함된 사전 설정 편집](parameter-presets.resources/parameter-presets-02.gif "포함된 사전 설정 편집"){width="512px"}

## 포함된 사전 설정

포함된 사전 설정은 외부 사전 설정과 다르게 작동합니다. 이러한 기능의 주요 장점은 SBS 또는 SBSAR 파일 내에 포함되어 있어 Substance Painter, Maya 및 3DS Max(현재 Substance 3D Sampler, UE4 및 Unity에서는 사용할 수 없음)에서 쉽게 전송하고 로드할 수 있다는 것입니다. 사용자가 SBSPRS 파일을 가지고 이리저리 작업할 필요도 없습니다.

노드 및 그래프 간에 전송할 수 없습니다(이 경우 [외부 사전 설정]을 사용해야 함). 또한 이 매개 변수는 그래프 속성의 입력 매개 변수에 대해서만 만들 수 있으며 미리 보기 모드에 있는 경우에만 만들 수 있습니다.

워크플로우는 다음과 같습니다.

1. <b>입력 매개 변수</b>에 대한 <b>미리 보기 모드</b>(으)로 전환
1. 원하는 결과로 값 설정
1. 사전 설정 드롭다운 옆에 있는 <b>+</b>을 클릭하여 새로 포함된 사전 설정을 만들면 사전 설정이 즉시 생성되어 저장됩니다

포함된 사전 설정은 이름을 바꿀 수 있지만 나중에 수정할 수는 없습니다. 수정 및 제거는 드롭다운 옆에 있는 톱니바퀴 아이콘과 + 아이콘을 클릭하여 이루어집니다. 사전 설정 옆에 있는 빼기 기호를 눌러 제거합니다.

사전 설정을 활성화하기 위해 더 이상 할 필요가 없습니다. SBSAR로 게시되면 가져오기 후 사전 설정을 Substance Painter에서 사용할 수 있습니다.

>[!IMPORTANT]
>
> [직접 편집](../../../interface/preferences-window/preferences-window.md)을 사용하는 경우 <b>사전 설정</b> 탭을 사용할 수 없습니다.
