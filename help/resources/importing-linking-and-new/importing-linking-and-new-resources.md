---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/resources/importing-linking-and-new-resources.html"
breadcrumb-title: ''
description: Substance 3D Designer에서 재질 프로젝트를 위한 리소스를 가져오고, 연결하고, 새 리소스를 만드는 방법을 알아봅니다.
helpx_creative_field: ""
helpx_description: Designer > Resources > Importing, linking and new resources
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 가져오기, 연결, 새 리소스
user-guide-description: ''
user-guide-title: ''
source-git-commit: 4f8830fa9ab6012f0a7ba5054eb171b151c44874
workflow-type: tm+mt
source-wordcount: '711'
ht-degree: 2%

---


# 가져오기, 연결, 새 리소스

[Substance 3D Designer](https://www.adobe.com/kr/products/substance3d-designer.html)은(는) 그래프에서 사용할 새 리소스를 가져오거나 만드는 3가지 모드를 지원합니다. 이러한 리소스는 [비트맵](../../resources/bitmap-resource/bitmap-resource.md), [벡터 그래픽](../../resources/vector-graphics-svg-res/vector-graphics-svg-resource.md), [3D 장면](../3d-scene-resource/3d-scene-resource.md) 및 [글꼴](../../resources/font-resource/font-resource.md)을(를) 포함하되 이에 국한되지 않고 다양한 유형으로 제공됩니다. 이 페이지에서는 다양한 방법과 각 방법을 가장 잘 사용하는 시기를 설명합니다.

모든 메서드는 탐색기의 패키지에서 RMB를 클릭하여 액세스합니다.

다음 표에서는 메서드 간 기능상의 차이점에 대해 간략하게 설명합니다.

|                                                                                                                                                                         | 새로 만들기 | 가져오기 | 링크 |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| 그래프([Substance 그래프](../../compositing-graphs/substance-compositing-graphs.md), [Substance 함수 그래프](../../function-graphs/function-graphs.md) | <div><img alt="(틱)" data-preserve-html="true" src="../../assets/check.svg"/></div> | <div><img alt="(오류)" data-preserve-html="true" src="../../assets/error.svg"/></div> | <div><img alt="(오류)&quot; data-preserve-html=&quot;true" src="../../assets/error.svg"/></div> |
| [비트맵](../../resources/bitmap-resource/bitmap-resource.md),[벡터 그래픽(SVG)](../../resources/vector-graphics-svg-res/vector-graphics-svg-resource.md) | <div><img alt="(틱)" data-preserve-html="true" src="../../assets/check.svg"/></div> | <div><img alt="(틱)" data-preserve-html="true" src="../../assets/check.svg"/></div> | <div><img alt="(틱)&quot; data-preserve-html=&quot;true" src="../../assets/check.svg"/></div> |
| 3D 장면, [글꼴](../../resources/font-resource/font-resource.md) | <div><img alt="(오류)" data-preserve-html="true" src="../../assets/error.svg"/></div> | <div><img alt="(오류)" data-preserve-html="true" src="../../assets/error.svg"/></div> | <div><img alt="(틱)&quot; data-preserve-html=&quot;true" src="../../assets/check.svg"/></div> |
| SBS 파일 옆에 만들어집니다. | <div><img alt="(틱)" data-preserve-html="true" src="../../assets/check.svg"/></div> | <div><img alt="(틱)" data-preserve-html="true" src="../../assets/check.svg"/></div> | <div><img alt="(오류)&quot; data-preserve-html=&quot;true" src="../../assets/error.svg"/></div> |
| Designer에서 편집 가능 | <div><img alt="(틱)" data-preserve-html="true" src="../../assets/check.svg"/></div> | <div><img alt="(틱)" data-preserve-html="true" src="../../assets/check.svg"/></div> | <div><img alt="(오류)&quot; data-preserve-html=&quot;true" src="../../assets/error.svg"/></div> |
| 외부 편집 내용이 자동으로 동기화됨 | <div><img alt="(오류)" data-preserve-html="true" src="../../assets/error.svg"/></div> | <div><img alt="(오류)" data-preserve-html="true" src="../../assets/error.svg"/></div> | <div><img alt="(틱)&quot; data-preserve-html=&quot;true" src="../../assets/check.svg"/></div> |
| 게시된 SBSAR에 포함됨 | <div><img alt="(틱)" data-preserve-html="true" src="../../assets/check.svg"/></div> | <div><img alt="(틱)" data-preserve-html="true" src="../../assets/check.svg"/></div> | <div><img alt="(틱)&quot; data-preserve-html=&quot;true" src="../../assets/check.svg"/></div> |

## 새 리소스

새 리소스를 작성하면 패키지의 리소스가 처음부터 작성됩니다. 모든 Designer 전용 리소스(예: Substance 그래프 및 Substance 함수 그래프)는 이러한 방식으로만 만들 수 있습니다.

특별한 경우는 새 [비트맵](../../resources/bitmap-resource/bitmap-resource.md)또는 [SVG](../../resources/vector-graphics-svg-res/vector-graphics-svg-resource.md)을 만들 때입니다. 이러한 파일은 탐색기에 표시되며 가져온 리소스처럼 작동하지만 외부 파일은 필요하지 않습니다. Designer에서 수정할 수 있습니다. 이렇게 만든 새 비트맵과 SVG은 빠르고 단순한 벡터 모양이나 단순하게 칠해진 2D 비트맵 마스크와 같이 외부 편집기에 의존할 필요가 없는 경우에도 유용합니다.

## 가져온 리소스

리소스를 가져오면 SBS 파일(*Graphname*.resources 폴더에서) 옆에 SVG 파일을 제외한 [개의 리소스 파일 중복이 만들어집니다](../../resources/vector-graphics-svg-res/vector-graphics-svg-resource.md). 리소스 &#39;포함&#39;이라고도 합니다.

그런 다음 그래프에 배치되면 [2D 보기](../../interface/2d-view/2d-view.md)에서 [비트맵 페인팅 도구](../../resources/bitmap-resource/bitmap-painting-tools/bitmap-painting-tools.md) 또는 [벡터 편집 도구](../../resources/vector-graphics-svg-res/vector-editing-tools/vector-editing-tools.md)를 사용하여 가져온 리소스를 Designer에서 편집할 수 있습니다. 가져온 리소스는 더 이상 원본 소스 파일에 연결되지 않습니다. 즉, 처음 가져온 파일을 변경, 제거 또는 업데이트하면 Designer의 리소스에는 영향을 주지 않습니다.

[AxF 파일](../../resources/axf-appearance-exchange/axf-appearance-exchange-format.md)의 경우 프로세스가 좀 더 복잡합니다. Substance 그래프와 비트맵 리소스는 AxF 패키지에서 생성됩니다. 그러나 이러한 모든 편집자는 해당 편집자(그래프 보기 또는 2D 보기)에서 편집할 수 있습니다.

>[!WARNING]
>
> 새 패키지의 경우 패키지를 저장할 때까지 가져온 리소스 및 새 리소스가 디스크에 저장되지 않습니다.

## 연결된 리소스

리소스를 연결하면 Designer이 디스크의 원래 위치에서 소스 파일을 참조하지만, 패키지의 일부처럼 탐색기에 계속 표시함을 의미합니다. Designer 내에서 직접 실제 리소스를 편집할 수는 없으며 그래프의 구성 요소나 맵 제빵의 소스로만 사용할 수 있습니다.

Designer에서 동시에 작업하는 동안 외부 편집기를 사용하여 리소스를 업데이트해야 한다는 점을 알고 있는 경우 연결하는 것이 이상적입니다. 제빵용 맵이 좋은 예입니다. 외부 제빵용 애플리케이션에서 Designer 참조 비트맵을 사용하면 이러한 파일이 변경되자마자 자동으로 그래프를 다시 로드하고 업데이트할 수 있습니다. 마찬가지로, 3D 장면은 연결만 할 수 있으므로 3D 애플리케이션에서 새 FBX 파일을 내보낼 때마다 Designer에서 3D 보기에 사용되는 메시를 자동으로 업데이트합니다. 이 메쉬에서 맵을 굽는 경우 RMB를 클릭하고 &#39;모든 베이킹된 맵 새로 고침&#39;을 선택하여 굽는 과정을 수동으로 시작해야 합니다.

## 리소스 삭제

패키지에서 리소스를 삭제할 때 <b>항목 제거 확인</b> 대화 상자가 표시됩니다. [Substance 그래프](../../compositing-graphs/substance-compositing-graphs.md)에 사용된 [그래프 인스턴스](../../compositing-graphs/creating-compositing-gra/graph-instances-sub-gra/graph-instances-sub-graphs.md) 및 [비트맵 리소스](../../resources/bitmap-resource/bitmap-resource.md)와 같은 *다른 리소스에서 참조하는 항목*&#x200B;이 제거되는 과정의 항목인 경우 대화 상자에 이러한 항목의 *경고 및 목록*&#x200B;이 포함됩니다.

>[!NOTE]
>
> 이러한 항목에 주의하고 *깨진 종속성을 예상*&#x200B;하는 데 필요한 작업을 수행하는 것이 좋습니다. 이는 패키지에서 항목을 삭제했을 때 발생할 수 있습니다.\
> 이러한 작업에는 삭제 전에 이러한 리소스의 *모든 사용을 제거*&#x200B;하는 작업이 포함될 수 있습니다.

![&#39;사용 중인 삭제된 리소스&#39; 경고](../../assets/confirm-item-removal.png "&#39;사용 중인 삭제된 리소스&#39; 경고"){width="512px"}
