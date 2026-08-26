---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/mdl-graphs/main-mdl-graph-concepts.html"
breadcrumb-title: ''
description: Substance 3D Designer에서 재질 제작을 위한 재질 정의 언어 그래프의 주요 개념에 대해 알아봅니다.
helpx_creative_field: ""
helpx_description: Designer > MDL graphs > Main MDL graph concepts
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 기본 MDL 그래프 개념
user-guide-description: ''
user-guide-title: ''
source-git-commit: 4f8830fa9ab6012f0a7ba5054eb171b151c44874
workflow-type: tm+mt
source-wordcount: '1033'
ht-degree: 0%

---


# 기본 MDL 그래프 개념

이 페이지에는 *특정*~[MDL 그래프](../../mdl-graphs/mdl-graphs.md)인 기본 개념이 표시되며, Substance 3D Designer에서 이 그래프 유형을 최대한 활용하려면 잘 이해해야 합니다.

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

## Iray

MDL 재질은 Designer에 포함된 [Ray](../../interface/3d-view/iray/iray.md) 렌더러가 지원하는 물리적 기반 렌더링 솔루션에 대한 설명을 사용합니다. 따라서 MDL 그래프 *의 결과를 표시하려면 활성 [3D 보기](../../interface/3d-view/3d-view.md) 패널에서 Ray 렌더러*&#x200B;를 선택해야 합니다.

</td>
<td style="border: 0;" valign="top">

[![NVIDIA Ray 로고](../../assets/iray-logo.jpg)](https://www.nvidia.com/en-us/design-visualization/iray/)

</td>
</tr>
</table>

MDL 그래프를 만들거나 로드할 때 Designer에서 찾은 첫 번째 [고정 해제](../../interface/customizing-your-wor/customizing-your-workspace.md) 3D 보기 패널이 [Ray](../../interface/3d-view/iray/iray.md) 렌더러로 *자동으로 전환*&#x200B;됩니다. 3D 보기를 사용할 수 없는 경우 *새* 3D 보기 패널이 만들어지고 Ray 렌더러로 전환되어 편집 중인 MDL 재질의 렌더링을 호스팅합니다.

3D 보기 패널에서 Ray 렌더러를 선택한 경우 해당 패널의 재질 메뉴를 통해 사용 가능한 MDL 재질 간을 전환할 수 있습니다. 이 머티리에는 탐색기 패널에서 로드한 재질과 Designer의 MDL 라이브러리에 있는 재질이 포함됩니다. 이 설명서의 [Iray](../../interface/3d-view/iray/iray.md) 섹션에서 Iray의 MDL 재질 작업에 대해 자세히 알아보십시오.

## 루트 노드

MDL 그래프의 결과는 <b>루트</b> 노드로 정의됩니다. 그래프의 모든 노드는 <b>재질</b> 유형의 출력 데이터, 즉 *재질 정의*&#x200B;이면 루트로 설정할 수 있습니다. MDL 그래프에는 *하나* 루트 노드만 있을 수 있습니다.

일반적으로 Root로 설정할 수 있는 노드에는 이미 *입력*&#x200B;에 데이터를 전달하여 사용자 지정할 수 있는 재질 정의가 포함되어 있으므로 *자급자족*&#x200B;이 될 수 있습니다.\
예를 들어 유리 같은 재질을 작업하려면 유리 재질 정의를 루트 노드로 시작점으로 사용할 수 있지만 *필수 사항이 아님*&#x200B;입니다. MDL 노드의 광범위한 목록을 사용하여 복합 재료로 변환될 수 있는 많은 재료 노드가 템플릿화됩니다.

루트 노드는 현재 출력의 미리보기를 표시하는 썸네일을 포함한다.

![MDL 그래프의 루트 노드](../../assets/mdl-root-hl.png "MDL 그래프의 루트 노드")

*MDL 그래프의 루트 노드 및 해당 속성이 [속성](../../interface/properties/properties.md)* *패널*&#x200B;에 표시됨

## 커넥터 및 유형

Designer의 다른 그래프보다 MDL 그래프에 데이터 유형이 훨씬 많으므로 노드 커넥터의 고유한 모양이 나타날 수 있습니다. 이해해야 할 중요한 개념은 아래에 나열되어 있습니다.

커넥터 모양

*커넥터 모양*&#x200B;은 데이터 형식이 *균일*(원)인지 *가변*(정사각형)인지를 나타냅니다.

&quot;균일 유형의 변수는 균일 값으로만 설정할 수 있습니다. 가변 유형의 변수는 가변 값뿐만 아니라 균일 값으로 설정될 수 있다. 그러면 변수의 결과 값은 항상 변화하는 것으로 간주됩니다.&quot; (출처: [MDL 사양](https://raytracing-docs.nvidia.com/mdl/specification/MDL_spec_1.7.2_17Jan2022.pdf)의 섹션 6.3)

다음은 몇 가지 예입니다.

* 값이 샘플 픽셀의 영향을 받으므로 <b>텍스처</b> 샘플은 *가변*&#x200B;입니다.
* <b>색상</b> 값은 컨텍스트에 관계없이 동일하게 전달되므로 *균일*&#x200B;입니다.
* 값이 입사각의 영향을 받으므로 <b>BRDF</b>은(는) *가변*&#x200B;입니다
* <b>Float</b> 또는 <b>Boolean</b> 값은 컨텍스트에 관계없이 동일하게 전달되므로 *균일*&#x200B;입니다.

커넥터 색상

출력 커넥터에서 보내거나 입력 커넥터에서 예상되는 *데이터 형식*&#x200B;은 색상으로 구분되며 마우스로 커넥터를 마우스로 가리킬 때 식별자/레이블 뒤에 괄호 사이에 표시됩니다.

>[!WARNING]
>
> *일치하는 데이터 형식*&#x200B;에 대한 커넥터만 함께 연결할 수 있습니다. 색상 코딩의 유일한 목적은 그래프에 전달되는 데이터의 유형 및 어떤 커넥터를 연결할 수 있는지에 대한 가독성을 높이는 것입니다.

![MDL 노드 커넥터 유형](../../assets/mdl-connector-types.png "MDL 노드 커넥터 유형"){width="512px"}

*커넥터의 특성은 I/O 값 유형에 따라 다르며 I/O 식별자 뒤에 괄호로 표시됩니다.*

## 필터링된 노드 만들기

<b>라이브러리 보기</b>에서 <b>그래프 보기</b>(으)로 *노드*&#x200B;를 드래그하거나 *아무것도 선택되지 않은 상태*&#x200B;에서 <b>스페이스바</b>를 눌러 그래프 보기에서 <b>노드 메뉴</b>를 열면 그래프의 <b>라이브러리</b>의 <b>mdl</b> 범주에서 사용할 수 있는 노드를 추가할 수 있습니다. 이 경우 *필터링되지 않은* 노드 목록이 표시됩니다.

그러나 노드 메뉴의 노드 목록을 필터링하여 대상 입력 또는 출력에 대해 일치하는 데이터 유형의 노드만 표시하는 경우가 있습니다.

* 그래프 보기에서 *노드가 선택*&#x200B;되고 <b>스페이스바</b>가 눌러진 경우
* <b>LMB</b>을 클릭하고 *노드 커넥터*&#x200B;에서 링크를 길게 누른 후 *드래그*&#x200B;하는 경우

필터링에 적용된 *규칙*&#x200B;을(를) 염두에 두십시오.

* *단일* 노드가 선택되어 있을 때 <b>스페이스바</b>를 눌러 노드 메뉴가 표시되면 *첫 번째 입력*&#x200B;의 데이터 형식이 선택한 노드의 *출력* 데이터 형식과 일치하는 노드가 목록에 포함됩니다.
* *다중* 노드가 선택된 경우 <b>스페이스바</b>를 눌러 노드 메뉴가 표시되면 *첫 번째 입력*&#x200B;의 데이터 형식이 *마지막으로 선택한* 노드의 *출력* 데이터 형식과 일치하는 노드가 목록에 포함됩니다.
* *출력* 커넥터에서 *링크를 끌어서* 노드 메뉴가 표시되면 *첫 번째 입력*&#x200B;의 데이터 형식이 선택한 *출력* 데이터 형식과 일치하는 노드가 목록에 포함됩니다.
* *입력* 커넥터에서 *링크를 끌어서* 노드 메뉴가 표시되면 *출력*&#x200B;의 데이터 형식이 *선택한 입력* 데이터 형식과 일치하는 노드가 목록에 포함됩니다.

![필터링된 노드 만들기](../../assets/mdl-filtered-node-creation.gif "필터링된 노드 만들기")

*MDL 그래프에서 필터링된 노드를 만듭니다. 커넥터의 값 유형에 따라 목록이 변경됩니다.*

## 그래프 입력 및 텍스처

MDL 재질은 예를 들어 값과 텍스처 형태로 외부 소스에서 데이터를 받을 수 있습니다. 전용 입력 노드가 있는 [Substance 그래프](../../compositing-graphs/substance-compositing-graphs.md)와 달리 <b>노드를 노출</b>하면 이러한 결과를 얻을 수 있습니다.

데이터는 *type*&#x200B;에 따라 노출된 노드로 전달될 수 있습니다. 예를 들어, Float 값은 노출된 <b>float</b> 노드에 전달되고 텍스처는 노출된 <b>color</b> 노드에 전달될 수 있습니다(이 경우 샘플링된 픽셀의 RGBA 값은 색상 값으로 전달됨).

![노출된 그래프 입력](../../assets/mdl-graph-inputs-samplers.png "노출된 그래프 입력")

*노출된 노드는 Raw 값 입력 및 텍스처의 샘플러인 그래프 입력을 만듭니다*
