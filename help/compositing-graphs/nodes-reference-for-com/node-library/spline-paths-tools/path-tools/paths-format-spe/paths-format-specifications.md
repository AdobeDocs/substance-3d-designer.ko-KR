---
helpx_url: "https://helpx.adobe.com/kr/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/spline-paths-tools/path-tools/paths-format-specifications.html"
breadcrumb-title: ''
description: 패스 및 스플라인 노드에서 사용하는 패스 형식 사양 및 데이터 구조에 대해 알아봅니다.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Spline  Path Tools > Path Tools > Paths Format Specifications
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 패스 형식 사양
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '2491'
ht-degree: 0%

---


# 패스 형식 사양

이 페이지에서는 경로 형식에 대해 설명하고 경로 도구에 포함된 함수를 사용하여 해당 형식으로 데이터를 조작하기 위한 지침을 제공합니다.

## 포맷 사양

<table>
<tr style="border: 0;">
<td width="100.00%" style="border: 0;" valign="top">

이 섹션에서는 <b>경로 문서</b>(또는 이미지)의 인코딩 방법에 대해 설명합니다.

패스 문서는 각각 <b>32비트 부동 소수점 색상 텍스처</b>로 인코딩된 세그먼트 목록을 설명하는 패스 목록입니다.

텍스처가 &#39;위&#39;(*$pos.y &lt; 0.5*) 부분과 &#39;아래&#39;(*$pos.y > 0.5*) 부분으로 분할됩니다.

&#39;위&#39; 부분의 픽셀에 있는 모든 데이터는 의미상 &#39;아래&#39; 부분의 일치하는 픽셀과 밀접하게 관련되며, 그 반대의 경우도 마찬가지입니다.

</td>
<td width="33.33%" style="border: 0;" valign="top">

![패스 다각형 인코딩 데이터](paths-format-specifications.resources/PathsPolygon_Data.jpg "패스 다각형 인코딩 데이터")

</td>
</tr>
</table>

>[!NOTE]
>
> 패스 데이터는 32비트 정밀도가 필요하며 비트 심도를 더 낮게 사용하면 잘못된 결과가 나옵니다.
> 
> 따라서 패스 데이터를 생성하는 노드의 &#39;출력 형식&#39; 매개 변수를 &#39;HDR High Precision(32F)&#39;으로 설정해야 합니다.

`*uv\_pos*`을(를) &#39;top&#39; 부분의 픽셀의 2D 주소(예: *$pos*)로 지정하십시오.

이 문서의 나머지 부분에서:

* <b>top[uv\_pos].XYZW</b>은(는) 위쪽 부분의 픽셀에 저장된 4개의 부동 소수점을 가리킵니다.\
  top[uv\_pos] == sample\_color(paths, uv\_pos)
* <b>bottom[uv\_pos].XYZW</b>은(는) 아래 부분의 일치하는 픽셀에 저장된 4개의 부동 소수점을 가리킵니다.\
  bottom[uv\_pos] == sample\_color(paths, uv\_pos + Float2(0, 0.5))

top[uv\_pos]와 bottom[uv\_pos]가 함께 8개의 플로트로 구성된 문서의 의미 단위 U[uv\_pos]를 형성하고 있습니다.

### 문서 헤더

모든 패스 문서는 문서 헤더로 시작합니다. 그것은 바로 첫 번째 의미 단위 U[(0,0)]:

+++위
<b>X</b>

경로 수([0; 16777216]에서 양의 정수여야 함)입니다.

일부 패스가 비어 있는 경우에도 여기에 포함됩니다. 따라서 &#39;디코딩할 경로 헤더의 수&#39;로 생각할 수 있습니다.

<b>YZ</b>

이 문서의 픽셀 크기입니다(예: 정확히 `Float2(1,1) / $size`).

이 기능은 출력 크기가 다른 [픽셀 프로세서](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/pixel-processor/pixel-processor.md) 또는 [Fx-Map](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/fx-map/fx-map.md)에서 패스를 읽을 때 유용합니다.

<b>폭</b>

1/16 = 0.0625(헤더 플래그)

+++

+++아래
<b>XY</b>

이 문서에 정의된 마지막 정점의 주소입니다. 새 데이터를 추가하는 데 유용합니다.

따라서 실제로 마지막 정점의 주소보다 스캔라인 순서로 더 큰 주소일 수 있습니다. 범위: &rbrack;0, 1[×]0,.5&lbrack;

<b>ZW</b>

사용되지 않음, 부동2(0, 1)여야 함

+++

### 패스 머리글

문서 머리글 바로 다음에 경로 수 = top[(0,0)].X 경로 헤더가 시맨틱 단위로 하나씩 옵니다.\
E.g. 문서에 3개의 경로가 있는 경우 해당 경로는 U[(0,1)\*pixel\_size], U[(0,2)\*pixel\_size] 및 U[(0,3)\*pixel\_size] (픽셀\_size = top[(0,0)].YZ 포함)에 저장됩니다.

한 픽셀 행에 포함할 수 있는 것보다 많은 패스가 있는 경우 나머지 패스-헤더는 다음 행 중 하나에 스캔라인 순서로 기록됩니다.\
Null 경로 헤더(`top[...].XYZW = Float4(0,0,0,0)`)를 사용할 수 있습니다. 이러한 경로는 하나의 빈 경로로 허용됩니다.

주소 `path\_addr`에서 N번째 경로의 경로 헤더는 다음과 같이 정의됩니다.

+++위
<b>X</b>

이 패스의 정점 수입니다. [0, 16777216] 범위 내에 있어야 합니다.

닫힌 패스의 시작 정점과 끝 정점이 같은 위치에 있으면 두 정점을 셉니다.\
정점이 0인 패스는 유효한 패스입니다.

<b>Y</b>

*Is\_closed* 플래그: 경로가 닫힌 경우 1(예: 원), 그렇지 않은 경우 0(예: 직선).

<b>Z</b>

경로 인덱스 *N.*&#x200B;반드시 *path\_addr*과(와) 일치해야 합니다(아래 참고 참조).

<b>폭</b>

헤더 플래그: 1/16 = 0.0625.

+++

+++아래
<b>XY</b>

시작(또는 첫 번째) 정점 주소.

<b>ZW</b>

끝(또는 마지막) 정점의 주소입니다.

+++

>[!NOTE]
>
> paths\_tools.sbs의 `Utils/pixel\_index\_to\_position` 함수를 사용하여 N에서 `path\_addr`을(를) 계산할 수 있습니다. `path\_addr = pixel\_index\_to\_position(N+1)`

### 정점 정보

정점은 머리글(문서 또는 패스 머리글) 뒤의 이미지 아무 곳에서나 찾을 수 있습니다. 정점은 다양한 &quot;유형&quot;(시작, 중간 또는 끝)일 수 있으며 2개의 주소 포인터(&quot;링크&quot;)를 사용하여 명시적으로 연결됩니다.

<b>시작</b> 및 <b>끝</b> 정점은 이와 관련하여 특별합니다. 닫힌 패스나 함께 연결된 임의의 경로 네트워크를 표시할 수 있도록 링크 중 하나를 사용하여 실제로 같은 정점을 나타내는 다른 모든 시작 또는 끝 정점의 순환 앞으로 연결된 목록을 만듭니다. 이렇게 서로 일치하는 정점을 &quot;형제&quot;라고 합니다. [일러스트레이션 환영됨]

공식적으로 주소 `*vert\_addr*`의 각 정점은 다음과 같이 정의됩니다.

+++위
<b>XY</b>

꼭지점 위치입니다. 좌표는 NaN 또는 ±inf가 아닌 부동 소수점 값일 수 있습니다. 이 수준에서 타일링에 대한 개념이 없기 때문에(이것은 각각의 필터의 구현에 의해 처리되거나 처리되지 않을 수 있다), 따라서 경로는 유클리드 평면에서 정의되어야 한다.

<b>Z</b>

정점 패스 인덱스 정점은 하나의 패스에만 속할 수 있습니다. 앞에서 언급한 것처럼 [시작] 및 [종료] 정점에는 형제가 있을 수 있습니다. 경로 인덱스는 path-header를 검색하는 데 사용할 수 있으므로(위의 [패스 헤더 섹션] 참조) 동기화해야 합니다.

<b>폭</b>

꼭지점 유형입니다. 값의 부호와 절대값 사이에서 분할됩니다.

부호 부분에서 0의 값은 실제로 여기 정점이 없다는 것을 의미할 것이다(다른 모든 성분들도 0이어야 한다). 음수 값을 지정하면 정점이 &quot;모퉁이&quot;로 표시되고 양수 값을 지정하면 정점이 &quot;매끄럽게&quot;됩니다. 모퉁이 정점과 부드러운 정점은 순수하고 분리된 특성이며 나머지 패스 인코딩에는 아무런 영향이나 의미가 없습니다.

절대값 부분에서는 픽셀의 종류(시작, 중간 또는 종료)와 다른 플래그(trivial\_link)가 인코딩됩니다.

* *0.125*: 끝 정점(모양의 마지막 정점; 항상 중요하지 않은 링크, 아래 참조)

* *0.25*: 시작 꼭지점(모양의 첫 번째 꼭지점; 항상 중요하지 않은 링크, 아래 참조)

* *0.5*: 중요한 링크가 있는 중간 정점

* *1*: 사소한 링크가 있는 중간 정점

&quot;Trivial links&quot;는 (현재 경로의 정점 목록에 있는) 이전 정점과 다음 정점이 각각 픽셀 내 왼쪽(vert\_addr-(0,pixel\_size))과 오른쪽(vert\_addr+(0,pixel\_size))에 저장되는 반면, &quot;Non-trivial links&quot;는 이 중 적어도 하나가 다른 곳에 저장된다는 것을 의미합니다.

+++

+++아래
링크 &quot;삼중성&quot;에 관계없이 링크의 신뢰할 수 있는 값은 아래 부분에 저장됩니다.

<b>XY</b>

이 패스의 이전 정점 주소입니다. [시작] 정점의 경우 이 정점은 다음 형제 정점을 가리킵니다.\
if |top[vert\_addr].W| = 1, bottom[vert\_addr].XY = vert\_addr - (0,pixel\_size)

<b>ZW</b>

이 패스의 다음 정점 주소입니다. 끝 정점의 경우 이 정점은 다음 형제 정점을 가리킵니다.\
if |top[vert\_addr].W| = 1, bottom[vert\_addr].ZW = vert\_addr + (0,pixel\_size)

+++

## 패스 정보 읽기 및 쓰기

자신만의 패스 처리 노드를 만들려면 몇 가지 도구를 사용할 수 있습니다.

기본 사항은 [패스 정점 프로세서](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/paths-vertex-processor/paths-vertex-processor.md) 및 [패스 정점 프로세서 단순](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/paths-vertex-processor-1/paths-vertex-processor-simple.md) 노드에서 제공되는데, 기본적으로 [픽셀 프로세서](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/pixel-processor/pixel-processor.md)와 같은 방식으로 사용할 수 있습니다.

패스 정점 프로세서 노드에서 제공하는 기능 이외의 기능이 필요한 경우(더 많은 입력 텍스처, 또는 더 많은 이전 또는 다음 정점), 이 그래프의 구현을 복사하는 것이 좋은 시작점이 될 수 있습니다(<b>Get(&quot;%perVertex&quot;)</b> 노드를 사용자 지정 처리로 바꾼다고 가정할 때).

그러나 정점당 함수를 적용하는 것보다 더 외계 적인 것을 하고자 하는 경우, 사용할 수 있는 도구에 대한 자세한 설명은 다음과 같다. 일반적으로 다른 Paths 노드(*paths\_tools.sbs)*&#x200B;와 동일한 패키지에서 찾을 수 있는 작은 도우미 함수입니다. 이러한 함수는 [<b>라이브러리</b>](../../../../../../interface/the-library/the-library.md) 및 <b>노드 메뉴</b>에 표시되지 않습니다.

### &#39;읽기&#39; 함수

`Read` 폴더에서 경로에 대한 정보를 수집하는 데 유용한 몇 가지 항목을 찾을 수 있습니다.

어떤 픽셀은 주어진 픽셀에 대한 정보를 줄 수 있습니다. 이들은 모두 \*top\* 부분에서 샘플링된 Float4 값을 입력으로 사용합니다. 그들의 구현을 보면, 그것들은 매우 간단합니다. 그들의 요점은 원자마디가 아니라 더 많은 의미를 전달하는 것이다.

+++is_header
현재 샘플 값이 패스 헤더 또는 문서 헤더인지 확인합니다.

+++

+++path_is_closed
경로 헤더에서 Is\_Closed 플래그(.Y)를 확인합니다. \*이미 경로가 `is\_header`이고 `current\_pixel\_is\_document\_header`이(가) false를 반환했음을 확인했다고 가정합니다.

+++

+++is_vertex
현재 샘플 값이 헤더가 아닌 정점이거나 빈 픽셀인지 확인합니다.

+++

+++is_start_vertex
\*상위 부분 샘플링\* 값이 시작 정점인지 확인합니다. 먼저 `is\_vertex`을(를) 확인할 필요가 없습니다.

+++

+++is_mid_vertex
\*상위 부분 샘플링\* 값이 시작 정점이나 끝 정점이 아닌 정점인지 확인합니다. 먼저 `is\_vertex`을(를) 확인할 필요는 없습니다.

+++

+++is_end_vertex
\*상위 부분 샘플링\* 값이 끝 정점인지 확인합니다. 먼저 `is\_vertex`을(를) 확인할 필요가 없습니다.

+++

+++is_segment_start
`is\_start\_vertex || is\_mid\_vertex`에 대한 약식. [Fx-Map](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/fx-map/fx-map.md) 기반 처리에 더 유용하여 각 세그먼트를 한 번에 처리할 수 있습니다.

+++

+++is_corner
정점의 모퉁이 플래그를 확인합니다. 먼저 `is\_vertex`을(를) 확인할 필요는 없습니다. 대답이 true이면 정점에 있는 것입니다. 이 플래그는 공식 노드에서 아직 지원되지 않습니다.

+++

+++has_trivial_links
정점이면 아래쪽 부분을 샘플링하지 않고도 이전 정점과 다음 정점의 위치를 쉽게 추론할 수 있는지 여부를 알려줍니다. 참고: 정점이 아닌 값은 항상 false를 반환합니다.

직접 사용하지 않고 `sample\_next\*` 또는 `sample\_prev\*` 함수 중 하나를 사용할 수 있습니다.

+++

+++sample_next, sample_prev
최상위 부분 샘플링 값 `*sampled*` 및 해당 위치 `*sampled\_position*`이(가) 주어지면 다음(각각 이전) 정점 최상위 부분 샘플링 값을 반환하고 Float2 변수 `*next\_sampled\_pos*`을(를) 이 인접 영역의 위치(즉, &lt;returned value> = SampleColor(next\_sampled\_pos, image0))로 설정합니다. `*input0PixSize*`은(는) 패스의 픽셀 크기(top[(0,0)].YZ)와 같아야 합니다.

현재 픽셀(`*sampled*`)이 <b>시작</b> 정점이면 *샘플\_이전*&#x200B;은(는) 이 정점의 다음 동위 멤버를 반환합니다. 마찬가지로, <b>끝</b> 정점이면 *샘플\_다음*&#x200B;은(는) 이 정점의 다음 동위 멤버를 반환합니다(즉, 원하지 않는). 이 문제를 해결하려면 아래 `*sample\_next\_advanced*` 및 `*sample\_prev\_advanced*`을(를) 참조하십시오.

<b>경로 정보는 단순하게 input0!</b>에 저장되어 있습니다. 또한 함수의 문서에서 설명하는 것과 달리 `*next\_sampled\_pos*`을(를) 미리 선언할 필요가 없습니다. `*[out]next\_sampled\_pos*`은(는) 이 두 번째 &quot;반환 값&quot;이 있음을 알리는 더미 매개 변수입니다.

세 번째 반복 노드의 Iterations 매개 변수에서 `*paths\_trace*` [Fx-Map](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/fx-map/fx-map.md)을(를) 확인할 수 있습니다. 사용 방법에 대한 예시.

![sample_next의 최소 사용 사례](paths-format-specifications.resources/paths-spec_fxmap-sample-next_02.png "sample_next의 최소 사용 사례")



![미리 보기 경로(path_trace)에서 sample_next의 대/소문자 사용](paths-format-specifications.resources/paths-spec_fxmap-sample-next_01.png "미리 보기 경로(path_trace)에서 sample_next의 대/소문자 사용")



+++

+++sample_next_advanced, sample_prev_advanced
이는 닫힌 경로에서 작업하기 위한 것입니다. 열린 패스의 경우 시작 또는 끝 정점에 형제 정점이 없으며 이 경우 두 함수 모두 같은 값을 반환하고 인접 정점만 반환합니다. 둘 이상의 형제가 있는 [시작] 또는 [종료] 정점(네트워크로 연결된 패스)의 경우 연결된 목록에서 다음 형제의 주변 정점을 반환합니다.

+++

### &#39;쓰기&#39; 함수

`Write` 폴더 아래에서 [Fx-Map](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/fx-map/fx-map.md)</b>을(를) 사용하여 <b>쓸 수 있는 Float4를 빌드하는 작은 도우미를 찾을 수 있습니다.

실제로 [Fx-맵](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/fx-map/fx-map.md)은 그리기 전에 RGB에 Alpha을 곱하므로 이를 보정하기 위해 실제 값은 미리 곱해지지 않습니다. 예를 들어 [픽셀 프로세서](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/pixel-processor/pixel-processor.md)에서 이러한 함수를 사용하려면, 사전 곱셈을 다시 적용하거나 사용자 지정 버전을 작성하는 것이 좋습니다(사용 사례에 더 최적화되어 사용하기 쉬움).

+++document_header
문서 헤더의 윗부분을 빌드하여 제공하는 경로 수를 선언합니다.

+++

+++document_last_vertex_spec
마지막 정점 주소를 지정하는 문서 헤더의 \*아래쪽\* 부분을 작성합니다(A.1 참조).

+++

+++path_header
`*nbVertices*` 경로의 정점 수, `*isClosed*` 플래그 및 `*pathIndex*`에 따라 패스 헤더의 윗부분을 빌드합니다.

+++

+++start_vertex, mid_vertex, end_vertex
정점의 위쪽을 빌드하여 위치, 문자 및 기타 옵션을 적절하게 설정합니다.

*mid\_vertex* 및 *hasTrivialLinks* 매개 변수 정보: 적절한 값을 설정하는 것이 이상적이지만 어떤 이유로 링크가 사소한지 여부를 알 수 없는 경우 생성된 경로를 더 느리게 처리하는 대신 안전하게 false로 설정할 수 있습니다.

+++

경로 헤더나 정점에 대한 하위 파트 작성기는 없습니다. 둘 다 상위 파트에 대한 두 링크를 인코딩하므로 이 함수는 기본적으로 두 Float2의 Vector Float4 생성자입니다. [Fx-Map](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/fx-map/fx-map.md)을(를) 사용하여 작성하는 경우 XYZ를 W로 나누는 것을 잊지 마십시오(W는 주소의 Y이므로 반드시 null이어야 함).

[패스 다각형](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/paths-polygon/paths-polygon.md) 노드를 호스팅하는 <b>*패스\_다각형.sbs* </b> 패키지에서 이러한 함수를 사용하는 방법에 대한 적절한 예를 확인할 수 있습니다.

### 경로 처리 방법

픽셀 프로세서 또는 Fx-Map을 사용하여 다음과 같은 장점과 단점이 있는 사용자 정의 처리를 구현할 수 있습니다.

+++FX-Map
일반적으로 전체 패스(또는 패스)에 대한 전역 지식이 필요한 고급 작업 또는 누적 패스(예: 데시메이션 또는 테셀레이션 후 정점을 다시 패킹)를 수행할 때는 [Fx-맵](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/fx-map/fx-map.md) 기반 솔루션을 사용하는 것이 좋습니다. 또한 가장 쉽게 접근할 수 있으므로 처음으로 사용자 지정 처리를 하는 경우 Fx-Map을 사용할 수 있습니다. *속도가 느려질 수 있습니다*.

우선 Fx-Map을 잘 알고 있어야 합니다. 그렇지 않으면 [특정 문서](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/fx-map/fx-map.md)를 확인하세요.

Fx-Map을 사용하여 경로를 읽고 쓰는 방법에 대한 아이디어를 얻으려면 <b>*paths\_trace.sbs*</b>&#x200B;의 [미리 보기 경로](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/preview-paths/preview-paths.md) 및 <b>*paths\_polygon.sbs*</b>&#x200B;의 [Paths Polygon](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/paths-polygon/paths-polygon.md)의 구현을 살펴보는 것이 좋습니다.

+++

+++픽셀 프로세서
&quot;로컬&quot; 정보만 필요한 경우 [픽셀 프로세서](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/pixel-processor/pixel-processor.md) 솔루션이 적합합니다. 여기서 우리는 공간(요소 사이의 거리)이 아니라 위상적(함께 연결된 정점들)인 &quot;국지적&quot;을 의미한다. 이 방법은 Vertex Processor의 구현 방법입니다. 픽셀 프로세서는 제한된 양의 데이터만 액세스하는 동시에 각 픽셀의 기능이 병렬로 평가되기 때문에 일반적으로 이러한 작업을 위해 Fx-Map보다 빠릅니다. 현재 픽셀만 수정할 수 있으므로 구현 노력이 훨씬 더 중요할 수 있습니다.

구체적인 사용 사례에 따라 할 말이 너무 많기 때문에 자세히 알아보지는 않겠지만, 가장 먼저 해야 할 일은 여러분이 어디에 있는지 확인하는 것입니다.

상단($pos.y &lt; 0.5) 또는 하단($pos.y > 0.5) 부분에 있습니까? 전용 변수(예: `*isTop*`)에서 `*vert.addr*` 부동2를 만들 때 해당 값은 위쪽 부분은 `*$pos*`이고 아래쪽 부분은 `$pos - (0,0.5)`임을 기억하는 것이 좋습니다.

*vert.addr*&#x200B;에는 어떤 항목이 있습니까? 샘플을 채취하여 (W != 0)이 있는지 확인한 다음, 있다면 정확히 무엇인지 확인합니다. 헤더(W = 0.0625)(`*Read/is\_header*` 확인) 또는 정점(`Read/is\_vertex` 확인) 중 어느 것입니까? 헤더라면 문서 헤더일까요, 패스 헤더일까요? `*Read/current\_pixel\_is\_document\_header*`을(를) 사용하여 확인할 수 있습니다. 하나 또는 여러 개의 도우미 함수를 사용하여 관심 있는 내용을 일치시킵니다.

+++
