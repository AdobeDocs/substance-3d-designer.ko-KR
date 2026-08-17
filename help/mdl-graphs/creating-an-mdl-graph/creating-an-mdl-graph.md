---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/mdl-graphs/creating-an-mdl-graph.html"
breadcrumb-title: ''
description: Substance 3D Designer에서 재질 정의 언어 그래프를 만들어 사용자 정의 재질을 만드는 방법을 알아봅니다.
helpx_creative_field: ""
helpx_description: Designer > MDL graphs > Creating an MDL graph
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: MDL 그래프 만들기
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '588'
ht-degree: 0%

---


# MDL 그래프 만들기

이 페이지에서는 Substance 3D Designer에서 MDL 재질을 제작하기 위해 MDL 그래프를 만드는 과정을 설명합니다.

![MDL 그래프 생성 경로](../../assets/mdl-new-graph-hl.png "MDL 그래프 생성 경로")

*Designer 인터페이스에서 새 MDL 그래프를 만드는 경로*

## MDL 그래프를 만드는 방법

다음 방법 중 하나를 사용하여 MDL 그래프를 생성할 수 있습니다.

* *기본 메뉴 막대*&#x200B;에서 **파일 > 새로 만들기 > MDL 그래프** 옵션을 선택합니다.
* *기본 도구 모음*&#x200B;에서 ![](../../assets/mdl-new-graph-icon.png) **MDL 그래프 추가** 단추를 클릭합니다.
* **탐색기** 패널에서 *기존 패키지*&#x200B;를 마우스 오른쪽 단추로 클릭하고 **새로 만들기 > MDL 그래프** 옵션을 선택합니다.

**새 MDL 그래프** 대화 상자가 표시됩니다(아래 참조).

![새 MDL 그래프 대화 상자](../../assets/mdl-templates.png "새 MDL 그래프 대화 상자")

*새 MDL 그래프 대화 상자*

## 새 MDL 그래프 대화 상자

새 MDL 그래프를 만드는 데 사용된 방법에 관계없이 항상 <b>새 MDL 그래프</b> 대화 상자를 통해 새 그래프를 구성할 수 있습니다.

### 템플릿

<b> 템플릿</b> 섹션에서 그래프 템플릿을 선택할 수 있습니다. 그래프 템플릿에는 미리 구성된 노드가 포함되어 있으므로 그래프를 더 빠르게 시작할 수 있습니다. 사전 구성된 노드에는 출력 노드, 이러한 출력에 값을 전달하는 단순 노드(예: 균일 색상) 및 템플릿에 따른 입력 노드 등이 포함됩니다.

완전한 *공백* 그래프에서 시작하려면 <b>비어 있음</b> 템플릿을 선택하십시오.

<b>프로젝트</b> 옵션을 사용하면 프로젝트 파일별로 템플릿 목록을 필터링할 수 있습니다. 이렇게 하면 프로젝트 파일에 대한 프로젝트 설정의 <b>일반</b> 섹션 아래에 추가된 위치에서 사용자 지정 템플릿을 쉽게 찾을 수 있습니다.

>[!WARNING]
>
> 잘못된 템플릿을 선택하면 그래프를 만든 후 다른 템플릿으로 전환할 수 *없습니다*.\
> 기존 그래프를 다른 템플릿에 연결하려면 적절한 템플릿을 사용하여 새 그래프를 만들고 새 그래프에 그래프를 복사하여 붙여넣을 수 있습니다. [루트](../../mdl-graphs/main-mdl-graph-concepts/main-mdl-graph-concepts.md) 노드를 포함하여 적절한 노드를 다시 연결하십시오.

템플릿 목록은 **프로젝트** 콤보 상자 옆에 있는 *단추*&#x200B;를 사용하여 다른 모드로 표시할 수 있습니다.

* **![](../../assets/mdl-template-recent-icon.png)최근에 사용한 표시**: *최근 항목에서 최근 항목* 순으로 마지막으로 사용한 템플릿이 표시되도록 목록을 필터링합니다. 최상위 항목은 최근 항목입니다.
* **![](../../assets/mdl-template-graphs-icon.png)그래프 표시**: 템플릿은 *레이블 전용*&#x200B;으로 표시됩니다. 템플릿 디렉터리의 [Substance 3D](https://www.adobe.com/products/substance3d/3d-augmented-reality.html) 파일 순서대로 표시됩니다.
* **![](../../assets/mdl-template-packages-icon.png)Substance 3D 파일 표시**: 템플릿은 해당 레이블에 따라 템플릿 디렉터리의 파일 순서대로 *해당 템플릿이 속한 Substance 3D 파일의 하위 항목*&#x200B;으로 표시됩니다.
* **![](../../assets/mdl-template-directory-icon.png)표시 디렉터리**: 템플릿은 해당 레이블에 의해 템플릿의 디렉터리에 있는 파일 순서대로 *자신이 속한 디렉터리의 자식*(으)로 표시됩니다.

### 속성

<b>그래프 속성 </b> 섹션에서 새 그래프에 대한 기본 정보를 설정할 수 있습니다. 이 중 어느 것이든 나중에 언제든지 변경할 수 있지만, 처음에는 주의를 기울이고 사용 사례에 맞게 설정하는 것이 합리적입니다.

* <b>그래프 이름</b>: 그래프의 식별자입니다. 지정된 패키지에 대해 고유해야 하며 공백 및 일부 특수 문자는 포함할 수 없습니다.
* <b>패키지에서 그래프 만들기</b>: 이 콤보 상자를 사용하여 새 그래프에 대한 *새*&#x200B;패키지를 만들거나 탐색기 패널에 이미 로드된 *기존* 패키지에 새 그래프를 추가할 수 있습니다.\
  참고: <b>4</b> 메서드를 사용하여 만들기 프로세스를 시작하는 경우(위 참조) 이 매개 변수는 프로세스가 시작된 기존 패키지에 대한 *사전 설정*&#x200B;입니다.
* <b>템플릿 세부 사항</b>: 이 섹션에서는 템플릿의 특성과 목적을 설명하는 짧은 텍스트를 제공합니다.
