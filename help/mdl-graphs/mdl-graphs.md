---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/mdl-graphs.html"
breadcrumb-title: ''
description: 고급 재질 작업 과정을 위해 Substance 3D Designer에서 [재질 정의 언어] 그래프를 만들고 사용하는 방법을 알아봅니다.
helpx_creative_field: ""
helpx_description: Designer > MDL graphs
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: MDL 그래프
user-guide-description: ''
user-guide-title: ''
source-git-commit: 4f8830fa9ab6012f0a7ba5054eb171b151c44874
workflow-type: tm+mt
source-wordcount: '757'
ht-degree: 0%

---


# MDL 그래프

이 페이지에는 Substance 3D Designer에 MDL 그래프가 표시되므로 MDL 재질을 작성하고 실시간으로 비헤이비어를 미리 볼 수 있습니다.

![말라카이트 MDL 재료](../assets/mdl-malachite-example.jpg "말라카이트 MDL 재료")

*Chrysocola, MDL 재질이 포함된 Malachite, [Mark Foreman](https://www.artstation.com/oggyart)* *[레거시 Substance share](https://share-legacy.substance3d.com/libraries/4043)* *플랫폼*&#x200B;에서 사용 가능

>[!WARNING]
> 
> MDL 그래프 및 모든 관련 기능은 버전 16.0.0에서 Designer에서 제거되었습니다.
> 
> 자세한 내용은 여기를 참조하세요. [MDL 그래프 및 수명 종료](../technical-issues/mdl-graph-iray-eol/mdl-graph-iray-eol.md)

+++목차

* [기본 MDL 그래프 개념](/help/mdl-graphs/main-mdl-graph-concepts/main-mdl-graph-concepts.md)
* [MDL 그래프 만들기](/help/mdl-graphs/creating-an-mdl-graph/creating-an-mdl-graph.md)
* [MDL 라이브러리](/help/mdl-graphs/mdl-library/mdl-library.md)
* [MDL 그래프에서 매개변수 노출](/help/mdl-graphs/exposing-parameters-mdl/exposing-parameters-in-mdl-graphs.md)
* [Substance 그래프 및 MDL 재질](/help/mdl-graphs/compositing-graphs-and/substance-compositing-graphs-and-mdl-materials.md)
* [MDL 컨텐츠 내보내기](/help/mdl-graphs/exporting-mdl-content/exporting-mdl-content.md)
* [MDL 그래프의 경고](/help/mdl-graphs/warnings-in-mdl-graphs/warnings-in-mdl-graphs.md)
* [MDL 학습 리소스](/help/mdl-graphs/mdl-learning-resources/mdl-learning-resources.md)

+++

## 개요

MDL은 [재질 정의 언어](http://www.nvidia.com/object/material-definition-language.html)의 약어입니다. &quot;물리적 기반 렌더링 솔루션을 위한 물리적 기반 재질을 정의하기 위해 [NVIDIA](https://www.nvidia.com/)에서 개발한 기술입니다.&quot; (출처: [NVIDIA MDL 설명서](https://raytracing-docs.nvidia.com/mdl/index.html))

이 언어를 사용하면 전체 재질 정의가 구현되므로 일관된 출력을 위해 응용 프로그램과 렌더러에서 사용할 수 있습니다. Substance 3D Designer은 현재 MDL 그래프에서 MDL 함수와 값 유형을 노드로 표시함으로써 MDL 재료의 그래프 기반 노드 작성을 제공하는 *전용* 애플리케이션입니다.

재질을 작성하는 동안 Designer에 포함되어 있고 [3D 보기](../interface/3d-view/3d-view.md) 패널에서 사용할 수 있는 NVIDIA의 자체 [Ray](../interface/3d-view/iray/iray.md) 렌더러를 사용하여 재질 *대화형으로* 동작을 미리 볼 수 있습니다.

MDL 그래프는 [Substance 그래프](../compositing-graphs/substance-compositing-graphs.md)와 보완되는데, 후자의 출력 *텍스처*&#x200B;는 MDL 재질에 의해 *표본*&#x200B;될 수 있으므로 그 비헤이비어와 모양에 영향을 줄 수 있습니다.

아래 MDL 그래프 리소스의 속성부터 시작하여 안내 학습 경로를 위해 이 문서의 섹션을 *순서대로* 살펴보는 것이 좋습니다.\
뛰어들고 싶으신가요? MDL 학습 리소스 섹션에서 MDL 그래프를 시작합니다!

>[!NOTE]
>
> NVIDIA에서 제작하고 유지 관리하는 MDL 사양 및 [MDL 핸드북](http://mdlhandbook.com/)에 대한 링크를 포함하는 [NVIDIA MDL 설명서](https://raytracing-docs.nvidia.com/mdl/index.html)에서 재료 정의 언어의 기술적 구현에 대해 자세히 알아볼 수 있습니다.

![MDL 그래프 속성](../assets/mdl-main.png "MDL 그래프 속성")

*속성 패널의 MDL 그래프 속성*

## MDL 그래프 속성

### 특성

이 섹션에서는 식별, 분류 및 저자 설정을 위한 MDL 재료에 대한 정보를 포함합니다.

* <b>식별자</b>: 이 리소스의 이름으로, 패키지의 부모 아래에서 고유해야 합니다.
* <b>표시 이름</b>: 인터페이스에 표시되는 MDL 재질 이름
* <b>아이콘</b>: Designer 라이브러리에서 이 그래프의 축소판으로 사용되는 이미지
* <b>숨김\*</b>:* True*(으)로 설정하면 MDL 재질이 MDL 라이브러리에 표시되지 않지만 내부적으로 존재하므로 참조될 수 있습니다
* <b>라이브러리에 표시</b>: *True*(으)로 설정하면 MDL 그래프가 Designer 라이브러리에 표시됩니다
* <b>설명</b>: MDL 재질에 대한 설명으로, 이 그래프를 참조하는 인스턴스 노드의 도구 설명에 표시될 수 있습니다.
* <b>범주\*</b>: MDL 그래프가 속한 범주 - 현재 Designer [라이브러리](../interface/the-library/the-library.md)에서 그래프가 정렬되는 방식에는 영향을 주지 않습니다.
* <b>그룹\*</b>: MDL 재질이 속한 라이브러리 그룹
* <b>작성자\*</b>: MDL 재질 작성자
* <b>기고자\*</b>: MDL 자료의 기고자(작성자 제외)
* <b>키워드\*</b>: 라이브러리 검색에서 MDL 재질을 찾는 데 사용할 수 있는 키워드
* <b>저작권 고지\*</b>: MDL 자료의 저작자 및 사용과 관련된 저작권 고지

참고: 별표(\*)로 표시된 속성은 MDL 라이브러리 통합에서 사용하는 MDL 주석이며 Designer에서*&#x200B;영향을 주지 않습니다*.

### 그래프 입력

이 섹션에서는 MDL 그래프의 노출된 매개 변수에 연결된 대화형 매개 변수를 나열하고 해당 *기본값*&#x200B;을 정의합니다. 언제든지 *수정* 및 *순서 변경*&#x200B;될 수 있습니다.

이러한 입력의 인터페이스 및 동작은 연결된 노출된 매개 변수의 *값 형식* 및 *범위*&#x200B;에 의해 정의됩니다. 예를 들면 다음과 같습니다.

* 소프트 범위 [0.0,4.0]으로 설정된 <b>Float</b> 유형의 노출된 값은 0.0에서 4.0 사이의 *단일 슬라이더*&#x200B;로 표시됩니다
* <b>색상</b> 유형의 노출된 값이 *색상 위젯*(선택 그레이디언트 및 색상 축소판 포함)으로 표시됩니다.

그래프 입력 순서를 변경하려면 매개 변수의 왼쪽에 있는 *어두운 핸들*&#x200B;에 커서를 놓고 *LMB</b>를 클릭한 다음* <b>LMB를 누르고 커서를 위나 아래로 드래그합니다. 이 사용자 정의 순서는 다음 컨텍스트에서 MDL 재료의 특성을 표시하는 데 사용됩니다.

* 이 재료의 MDL 그래프를 참조하는 인스턴스 노드
* [3D 보기](../interface/3d-view/3d-view.md)의 재질 속성
* 타사 MDL 통합
