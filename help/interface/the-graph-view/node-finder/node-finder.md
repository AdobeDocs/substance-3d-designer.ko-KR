---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/interface/the-graph-view/node-finder.html"
breadcrumb-title: ''
description: Node Finder 를 사용하여 Substance 그래프에서 노드를 신속하게 검색하고 찾아 효율적으로 탐색할 수 있습니다.
helpx_creative_field: ""
helpx_description: Designer > Interface > The graph view > Node finder
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 노드 찾기 도구
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '1342'
ht-degree: 0%

---


# 노드 찾기 도구

![노드 찾기 도구 모음](node-finder.resources/node-finder-toolbar.png "노드 찾기 도구 모음"){zoomable="yes"}

노드 찾기 도구 를 사용하면 텍스트 쿼리를 사용하여 <b>노드 및 변수 검색</b>을 수행할 수 있습니다. 쿼리와 일치하지 않는 모든 노드는 결과가 눈에 띄도록 흐리게 표시됩니다.

쿼리는 다음 조건 중 하나와 일치할 수 있습니다.

* 인스턴스 노드에서 참조하는 <b>그래프 식별자</b>입니다.
* 노드 매개 변수 함수에 사용되는 노출된 매개 변수 또는 변수의 <b>식별자</b>
* 노드의 <b>UID</b>(고유 식별자)
* 노드의 <b>레이블</b>

[하위 그래프](../../../compositing-graphs/creating-compositing-gra/graph-instances-sub-gra/graph-instances-sub-graphs.md)에서 노드와 변수를 찾을 수 있도록 재귀적으로 [그래프 인스턴스](../../../compositing-graphs/creating-compositing-gra/graph-instances-sub-gra/graph-instances-sub-graphs.md)를 검색할 수 있습니다. 검색해야 할 정확한 용어가 확실하지 않은 경우 퍼지 검색 옵션을 사용하여 질의에 허용치를 적용할 수 있습니다.

## 인터페이스

노드 Finder는 다음 두 가지 방법으로 액세스할 수 있습니다.

그래프 보기에서 <b>Ctrl+F</b>(Windows) / <b>Cmd+F</b>(macOS)을 눌러 노드 찾기 도구 모음을 표시하고 쿼리 필드에 포커스를 자동으로 설정합니다. 이렇게 하면 검색을 빠르게 수행할 수 있습니다.

그래프 보기 도구 모음에서 <b>노드 찾기 단추 ![](node-finder.resources/graph-node-finder.png)</b>을(를) 클릭하여 노드 찾기 도구 모음을 표시합니다. 일단 표시되면 도구 모음은 이 단추를 클릭하기만 하면 닫힙니다.

<b>트래버스 그래프를 검색합니다</b>. 즉, 다음과 같은 작업을 통해 그래프를 열 때 검색이 활성 상태로 유지됩니다.

* 인스턴스 노드: 컨텍스트에서 참조 열기(Ctrl+E / Cmd+E)(*참고:* 컨텍스트에서 그래프 편집을 편집 > 환경 설정 > 그래프에서 활성화해야 함)
* 픽셀 프로세서: 편집 기능(Ctrl+E / Cmd+E)
* 값 프로세서: 편집 기능(Ctrl+E / Cmd+E)
* FX-Map: FX-Map 그래프 편집(Ctrl+E / Cmd+E)
* 노드 매개변수: 함수 편집

![노드 찾기 도구: 검색 중 그래프 통과](node-finder.resources/node-finder-traversal.gif "노드 찾기 도구: 검색 중 그래프 통과"){zoomable="yes"}

### 검색 쿼리

![노드 찾기 쿼리 필드](node-finder.resources/node-finder-query-field.png "노드 찾기 쿼리 필드"){zoomable="yes"}

이 필드에 검색어를 입력할 수 있으며 화살표 단추를 클릭하면 현재 컨텍스트에서 사용 가능한 일부 변수를 포함하는 질의 제안 목록이 열립니다.

아래의 [검색 쿼리](#search-query) 섹션에서 수행할 수 있는 쿼리에 대해 자세히 알아보십시오.

### 노드 유형

![노드 유형](node-finder.resources/node-finder-node-types.png "노드 유형"){zoomable="yes"}

이 콤보 상자를 사용하면 특정 유형의 노드만 유지하도록 검색 결과를 필터링할 수 있습니다.

모든 인스턴스 노드는 노드의 *동일한 유형*(사실 &#39;인스턴스&#39; 유형)이지만 원자 노드는 각각 고유한 유형입니다.

+++노드 유형 목록
이 목록은 현재 그래프 유형에 따라 달라집니다.

![노드 형식(합성)](node-finder.resources/node-finder-types-compositing.png "노드 형식(합성)"){zoomable="yes"}



그래프 합성에 대한 *노드 유형*

![노드 형식(함수)](node-finder.resources/node-finder-types-function.png "노드 형식(함수)"){zoomable="yes"}



*함수 그래프의 노드 유형*

+++

+++원자 노드 검색
![노드 찾기 도구: &#39;Levels&#39; 유형별 검색(합성)](node-finder.resources/node-finder-compositing-levels.png "노드 찾기 도구: &#39;Levels&#39; 유형별 검색(합성)"){zoomable="yes"}



*Substance 그래프에서 &#39;Levels&#39; 노드 유형을 검색하는 중*

+++

+++인스턴스 노드 검색
![노드 찾기 도구: &#39;인스턴스&#39; 유형별 검색(합성)](node-finder.resources/node-finder-compositing-instances.png "노드 찾기 도구: &#39;인스턴스&#39; 유형별 검색(합성)"){zoomable="yes"}



*Substance 그래프에서 &#39;인스턴스&#39; 노드 유형을 검색하는 중*

![노드 찾기 도구: &#39;인스턴스&#39; 유형(함수)으로 검색](node-finder.resources/node-finder-functions-instances.png "노드 찾기 도구: &#39;인스턴스&#39; 유형(함수)으로 검색"){zoomable="yes"}



*Substance 함수 그래프에서 &#39;인스턴스&#39; 노드 유형을 검색하는 중*

+++

### 검색 옵션

<table>
<tr style="border: 0;">
<td width="100.00%" style="border: 0;" valign="top">

<b>검색 옵션 단추 ![](node-finder.resources/node-finder-search-options.png)</b>은(는) 검색에 사용되는 설정 목록을 열고 켜거나 끌 수 있습니다.

아래의 검색 옵션 섹션에서 이러한 옵션에 대해 자세히 알아보십시오.

</td>
<td width="33.33%" style="border: 0;" valign="top">

![노드 찾기 검색 옵션](node-finder.resources/node-finder-search-options-open.png "노드 찾기 검색 옵션"){zoomable="yes"}

</td>
</tr>
</table>

## 검색 쿼리

노드를 찾으려면 텍스트 쿼리를 아래에 나열된 노드 속성과 일치시킵니다.

>[!NOTE]
>
> 다음 주의 사항을 염두에 두고 쿼리를 입력해야 합니다.
> 
> * 검색은 대소문자를 구분하지 않습니다. 예를 들어, &#39;my node label&#39; 및 &#39;My Node Label&#39;은 동일한 결과를 반환합니다.
> * 쿼리 앞뒤에 있는 공백은 무시됩니다.
> * 동일한 그래프에서 여러 쿼리를 동시에 수행할 수 없습니다. 예를 들어, &#39;레벨 흐림 효과&#39;는 &#39;레벨&#39; 및 &#39;흐림 효과&#39; 노드와 모두 일치하지 않습니다. 마찬가지로 논리 연산자도 지원되지 않습니다.

<table>
<tr style="border: 0;">
<td width="100.00%" style="border: 0;" valign="top">

### 인스턴스 그래프 식별자

[인스턴스 노드](../../../compositing-graphs/creating-compositing-gra/graph-instances-sub-gra/graph-instances-sub-graphs.md)는 참조하는 그래프의 <b>식별자</b>를 사용하여 찾을 수 있습니다.

</td>
<td width="33.33%" style="border: 0;" valign="top">

![노드 찾기 도구: 그래프 식별자로 검색](node-finder.resources/node-finder-functions-identifier.png "노드 찾기 도구: 그래프 식별자로 검색"){zoomable="yes"}

*확대하려면 이미지 클릭*

</td>
</tr>
</table>

+++탐색기의 식별자
그래프는 탐색기에서 해당 식별자별로 나열됩니다.

![탐색기: 패키지 콘텐츠](node-finder.resources/explorer-package-simple.png "탐색기: 패키지 콘텐츠"){zoomable="yes"}



+++

+++인스턴스 노드의 도구 설명 식별자
인스턴스 노드의 도구 설명에는 참조된 그래프의 식별자가 포함되어 있습니다.

![인스턴스 노드의 도구 설명에 있는 그래프 식별자](node-finder.resources/node-finder-compositing-identifier.png "인스턴스 노드의 도구 설명에 있는 그래프 식별자"){zoomable="yes"}



+++

<table>
<tr style="border: 0;">
<td width="100.00%" style="border: 0;" valign="top">

### 노출된 매개 변수 및 변수

[노출된 매개 변수](../../../compositing-graphs/manage-parameters/exposing-a-parameter/exposing-a-parameter.md)의 식별자 또는 다른 변수를 직접 검색할 수 있습니다.

</td>
<td width="33.33%" style="border: 0;" valign="top">

![노드 찾기 도구: 노드 변수](node-finder.resources/node-finder-compositing-variable.png "노드 찾기 도구: 노드 변수"){zoomable="yes"}

*확대하려면 이미지 클릭*

</td>
</tr>
</table>

+++쿼리 제안
제안 목록을 표시하도록 쿼리 필드를 확장할 수 있습니다.

여기에는 현재 그래프 유형에 사용할 수 있는 [기본 제공 식별자](../../../function-graphs/variables/system-variables/system-variables.md)과 그래프에 노출된 매개 변수의 변수가 포함됩니다.

![노드 찾기 쿼리 제안](node-finder.resources/node-finder-available-query-suggestions.png "노드 찾기 쿼리 제안"){zoomable="yes"}



노출된 매개 변수의 식별자는 [Substance 그래프 속성](../../../compositing-graphs/graph-parameters/graph-parameters.md)에서 직접 복사하거나 편집할 수도 있습니다.

![노드 찾기 도구: 노출된 매개 변수](node-finder.resources/node-finder-compositing-exposed-parameter.png "노드 찾기 도구: 노출된 매개 변수"){zoomable="yes"}



*확대하려면 이미지 클릭*

+++

+++콘솔 경고/오류에서 변수 검색
그래프에 노드에서 사용하는 <b>변수</b>에 의해 발생한 오류 또는 경고가 있으면 <b>Windows > 콘솔</b>로 이동하여 변수를 포함할 전체 오류/경고 메시지를 표시합니다. 그런 다음 이 변수를 복사하여 노드 파인더 쿼리 필드에 붙여넣어 문제를 일으킨 노드를 빠르게 찾을 수 있습니다.

텍스트 편집기를 사용하여 SBS 파일의 XML 데이터에서 직접 변수를 복사할 수도 있습니다.

![노드 찾기 도구: 콘솔 경고/오류에서 변수 검색](node-finder.resources/node-finder-console-identifier.png "노드 찾기 도구: 콘솔 경고/오류에서 변수 검색"){zoomable="yes"}



+++

+++노드 가져오기/설정
그래프에서 변수를 검색할 때(노출된 매개 변수 포함) [Get](../../../function-graphs/nodes-reference-for-fun/atomic-function-nodes/get-nodes/get-nodes.md) 또는 [Set](../../../function-graphs/fxmaps/using-functions-in-fxmaps/using-the-set-sequence/using-the-set-sequence-nodes.md) 노드가 노드의 매개 변수 함수에서 해당 변수를 사용하는 모든 노드를 강조 표시합니다.

![노드 찾기 도구: 변수를 검색하면 해당 변수를 사용하는 Get 노드가 검색됨](node-finder.resources/node-finder-exposed-parameter-01.gif "노드 찾기 도구: 변수를 검색하면 해당 변수를 사용하는 Get 노드가 검색됨"){zoomable="yes"}



+++

<table>
<tr style="border: 0;">
<td width="100.00%" style="border: 0;" valign="top">

### 노드 UID

그래프의 각 노드에는 해당 노드를 검색하는 데 사용할 수 있는 고유한 식별자 번호(UID)가 있습니다.

</td>
<td width="33.33%" style="border: 0;" valign="top">

![노드 찾기 도구: UID로 검색](node-finder.resources/node-finder-compositing-uid-search.png "노드 찾기 도구: UID로 검색"){zoomable="yes"}

*확대하려면 이미지 클릭*

</td>
</tr>
</table>

+++노드의 UID 복사
노드의 UID는 컨텍스트 메뉴에서 클립보드에 복사할 수 있습니다.

이 작업은 UID를 다음 형식으로 복사합니다.

uid=1234567890

![노드 찾기 도구: 노드 UID 동작 복사](node-finder.resources/node-finder-compositing-uid-copy.png "노드 찾기 도구: 노드 UID 동작 복사"){zoomable="yes"}



+++

+++콘솔 경고/오류에서 노드 UID 검색
그래프에 노드에서 발생한 오류 또는 경고가 있으면 Windows > 콘솔로 이동하여 노드의 <b>UID</b>를 포함하는 전체 오류/경고 메시지를 표시합니다. 그런 다음 이 UID를 복사하여 Node Finder 쿼리 필드에 붙여넣어 문제를 일으킨 노드를 빠르게 찾을 수 있습니다.

노드 UID는 텍스트 편집기를 사용하여 SBS 파일의 XML 데이터에서 직접 복사할 수도 있습니다.

![노드 찾기 도구: 콘솔에서 노드 UID 검색](node-finder.resources/node-finder-console-uid.png "노드 찾기 도구: 콘솔에서 노드 UID 검색"){zoomable="yes"}



+++

### 노드 레이블

해당 레이블을 사용하여 노드를 찾을 수도 있습니다.

특정 노드를 검색하는 것은 퍼지 검색이 해제된 상태에서 정확한 레이블을 사용할 때 특히 효과적입니다.

## 검색 옵션

<table>
<tr style="border: 0;">
<td width="100.00%" style="border: 0;" valign="top">

<b>검색 옵션 단추 ![](node-finder.resources/node-finder-search-options.png)</b>을(를) 사용하면 노드 검색을 위한 <b>반복</b> 및 <b>유사 항목</b> 모드를 전환할 수 있습니다.

두 기능을 동시에 활성화할 수 있습니다.

</td>
<td width="33.33%" style="border: 0;" valign="top">

![노드 찾기 검색 옵션](node-finder.resources/node-finder-search-options-open.png "노드 찾기 검색 옵션"){zoomable="yes"}

</td>
</tr>
</table>

### 재귀 모드

[하위 그래프](../../../compositing-graphs/creating-compositing-gra/graph-instances-sub-gra/graph-instances-sub-graphs.md)의 결과를 포함하도록 [그래프 인스턴스](../../../compositing-graphs/creating-compositing-gra/graph-instances-sub-gra/graph-instances-sub-graphs.md)를 탐색하려면 이 옵션을 사용하도록 설정하십시오.

이 옵션은 Console의 경고 또는 오류 메시지에서 얻은 UID로 노드를 찾아야 하는 경우, 그래프 문제를 해결할 때 필수적일 수 있습니다.

![노드 찾기: 재귀 검색](node-finder.resources/node-finder-recursion-01.png "노드 찾기: 재귀 검색"){zoomable="yes"}

*오른쪽의 쿼리는 아래의 인스턴스 노드를 강조 표시합니다. 왼쪽의 참조된 그래프가 해당 쿼리와 일치하기 때문입니다.*

+++예제 1
![노드 찾기: 재귀 검색 예 1](node-finder.resources/node-finder-recursion-01.gif "노드 찾기: 재귀 검색 예 1"){zoomable="yes"}



인스턴스 노드는 여러 노드가 쿼리와 일치하는 그래프를 참조합니다.

+++

+++예제 2
![노드 찾기: 재귀 검색 예 2](node-finder.resources/node-finder-recursion-02.gif "노드 찾기: 재귀 검색 예 2"){zoomable="yes"}



&#39;재귀 검색&#39; 옵션을 활성화하면 픽셀 프로세서 노드가 쿼리와 일치하는 변수를 사용하는 그래프를 참조하는 인스턴스 노드가 강조 표시됩니다.

+++

### 퍼지 모드

쿼리의 정확한 철자가 확실하지 않은 경우 이 옵션을 사용하면 결과에서 <b>허용치</b>를 사용할 수 있습니다.

이 옵션을 사용하면 원하지 않는 일치 항목이 생길 수 있습니다.

![노드 찾기 도구: 퍼지 모드](node-finder.resources/node-finder-functions-fuzzy.png "노드 찾기 도구: 퍼지 모드"){zoomable="yes"}
