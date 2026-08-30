---
helpx_url: "https://helpx.adobe.com/kr/substance-3d-designer/substance-compositing-graphs/graph-parameters.html"
breadcrumb-title: ''
description: Substance 3D Designer에서 그래프 매개 변수를 만들고 관리하여 재질 속성과 비헤이비어를 제어하는 방법을 알아봅니다.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Graph parameters
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 그래프 매개변수
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '1492'
ht-degree: 1%

---


# 그래프 매개변수

이 페이지에서는 <b>Substance 그래프</b>의 표준 매개 변수에 대해 설명합니다.

그래프에는 수정할 수 있는 여러 매개 변수가 있습니다. 그래프에서 *빈 공간*&#x200B;을 클릭하거나 <b>탐색기</b> 패널에서 *그래프 항목*&#x200B;을 선택하여 찾을 수 있습니다. 그러면 매개 변수가 매개 변수 보기에 표시됩니다.

<a name="base-parameters"></a>

## 베이스 파라미터

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

이 섹션에는 *포함된 모든 노드*&#x200B;에 영향을 주는 매개 변수가 포함되어 있습니다.

실제로 기본 매개 변수가 &#39;부모 대비&#39; [상속 메서드](../../compositing-graphs/inheritance-compositing/inheritance-in-substance-compositing-graphs.md)(으)로 설정된 이 그래프의 모든 노드는 *그래프*&#x200B;의 기본 매개 변수에서 값을 가져옵니다.

차례로 그래프의 기본 매개 변수 값은 그래프가 사용되는 컨텍스트에 따라 달라집니다.

</td>
<td style="border: 0;" valign="top">

![기본 매개 변수](graph-parameters.resources/doc-graph-props-base-params.png "기본 매개 변수"){width="512px" zoomable="yes"}

</td>
</tr>
</table>

예를 들어, 다른 그래프에서 그래프를 인스턴스 노드로 사용하는 경우 해당 기본 매개 변수는 기본적으로 &#39;입력 기준&#39; 상속 메서드를 사용합니다. 즉, 기본 입력에 연결된 노드에서 해당 값을 가져옵니다. ([재정의](#input-parameters)가 아닌 경우)

대부분의 경우 상속은 이러한 값을 정의하고 이러한 값이 그래프 전체에서 어떻게 변경되는지를 정의하는 데 중요한 역할을 합니다. 따라서 이러한 매개 변수를 사용하기 전에 Substance 그래프의 [상속](../../compositing-graphs/inheritance-compositing/inheritance-in-substance-compositing-graphs.md)에 대해 잘 이해하는 것이 좋습니다.

|                      |                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|:---------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <b>출력 크기</b> | 이 매개 변수를 사용하면 그래프에서 이미지의 *기본 해상도*&#x200B;를 선택할 수 있습니다.  사용: <div><img data-preserve-html="true" height="22" src="graph-parameters.resources/props-output-size-lock.jpg"/></div> 크기를 조정할 때 높이 및 폭 값이 일치하도록 단추를 잠그고 이미지의 정사각형을 유지합니다.<br><br>*기본값: (0,0) - 부모에 대한 상대* [자세히 알아보기](../../compositing-graphs/output-size/output-size.md) |
| <b>출력 형식</b> | 다음 옵션에서 그래프의 *기본 비트 심도*&#x200B;을(를) 선택할 수 있습니다.<ul data-preserve-html="true"><li data-preserve-html="true">8비트</li><li data-preserve-html="true">16비트</li><li data-preserve-html="true">HDR 낮은 정밀도 16F(16비트 부동 소수점)</li><li data-preserve-html="true">HDR High Precision 32F(32비트 부동 소수점)</li></ul>*기본값: 채널당 8비트 - 부모에 대한 상대* |
| <b>픽셀 크기</b> | 픽셀 크기를 정의합니다. **폭** 및 **Height** 값을 모두 **1**(으)로 설정하는 것이 좋습니다.*기본값: (1,1) - 부모 기준* |
| <b>타일링 모드</b> | 다음 옵션에서 그래프의 기본 *타일링 모드*&#x200B;를 정의합니다.<ul data-preserve-html="true"> <li data-preserve-html="true">타일링하지 않음</li> <li data-preserve-html="true">수평 타일링</li> <li data-preserve-html="true">수직 타일링</li> <li data-preserve-html="true">H+V 타일링(즉, 수평 및 수직)</li> </ul>*기본값: H 및 V 타일링 - 부모를 기준으로* |
| <b>임의 시드</b> | 그래프의 기본 *임의 시드*&#x200B;를 정의합니다.  사용: <div><img data-preserve-html="true" height="22" src="graph-parameters.resources/prop-randomise.jpg"/></div> 임의의 시드에 새 임의의 값을 할당하는 단추입니다.<br><br>*기본값: 0 - 부모에 대한 상대* |

<table>
<tr style="border: 0;">
<td width="100.00%" style="border: 0;" valign="top">

<a name="attributes"></a>

## 특성

<b>특성</b> 섹션에는 그래프에 대한 *메타데이터*&#x200B;가 포함되어 있습니다. 이 메타데이터는 작성자가 디자인한 대로 그래프를 *식별*, *범주화* 및 *적용*&#x200B;하는 데 필요한 정보를 제공합니다.

</td>
<td width="33.33%" style="border: 0;" valign="top">

![그래프 특성](graph-parameters.resources/doc-graph-props-attributes.png "그래프 특성"){zoomable="yes"}

</td>
</tr>
</table>

+++속성 목록

|                      |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
|:---------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **식별자** | 그래프의 이름이며 *고유*&#x200B;이어야 합니다. 같은 패키지에 같은 <b>식별자</b>를 가진 그래프를 두 개 이상 포함할 수 없습니다. [탐색기](../../interface/the-explorer-window/the-explorer-window.md) 패널에서 그래프의 *이름*(으)로 사용됩니다.<br><br>*참고:* 식별자 *은(는) 빈 문자열일 수 없습니다*. 빈 문자열은 자동으로 `_` 또는 `Substance_graph`(으)로 바뀝니다. 이 값에 *만* 문자를 사용할 수 있습니다. *`A-Z, 1-9, @$%[{]}_-`.* 승인되지 않은 문자는 `_`(으)로 자동 대체됩니다.<br><br>*기본값: New\_Graph 또는 그래프 생성 시 사용자가 설정합니다.* |
| **레이블** | <b>레이블</b>은 <b>식별자</b> 대신 *사용자 대면* 시나리오에서 더 나은 가독성을 위해 그래프의 *이름*&#x200B;을 표시하는 데 사용됩니다(예: [라이브러리](../../interface/the-library/the-library.md) 항목 또는 [인스턴스 노드](../creating-compositing-gra/graph-instances-sub-gra/graph-instances-sub-graphs.md) 레이블).  레이블은 *고유하지 않은*&#x200B;일 수 있으며 특수 문자를 포함할 수 있습니다.<br><br>*팁:* 그래프의 이름을 바꾸는 경우(예: [탐색기](../../interface/the-explorer-window/the-explorer-window.md)에서) 레이블을 변경할 수도 있습니다!<br><br>*기본값: 비어 있는* |
| **유형** | <b>유형</b>은 [Substance 그래프](../../compositing-graphs/substance-compositing-graphs.md)의 의도된 목적을 정의하는 데 사용됩니다. 이는 주로 [&#39;Send&#39; 상호 운용성 기능](../../interface/the-explorer-window/send-to-interoperability/send-to-interoperability.md)을 위한 것입니다. |
| **재질 모델** | 그래프의 재질 모델을 설정하면 셰이더 *모델과 일치하는 셰이더*&#x200B;를 사용할 수 있는 경우 3D 보기에서 적절한 셰이더가 사용됩니다.<br>예: 3D 뷰에서 `OpenPBR v1.1` 재료 모드로 그래프를 보면 대상 재료에 대한 `OpenPBR Surface` 셰이더가 선택됩니다.<br><br>일치하는 셰이더가 없거나 그래프의 모델이 `Undefined`(으)로 설정된 경우 3D 뷰의 대상 자료에 사용되는 셰이더는 *변경되지 않음*&#x200B;입니다. |
| **물리적 크기** | 이 값은 *물리적 세계*&#x200B;에 있는 텍스처의 차원을 X(길이), Y(너비) 및 Z(Height)로 지정합니다. 따라서 그래프에서 생성되는 자료와 본질적으로 관련이 있다. 예를 들어 <b>2D 보기</b> 및 <b>3D 보기</b>에서 텍스처를 올바른 비율로 표시하는 데 물리적 크기를 사용할 수 있습니다.<br><br>*팁:* $physicalsize [내장 변수](../../function-graphs/variables/system-variables/system-variables.md)를 사용하여 Substance 그래프의 모든 노드에 적용된 Substance 함수 그래프에서 Float3 값으로 물리적 크기 그래프를 검색할 수 있습니다.<br><br>*참고:* **Z** 값은 현재 **3D 보기**&#x200B;에서 *고려되지 않습니다*. 따라서 재질에 대한 **Height 비율** 값은 **heightscale** 사용으로 설정된 **출력** 노드를 사용하거나 **재질 속성**&#x200B;에서 직접 설정해야 합니다.<br><br>*기본값: (0,0,0)* |
| **아이콘** | 이 영역에서는 <b>라이브러리</b>에서 이 그래프의 항목을 표시하는 데 사용할 *아이콘*&#x200B;을(를) <b>SBS</b> 및 <b>SBSAR</b> 모두로 정의할 수 있습니다. 아이콘은 [Substance 3D Painter](https://www.adobe.com/kr/products/substance3d-painter.html)의 <b>선반</b>과 같은 다른 상황에서도 사용됩니다. 이 영역에는 다음과 같은 옵션이 있습니다.<ul data-preserve-html="true"> <li data-preserve-html="true"><b>찾아보기</b>: 아이콘으로 사용해야 하는 <i>기존 이미지</i>에 대한 시스템 파일을 찾아볼 수 있습니다.</li> <li data-preserve-html="true"><b>생성</b>: <b>PBR 렌더링</b> 노드의 <i>기본 제공 사전 설정</i>을 사용하여 아이콘을 생성합니다.</li> <li data-preserve-html="true"><b>붙여넣기</b>: 현재 <i>클립보드</i>에 있는 이미지 데이터를 아이콘으로 붙여넣을 수 있습니다.</li> <li data-preserve-html="true"><b>제거</b>: 이 옵션은 기존 아이콘을 <i>제거</i>하고 아이콘 슬롯을 <i>비웁니다</i>.</li> </ul>*참고:* **생성** 옵션은 **물리적 크기**&#x200B;을 사용하여 변위 효과에 대한 **PBR 렌더링**&#x200B;의 **Height 크기**&#x200B;를 결정합니다. **physicalsize** 사용법으로 설정된 **출력** 노드가 그래프에 있으면 이 출력이 사용됩니다. 이러한 출력이 없으면 그래프의 **특성**&#x200B;의 값이 *대신* 사용됩니다. 특성 값이 (0,0,0)이면 0.1의 *사전 설정 값*&#x200B;이 사용됩니다.<br><br>*참고:* *아이콘 없음*&#x200B;이 정의되면 그래프에 대한 *첫 번째 이미지 출력*&#x200B;이 대신 사용됩니다.<br><br>*기본값: 비어 있음* |
| **패키지** | 이 그래프가 속한 **패키지**&#x200B;에 대한 *절대* 파일 이름입니다.**폴더** 단추를 사용하면 이 위치에서 새 시스템 *파일 브라우저 창*&#x200B;을 열 수 있습니다.*기본값: 패키지가 저장되지 않은 경우 패키지 파일 이름/비어 있음* |
| **SBSAR에서 노출됨** | 그래프와 해당 출력을 그래프의 **패키지**&#x200B;에서 게시된 **SBSAR** 파일에서 *보기*&#x200B;할 수 있는지 여부를 제어합니다. 이는 패키지의 일부 그래프가 패키지의 기본 그래프에 대해 *하위 그래프*&#x200B;으로만 사용되고 *이(가)**SBSAR**&#x200B;에 나타나지 않아야*&#x200B;하는 경우 유용합니다.*기본값: 예* |
| **라이브러리에 표시** | 패키지가 **라이브러리**&#x200B;에서 *시청*&#x200B;된 위치에 저장된 경우 **라이브러리**&#x200B;에서 *표시*&#x200B;할지 여부를 제어합니다.*기본값: 프로젝트 설정의 [라이브러리] 탭에서 설정* |
| **설명** | 그래프의 *설명 텍스트*&#x200B;입니다.**라이브러리**&#x200B;의 그래프 항목, 이 그래프의 모든 **인스턴스** 노드 및 기존 **Substance 통합**&#x200B;이 포함된 소프트웨어의 *도구 설명*&#x200B;에 표시됩니다.*기본값: 비어 있음* |
| **범주** | 이 필드를 사용하여 **라이브러리**&#x200B;에서 이 그래프 항목에 대한 *범주*&#x200B;를 설정할 수 있습니다.*기본값: 비어 있음* |
| **작성자** | 이 필드를 사용하여 작성자의 *이름*&#x200B;을 넣을 수 있습니다.*기본값: 비어 있음* |
| **작성자 URL** | 이 필드에서 *URL*(예: 작성자의 웹 사이트)을 입력할 수 있습니다.*기본값: 비어 있음* |
| **태그** | 이 필드를 사용하여 그래프의 *검색 가능성* 및 *검색 가능성*&#x200B;을 개선하기 위해 고유한 *태그*&#x200B;를 추가할 수 있습니다.*기본값: 비어 있음* |
| **그룹** | [노드] 메뉴에서 항목을 그룹화할 수 있습니다. 공통 &#39;그룹&#39; 값을 공유하는 그래프 또는 비트맵과 같은 리소스는 그룹 이름을 따서 명명된 섹션에 함께 그룹화됩니다. *기본값: 비어 있음* |
| **사용자 데이터** | 이 필드를 사용하여 자신의 추가 데이터를 추가할 수 있습니다. 서드파티 소프트웨어의 사용자 정의 통합에 유용합니다. Substance 3D Painter 및 Sampler은 이 사용자 데이터를 사용하여 특정 동작을 설정합니다.*기본값: 비어 있음* |
| **템플릿 데이터** | Substance 그래프를 템플릿으로 사용할 때 이 특성은 [템플릿의 범주와 부제](../../compositing-graphs/creating-compositing-gra/creating-a-substance-compositing-graph.md)를 설정합니다. 다음 방법으로 구분됩니다. &lt;category>;&lt;subtitle> <br><br>*기본값: Empty* |

+++
<a name="input-parameters"></a>

## 입력 매개 변수

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

[노출된 매개 변수](../../compositing-graphs/manage-parameters/exposing-a-parameter/exposing-a-parameter.md)를 포함하여 그래프와 관련된 모든 매개 변수는 [관리](../../compositing-graphs/manage-parameters/manage-parameters.md)되며 여기서 편집하고 미리 볼 수 있습니다.

일부 또는 모든 매개 변수에 대해 [매개 변수 사전 설정](../../compositing-graphs/manage-parameters/parameter-presets/parameter-presets.md)을 만들 수도 있습니다.

</td>
<td style="border: 0;" valign="top">

![입력 매개 변수](graph-parameters.resources/doc-graph-props-input-parameters.png "입력 매개 변수"){zoomable="yes"}

</td>
</tr>
</table>

+++기본 매개 변수 재정의
다른 그래프의 그래프를 [인스턴스 노드](../creating-compositing-gra/graph-instances-sub-gra/graph-instances-sub-graphs.md)(으)로 사용하는 경우 해당 새 인스턴스 노드의 기본 매개 변수에 대한 기본값을 제어할 수 있습니다.

&#39;입력 매개 변수&#39; 섹션 위쪽에 있는 햄버거 메뉴를 열고 &#39;기본 매개 변수 재정의&#39; 하위 메뉴로 이동하여 임의의 기본값을 설정할 기본 매개 변수를 선택합니다.

선택한 매개변수의 편집기가 그래프 입력 매개변수 목록 상단에 나타납니다. 그런 다음 해당 값과 [상속 방법](../../compositing-graphs/inheritance-compositing/inheritance-in-substance-compositing-graphs.md)을 원하는 대로 조정할 수 있습니다.

+++

>[!IMPORTANT]
>
> [직접 편집](../../interface/preferences-window/preferences-window.md)을 사용하는 경우 <b>미리 보기</b> 및 <b>사전 설정</b> 탭이 비활성화됩니다.

<a name="inputs"></a>

## 입력

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

이 부분에서는 모든 그래프의 [입력](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/input/input.md) 노드가 나열됩니다.

각 항목의 맨 왼쪽에 있는 핸들을 드래그하여 놓아 순서를 변경할 수 있습니다.

</td>
<td style="border: 0;" valign="top">

![입력](graph-parameters.resources/doc-graph-props-inputs.png "입력"){zoomable="yes"}

</td>
</tr>
</table>

<a name="outputs"></a>

## 출력

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

이 부분에서는 모든 그래프의 [출력](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/output/output.md) 노드입니다.

각 항목의 맨 왼쪽에 있는 핸들을 드래그하여 놓아 순서를 변경할 수 있습니다.

</td>
<td style="border: 0;" valign="top">

![출력](graph-parameters.resources/doc-graph-props-outputs.png "출력"){zoomable="yes"}

</td>
</tr>
</table>
