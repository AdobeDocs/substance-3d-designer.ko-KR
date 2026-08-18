---
helpx_url: "https://helpx.adobe.com/kr/substance-3d-designer/interface/the-library/managing-custom-content-and-filters.html"
breadcrumb-title: ''
description: 체계적인 에셋 액세스를 위해 Substance 3D Designer Library에서 사용자 정의 콘텐츠 및 필터를 관리하는 방법을 알아보십시오.
helpx_creative_field: ""
helpx_description: Designer > Interface > The Library > Managing custom content and filters
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 사용자 정의 컨텐츠 및 필터 관리
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0b8b2d2c05587d7fe84a71bb54244a492540d6dc
workflow-type: tm+mt
source-wordcount: '912'
ht-degree: 0%

---


# 사용자 정의 컨텐츠 및 필터 관리

이 페이지에서는 라이브러리에서 사용자 정의 콘텐츠를 관리하기 위한 범주와 필터를 만드는 방법에 대해 설명합니다. 또한 프로젝트 기반 워크플로우에 대한 제안도 포함되어 있습니다.

## 개요

[라이브러리에 사용자 지정 콘텐츠를 추가](../../../interface/preferences-window/project-settings/project-settings.md)한 후에는 *검색 가능*&#x200B;해야 합니다.

라이브러리는 콘텐츠를 필터링하고 검색에 표시할 목적으로 콘텐츠를 식별하는 데 *데이터 요소*&#x200B;를 사용합니다. 이러한 데이터 포인트는 다음과 같습니다.

* 이름
* 확장
* URL(예: *파일 이름*)
* 특성

<b>라이브러리</b>를 특정 필터가 포함된 범주로 구성하고 프로젝트의 요구 사항에 맞게 조정할 수 있습니다.\
실제로 사용자 지정 범주 및 필터는 *프로젝트별*&#x200B;일 수 있으며 [프로젝트 파일](../../../interface/preferences-window/project-settings/project-settings.md)(\*.sbsprj)에 저장될 수 있습니다. 그런 다음 이러한 파일을 [구성 파일](../../../interface/preferences-window/project-settings/project-settings.md)(\*.sbscfg)로 취합하고 팀에 배포하여 아티스트가 주어진 프로젝트에 대해 모두*&#x200B;동일한 <b>라이브러리</b> 범주*를 사용할 수 있도록 합니다.

즉, 하나 이상의 프로젝트 파일을 사용하여 <b>라이브러리</b>에 콘텐츠를 추가해야 하는 폴더와 해당 콘텐츠를 정렬하고 구성하는 범주 및 필터를 설정할 수 있습니다.

![라이브러리의 사용자 지정 콘텐츠](../../../assets/library-filters.png "라이브러리의 사용자 지정 콘텐츠")

## 그래프 특성

그래프 속성의 [특성](../../../compositing-graphs/graph-parameters/graph-parameters.md) 섹션에 있는 데이터 집합을 사용하여 [SBS](../../../getting-started/overview/overview.md) 및 [SBSAR](../../../getting-started/overview/overview.md) 파일에 포함된 그래프를 라이브러리에서 *필터링 및 검색*&#x200B;할 수 있습니다. 이러한 특성 중 일부는 다른 [리소스 형식](../../../resources/resources.md)에도 설정할 수 있습니다.

## 사용자 정의 필터 및 폴더

필터는 단순 부울(True/False) 검색 매개 변수로, <b>Filter</b>을(를) 선택하면 라이브러리 내에 리소스가 표시됩니다. 리소스는 패키지 내에 보관된 모든 것일 수 있습니다. 다음 사항에 유의하십시오.

* <b>필터</b>는 *모든 시청 경로*&#x200B;의 모든 리소스와 일치합니다.
* <b>필터</b>에는 여러 조건이 포함될 수 있습니다. *이러한 조건은 모두 해당 필터 아래에 표시할 리소스의 True*(AND 조건)로 평가되어야 합니다.
* [리소스](../../../resources/resources.md)가 여러 필터 아래에 표시될 수 있습니다. 모든 필터에 대해 *배타적이지 않습니다*.
* <b>검색</b> 기능을 사용하여 <b>필터</b>에서 *지원되지*&#x200B;하더라도 감시 경로의 [리소스](../../../resources/resources.md)는 <b>라이브러리</b>에서 *계속 사용 가능*&#x200B;합니다.

### 필터 및 폴더를 만드는 방법

범주(폴더) 및 필터는 다음 단추를 사용하여 만들고 편집합니다.

<b>![](../../../assets/library-icon-new-folder.png) 폴더 추가:</b> 라이브러리 보기에서 확장 가능한 폴더를 만듭니다. 하위 폴더를 만들 수 *없습니다*.

<b>![](../../../assets/library-icon-new-filter.png) 필터 추가:</b> 선택한 폴더 내에 새 필터를 추가합니다. 기존 기본 폴더에 필터를 추가할 수 *없습니다*.

<b>![](../../../assets/library-icon-edit.png) 항목 편집:</b> 현재 선택한 폴더 또는 필터를 편집합니다. 기본 폴더 및 필터의 속성은 *편집할 수 없습니다*.

폴더 또는 필터를 *제거*&#x200B;하려면 해당 폴더 또는 필터를 *마우스 오른쪽 단추로 클릭*&#x200B;하고 상황에 맞는 메뉴에서 <b>제거</b> 옵션을 선택합니다.

### 필터 및 폴더 편집

<b>폴더</b> 및 <b>필터</b>는 다음 데이터로 식별됩니다.

* 라이브러리 트리 보기에 표시된 <b>이름</b>
* 이 항목이 저장된 [SBSPRJ(프로젝트 구성 파일)](../../../pipeline-and-project-con/project-configuration-fil/project-configuration-files-sbsprj.md).

>[!WARNING]
>
> *올바른 프로젝트*&#x200B;를 편집하기 위해 이러한 설정을 올바르게 설정하는 것이 *매우*&#x200B;중요합니다!

![사용자 지정 필터 버전](../../../assets/library-filters-edit.png "사용자 지정 필터 버전")

**필터**&#x200B;의 필터링 목적을 달성하려면 일반적으로 *조건*&#x200B;을 설정해야 합니다. 이러한 조건은 다음 기준을 사용하여 구성됩니다.

* **리소스 유형**: [그래프](../../../compositing-graphs/substance-compositing-graphs.md)와 같은 특정 [리소스 유형](../../../resources/resources.md)을 설정합니다.
* 조건을 적용할 **특성** - 위 목록 참조
* **조건 논리**: 필터에 양수, 음수, 부분 및 전체 일치의 결과를 포함하도록 합니다.
* **조건 키워드:** **특성** 및 **조건 논리** 조건을 테스트하는 문자열입니다. 비워 두면 이 두 가지 조건과 일치하는 모든 리소스가 포함됩니다

Condition 키워드 맨 오른쪽에 있는 &#39;**+**&#39; 및 &#39;**x**&#39; 단추를 사용하여 *조건을 추가 또는 제거*&#x200B;할 수 있습니다.

>[!NOTE]
>
> 조건을 설정하지 않은 필터를 사용하면 *모두* **라이브러리** 콘텐츠가 표시됩니다.

## 모범 사례

### 권장 지침

* 기본 라이브러리에 대한 일반 규칙은 <b>폴더</b>가 <b>범주</b> 특성에 나열되는 반면 <b>필터</b> 이름은 <b>태그</b> 특성에 의해 결정됩니다
* *명시적으로*&#x200B;하려는 경우를 제외하고 기본 라이브러리와 혼합되는 사용자 지정 노드를 만들지 마십시오. 일치하는 경우 노드 *will*&#x200B;이(가) 기본 필터 아래에 표시되므로 이를 방지하려면 *다른 태그 지정/이름 지정 시스템*&#x200B;을 사용해야 합니다
* *고유*, *프로젝트당* 식별자를 사용하십시오. 모든 프로젝트에서 *일관성*&#x200B;을 유지하는 한 <b>설명</b>, <b>범주</b> 또는 <b>사용자 데이터</b>와 같이 원하는 위치에 배치할 수 있습니다. 이렇게 하면 *프로젝트별* 콘텐츠를 훨씬 쉽게 검색하고 필터링할 수 있습니다.
* <b>작성자</b> 특성을 사용하여 버전 제어 레코드를 뒤질 필요 없이 콘텐츠를 처음 담당하는 사람을 추적합니다
* <b>아이콘</b>을 효율적으로 만드는 방법은 그래프 특성 [아이콘](../../../compositing-graphs/graph-parameters/graph-parameters.md)의 <b>생성</b> 옵션을 사용하거나 그래프 [템플릿](../../../interface/preferences-window/project-settings/project-settings.md)을 만들어 생성하는 것입니다. 이렇게 하면 일관성을 보장하고 파일 작성 작업을 저장할 수 있습니다. 모든 기본 라이브러리 아이콘은 이러한 방식으로 Designer 내에서 만들어졌습니다.

### 다양한 범위의 컨텐츠 관리

* *기존 범주*&#x200B;에 리소스를 추가할 수 있습니다. 필터를 관리하고 유지 관리하는 작업이 줄어들며, 특수 아이콘 스타일을 사용하여 *구별하기*&#x200B;할 수 있습니다.
* *전역*(스튜디오 수준) [프로젝트 구성 파일](../../../pipeline-and-project-con/project-configuration-fil/project-configuration-files-sbsprj.md)에서 폴더 및 필터를 정의한 다음 *연속* [프로젝트 파일](../../../interface/preferences-window/project-settings/project-settings.md)에서 시청 경로를 추가하여 콘텐츠를 추가할 수 있습니다.
* *각 프로젝트*&#x200B;에 대한 특정 폴더 및 필터를 정의하여 별도로 유지할 수 있습니다.
* 기존 필터를 사용하고, 새 전역 필터를 정의하고, 프로젝트별로 고유한 필터를 만드는 방법 등 위의 세 가지 방법을 모두 혼합하여 사용할 수 있습니다
