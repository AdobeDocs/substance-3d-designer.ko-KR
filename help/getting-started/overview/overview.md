---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/getting-started/overview.html"
breadcrumb-title: ''
description: Substance 3D Designer에 대한 개요를 보고 절차 자료 및 텍스처를 만들기 위한 기능에 대해 알아보십시오.
helpx_creative_field: ""
helpx_description: Designer > Getting started > Overview
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 개요
user-guide-description: ''
user-guide-title: ''
source-git-commit: f320cf6842ff56ac24912ceda264f30c28317c05
workflow-type: tm+mt
source-wordcount: '970'
ht-degree: 2%

---


# 개요

[Substance 3D Designer](https://www.adobe.com/kr/products/substance3d-designer.html)은 노드 기반의 인터페이스에서 2D 텍스처, 재질 및 필터를 만들기 위한 응용 프로그램이며 절차적 생성, 매개변수화 및 비파괴적 워크플로에 중점을 둡니다. Substance 3D 생태계에서 가장 오래 실행되는 애플리케이션이며, 이를 통해 만들어진 리소스는 가장 다재다능하고 역동적입니다.

다른 애플리케이션과 비교한 내용은 다음과 같습니다.

|  | <div><img alt="Substance 3D Sampler 아이콘" class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid_items_grid-cell_position-par_dx_table_row-r0-column-c1_position_position-par_image_713298714" src="../../assets/sa-appicon-noshadow-256.png" title="Substance 3D Sampler 아이콘" width="64px"/></div>  Substance 3D Sampler | <div><img alt="Substance 3D Painter 아이콘" class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid_items_grid-cell_position-par_dx_table_row-r0-column-c2_position_position-par_image" src="../../assets/pt-appicon-noshadow-256.png" width="64px"/></div>  Substance 3D Painter | <div><img alt="Substance 3D Designer 아이콘" class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid_items_grid-cell_position-par_dx_table_row-r0-column-c3_position_position-par_image" src="../../assets/ds-appicon-noshadow-256.png" title="Substance 3D Designer 아이콘" width="64px"/></div>  Substance 3D Designer |
| --- | --- | --- | --- |
| <b>학습 곡선</b> | 저 | 중 | 높음 |
| <b>작성자 자료</b> | 예 | 예 | 예 |
| <b>3D 모델 작성</b> | 아니요 | 제한\* | 제한\* |
| <b>작성자 필터, 패턴 및 효과</b> | 아니요 | 제한됨 | 예 |
| <b>파라메트릭 콘텐츠 내보내기</b> | 아니요 | 아니요 | 예 |

\*: 변위 전용입니다. [3D 보기](../../interface/3d-view/3d-view.md) 섹션의 <b>장면 내보내기</b> 기능을 확인하세요.

요컨대, Substance 3D Designer은 사용 가능한 가장 기술적이고 진보된 텍스처링 애플리케이션으로 간주되어야 합니다.

거의 모든 사용 사례 또는 시나리오에 대한 콘텐츠를 작성할 수 있습니다. 이는 UV 매핑된 메쉬의 고유한 재질/텍스처 세트와 같은 단일 출력 유형에 제한되지 않지만 훨씬 더 확장된 사용 세트를 위한 콘텐츠를 만들 수 있음을 의미합니다.

예를 들어 Painter 및 Sampler에서 대부분의 절차적 스마트 콘텐츠는 Designer에서 제작되고 내보내졌습니다. 브러시 Alpha, 생성기, 필터 및 기본 재질과 같은 기능은 모두 Designer에서 작성할 수 있습니다.

## 워크플로

Substance 3D Designer은 노드 기반의 편집기로 다양한 복잡성으로 다양한 방식으로 콘텐츠를 제작할 수 있습니다. [워크플로는 전용 페이지](../../getting-started/workflow-overview/workflow-overview.md)에서 자세히 설명되지만, 다음은 소프트웨어를 사용하여 작업할 때의 이점입니다.

<b>[비선형](../../compositing-graphs/substance-compositing-graphs.md) </b>: 한 번에 많은 텍스처 출력을 만들 수 있습니다. 하나의 마스크 또는 슬라이더를 편집하면 연결된 출력이 자동으로 다시 계산됩니다. 이제 [기본 색상], [거칠음], [표준] 등의 지도를 별도로 작성할 필요가 없습니다.

<b> [비파괴](../../compositing-graphs/compositing-graph-key-con/substance-compositing-graph-key-concepts.md) </b>: 작업을 손실하지 않고 *작업을 되돌릴 수 있습니다*. 반복과 실험이 훨씬 빨라져 작업 과정이 훨씬 더 효율적이 됩니다.

<b> [Integrated Baking](../../bakers/bakers.md) </b>: 소프트웨어 내부에서 바로 매우 빠른 고급 메시 베이킹 도구에 액세스합니다. 더 이상 별도의 소프트웨어에서 베이크를 수행하지 않아도 되며 긴 가져오기 및 내보내기 프로세스를 수행할 필요가 없습니다.

<b> [파라메트릭](../../compositing-graphs/manage-parameters/exposing-a-parameter/exposing-a-parameter.md) </b>: 단일 슬라이더 또는 드롭다운을 통해 텍스처의 거의 모든 측면을 제어하도록 설정할 수 있습니다. 이를 통해 하나의 에셋에 무한한 컨트롤과 변형을 추가할 수 있습니다.

## 파일 유형

응용 프로그램과 해당 에코시스템은 4개의 다른 파일 유형을 사용합니다. 명확히 하자면, 이 파일 유형은 <b>Substance 3D Designer에서 내보내</b>며 일부 또는 다른 모든 Substance 3D 응용 프로그램으로 가져올 수 있는 파일 유형입니다.

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../assets/ds-sbs-48.png)

### Substance 3D 파일

*(\*.SBS)*

Substance 파일은 Designer의 **기본 소스 파일**&#x200B;입니다. Substance 파일을 열면 **그래프의 모든 노드를 보고 편집**&#x200B;할 수 있습니다. 그래프, 함수, 비트맵, 메시 등과 같은 다양한 리소스를 포함할 수 있는 패키지로 표시됩니다. 그것들은 공유하기가 더 어렵고 계산하기가 더 빠릅니다. Substance 3D Designer 및 Substance Player에서만 열 수 있습니다.

</td>
<td style="border: 0;" valign="top">

![](../../assets/sbsar-48.png)

### Substance 3D 에셋

*(\*.SBSAR)*

Substance 아카이브는 <b>개 컴파일되고 </b>개의 Substance 파일이 최적화되었습니다. 계산 속도가 훨씬 빠르며 참조 문제 없이 쉽게 공유할 수 있습니다. 매개 변수를 계속 변경할 수 있지만 그래프를 편집하면 <b>잠김</b>됩니다. Substance 아카이브는 모든 Substance 3D 응용 프로그램과 Autodesk 3DS Max &amp; Maya, Unreal Engine 또는 Unity Engine과 같은 [Substance 3D 통합](https://experienceleague.adobe.com/en/docs/substance-3d/ecosystem/home)이 있는 모든 응용 프로그램(일부는 외부 플러그인과 함께)에서 사용할 수 있습니다.

</td>
<td style="border: 0;" valign="top">

![](../../assets/bmp-96.png){width="48px"}

### 정적 파일

*(\*.TGA, \*.BMP, \*.PNG, \*.FBX, \*.OBJ 등)*

Substance 3D Designer은 항상 정적 파일 형식으로 내보내기를 지원합니다. 2D 이미지는 비트맵 파일로 내보낼 수 있고 3D 모델은 일반적인 3D 파일 유형으로 내보낼 수 있습니다. 정적 파일로 내보낼 때 **모든 동적 기능이 손실됩니다**. 이미지는 해상도에서 잠겨 있고 3D 모델은 polycount에서 잠겨 있습니다.

</td>
</tr>
</table>

이는 일반적으로 Designer 내에서 작업할 때 작업을 SBS 형식으로 유지한다는 것을 의미하며 대상이 이를 지원하는 경우 SBSAR로 내보내고(예: Painter), SBSAR을 지원하지 않거나 지원하지 않는 경우 정적 비트맵 파일을 사용합니다.

## 리소스 유형

Substance 3D 파일에는 다양한 용도로 사용되는 다양한 리소스가 포함될 수 있습니다. 일부 리소스는 Designer 내부에서만 작성할 수 있으며, 일부는 외부 애플리케이션에서 가져옵니다.

<table>
<tr style="border: 0;">
<td width="16.67%" style="border: 0;" valign="top">

[![](../../assets/graph-5.png){width="150px"}](../../compositing-graphs/substance-compositing-graphs.md)

</td>
<td width="100.00%" style="border: 0;" valign="top">

### Substance 그래프

Substance 그래프를 사용하면 *2D 이미지 데이터*&#x200B;를 생성 및 처리한 다음 하나 이상의 텍스처 출력으로 출력할 수 있습니다. 대부분의 사용 사례에서 프로젝트는 하나 이상의 Substance 그래프를 중심으로 회전합니다.

[Substance 그래프 전용 섹션으로 이동합니다.](../../compositing-graphs/substance-compositing-graphs.md)

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td width="16.67%" style="border: 0;" valign="top">

[![](../../assets/function-1.png){width="150px"}](../../function-graphs/function-graphs.md)

</td>
<td width="100.00%" style="border: 0;" valign="top">

### Substance 함수 그래프

<b>함수</b>는 더 높은 수준의 추상화와 복잡성입니다. 이미지 데이터(픽셀 값 집합)를 처리하는 대신 *단일 값 처리*(정수, 부동 소수점, 벡터)를 처리합니다. 함수는 보다 복잡한 연산을 수행하거나 특정 비헤이비어를 미세 조정하려는 경우에 사용됩니다. 함수는 일반적으로 독립적으로 작동하지 않으며 Substance 그래프의 컨텍스트 외부에서 사용되지 않습니다.

[Substance 함수 그래프 전용 섹션으로 이동합니다.](../../function-graphs/function-graphs.md)

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td width="16.67%" style="border: 0;" valign="top">

[![](../../assets/folder-4.png){width="150px"}](../../resources/importing-linking-and-new/importing-linking-and-new-resources.md)

</td>
<td width="100.00%" style="border: 0;" valign="top">

### 그래프가 아닌 리소스

그래프가 아닌 리소스는 외부 응용 프로그램(예: Photoshop 또는 Autodesk Maya)에서 가져올 수 있으며, *Designer 내에서 만들기*&#x200B;할 수도 있습니다. 가장 큰 차이점은 노드 기반의 그래프가 아니라는 점입니다. 대부분의 그래프는 이전에 언급된 그래프 유형 내부 또는 옆에 사용되는 요소입니다.

다음과 같은 리소스 유형이 있습니다.

* [비트맵](../../resources/bitmap-resource/bitmap-resource.md)
* [벡터 그래픽 (SVG)](../../resources/vector-graphics-svg-res/vector-graphics-svg-resource.md)
* [3D 메시 및 장면](https://helpx.adobe.com/substance-3d/unlisted/documentation/sddoc/3d-mesh-resource-200574577.html)
* [글꼴](../../resources/font-resource/font-resource.md)
* [AxF](../../resources/axf-appearance-exchange/axf-appearance-exchange-format.md)

</td>
</tr>
</table>
