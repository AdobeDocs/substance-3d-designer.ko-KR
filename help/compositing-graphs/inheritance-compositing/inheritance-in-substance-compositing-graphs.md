---
helpx_url: "https://helpx.adobe.com/kr/substance-3d-designer/substance-compositing-graphs/inheritance-in-substance-compositing-graphs.html"
breadcrumb-title: ''
description: 상속이 Substance 합성 그래프에서 작동하여 재사용 가능한 그래프 계층 및 변형을 만드는 방법을 알아봅니다.
helpx_creative_field: ""
helpx_description: Designer > Substance graphs > Inheritance in Substance graphs
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Substance 그래프에서 상속
user-guide-description: ''
user-guide-title: ''
source-git-commit: 4f8830fa9ab6012f0a7ba5054eb171b151c44874
workflow-type: tm+mt
source-wordcount: '1681'
ht-degree: 0%

---


# Substance 그래프에서 상속

이 페이지에서는 [Substance 3D Designer](https://www.adobe.com/kr/products/substance3d-designer.html)의 [Substance 그래프](../../compositing-graphs/substance-compositing-graphs.md)에서 상속이 적용되는 방법과 상속이 그래프의 출력에 미치는 영향에 대해 설명합니다.

![상속 메서드](../../assets/inheritance-overview-1.jpg "상속 메서드"){width="1400px"}

## 개요

Substance 그래프의 모든 노드는 소스의 일부 매개 변수 값을 *상속*&#x200B;할 수 있습니다. 상속은 원본의 값을 변경하면 원본에서 상속되는 모든 노드에서 *해당 변경을 수행*&#x200B;함을 의미합니다. 이는 Substance 3D Designer이 파라메트릭 에셋을 생성하는 토대를 제공하는 기본 개념 중 하나입니다.

>[!NOTE]
>
> 상속을 설명하는 주석이 달린 프로젝트 파일은 이 설명서의 [샘플 Substance 그래프](../../compositing-graphs/sample-compositing-graphs/sample-substance-compositing-graphs.md) 섹션에서 사용할 수 있습니다.

### 상속 메서드

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![&#39;Absolute&#39; 상속 메서드 아이콘](../../assets/ds-inheritance-absolute.png "&#39;Absolute&#39; 상속 메서드 아이콘"){width="128px"}

<b>절대</b>

상속이 없습니다. 매개 변수에 대해 값이 *임의 및 로컬로* 정의됩니다.

</td>
<td style="border: 0;" valign="top">

![&#39;Relative to input&#39; 상속 메서드에 대한 아이콘](../../assets/ds-inheritance-relative-to-input.png "&#39;Relative to input&#39; 상속 메서드에 대한 아이콘"){width="128px"}

<b>입력 기준</b>

값은 노드의 *기본 입력*&#x200B;에 연결된 데이터에서 상속됩니다.

</td>
<td style="border: 0;" valign="top">

![부모 상속 메서드에 대한 아이콘](../../assets/ds-inheritance-relative-to-parent.png "부모 상속 메서드에 대한 아이콘"){width="128px"}

<b>부모에 대한 상대</b>

값은 노드 또는 그래프의 *부모*&#x200B;에서 상속됩니다.

</td>
</tr>
</table>

![상속 메서드 데모](../../assets/inheritance-overview.gif "상속 메서드 데모")

상속 메서드는 노드의 [기본 매개 변수](../../compositing-graphs/graph-parameters/graph-parameters.md)에 적용됩니다. 이 매개 변수는 모든 노드에서 해당 동작의 *기본 측면*&#x200B;을 제어하는 공통 매개 변수 집합입니다. 이러한 매개 변수에는 다음이 포함됩니다.

* **출력 크기**
* **출력 형식**(예: 비트 심도)
* **픽셀 크기**
* **픽셀 비율**
* **타일링 모드**
* **임의화**

이렇게 하면 *one* 노드의 변경이 해당 노드의 *모든 노드 다운스트림*&#x200B;의 해상도, 정밀도 및 타일링 동작에 어떤 영향을 미칠 수 있는지 알아볼 수 있습니다.

>[!WARNING]
>
> 이 페이지에서 설명하는 개념을 이해하기 위한 중요한 미리 알림: *인스턴스 노드*&#x200B;는 *고유한 개별 매개 변수 값*&#x200B;이 있는 다른 그래프의 그래프를 나타내는 [노드](../../compositing-graphs/creating-compositing-gra/graph-instances-sub-gra/graph-instances-sub-graphs.md)이며 용어 *인스턴스*&#x200B;입니다.\
> 예를 들어, 동일한 그래프에 있는 두 [Perlin 노이즈](../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/perlin-noise/perlin-noise.md) 노드는 모두 *자체 집합*&#x200B;의 매개 변수 값으로 *동일한* 소스 그래프(`noise_perlin_noise.sbs`의 `perlin_noise`)를 나타냅니다.

>[!NOTE]
>
> **출력 크기:** ![](../../assets/props-output-size-lock.jpg) 잠금 단추를 사용하여 Height 값이 너비 값과 *일치*&#x200B;하도록 합니다.\
> **임의 시드:** ![](../../assets/prop-randomise.jpg) 단추를 사용하여 임의 시드에 새 임의 값을 할당합니다.

## 변경

### 상속 메서드 변경

[속성] 패널에서 노드 속성의 [기본 매개 변수](../../compositing-graphs/graph-parameters/graph-parameters.md) 섹션에 나열된 모든 매개 변수에는 해당 레이블 반대쪽에 (아이콘) <b>상속 메서드 설정</b> 드롭다운 단추가 있습니다.\
이 단추를 사용하여 매개변수에 사용할 상속 방법을 선택할 수 있습니다.

![상속 메서드 변경](../../assets/inheritance-change.gif "상속 메서드 변경"){width="512px"}

대부분의 경우 *노드*&#x200B;의 기본 매개 변수는 노드를 함께 체인화하는 절차적 동작을 활용하기 위해 *입력에 상대적인*(으)로 설정되며, *그래프*&#x200B;의 기본 매개 변수는 *부모에 상대적인*(으)로 설정되므로 전체 매개 변수는 그래프가 사용되는 컨텍스트에 맞게 조정할 수 있습니다.

### 상속된 값 수정

[출력 크기](../../compositing-graphs/output-size/output-size.md), 픽셀 크기 또는 임의 시드 등의 일부 기본 매개 변수는 *상속된 값*&#x200B;에 상대적으로 변경될 수 있습니다.

예를 들어, Output Size 매개 변수가 *Relative to..* 상속 메서드를 사용하는 경우 값 또는 `(1, -1)`은(는) X에 대한 상속된 값보다 *위*&#x200B;이고 Y에 대한 상속된 값보다 *아래*&#x200B;인 두 해상도의 제곱을 의미합니다.

* 상속된 값: `(9, 9)`, 즉 `2^9, 2^9 = 512, 512`
* 상대 값: `(1, -1)`, 즉 `2^(9+1), 2^(9-1) = 256, 1024`

>[!NOTE]
>
> [출력 크기](../../compositing-graphs/output-size/output-size.md) 페이지는 이 중요한 기본 매개 변수에 더 자세히 포함되며, 노드의 최종 해상도를 계산하는 방법을 이해하도록 읽는 것이 좋습니다.

함수가 Base 매개 변수에 적용되면 함수의 결과도 매개 변수의 상속 메서드를 사용하여 해석됩니다.\
출력 크기 예제를 염두에 두고 상속된 해상도를 X 및 Y로 두 배로 늘리는 것을 목표로 하는 함수는 `(2, 2)` Integer2 값을 출력해야 합니다.

## 노드 및 그래프의 괄호

부모 상속 방법에 대한 상대 방법을 사용할 때는 특정 컨텍스트에서 해당 부모가 정확하게 무엇인지 이해해야 합니다.

노드의 부모는 해당 노드가 있는 *그래프*&#x200B;입니다.

그래프의 부모는 다음 위치에 있는 *컨텍스트*&#x200B;입니다.

* 해당 그래프가 다른 호스트 그래프에 *인스턴스 노드*(으)로 인스턴스화된 하위 그래프인 경우, 하위 그래프의 상위는 *인스턴스 노드*&#x200B;입니다. 해당 인스턴스 노드의 부모는 *호스트 그래프*&#x200B;입니다.
* 해당 그래프가 루트 그래프이면 상위 그래프는 *응용 프로그램 자체*&#x200B;이며 응용 프로그램이 지정된 매개 변수에 대해 설정한 값입니다. 예를 들어 그래프는 [그래프 보기의 도구 모음](../../interface/the-graph-view/the-graph-view.md)에 설정된 <b>부모 크기</b> 매개 변수에서 상속됩니다.

>[!WARNING]
>
> SBSAR(Substance 3D 에셋 파일)에 패키지를 게시할 때 상위 경로가 *그대로 적용*&#x200B;됩니다. 즉, 매개 변수를 *Absolute* 상속 메서드에 설정하면 해당 매개 변수가 게시된 에셋의 현재 값에 *잠금*&#x200B;됩니다.\
> 예를 들어 [비트맵](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/bitmap/bitmap.md) 노드 또는 [최적화 목적](../../best-practices/performance-optimization/performance-optimization-guidelines.md)에 대해 권장되지만, *명확하고 계획적인 목적*&#x200B;이 없으면 Substance 그래프에서 작업할 때 *강력하게*&#x200B;에서는 *상대...* 상속 방법을 사용하는 것이 좋습니다.

### 직접 편집

그래프 인스턴스 노드에서 [컨텍스트 편집](../../compositing-graphs/creating-compositing-gra/graph-instances-sub-gra/graph-instances-sub-graphs.md)을 사용하는 경우 그래프의 상위는 *인스턴스 노드*&#x200B;입니다. 이 경우 상속되는 그래프가 인스턴스 노드의 기본 매개 변수이므로 [그래프 보기의 도구 모음](../../interface/the-graph-view/the-graph-view.md)에 있는 <b>부모 크기</b> 설정은 *사용 안 함*&#x200B;입니다.

이 특성은 컨텍스트 편집의 *포인트*&#x200B;이며 상속 메서드를 설정하고 노드의 기본 매개 변수의 현재 값을 평가할 때 *팩토링 인*&#x200B;해야 합니다.

## 여러 입력을 사용한 상속

그래프에 여러 입력이 있는 경우 각 입력은 상속 방법에 따라 개별 입력 데이터 또는 그래프에서 상속될 수 있습니다.

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![&#39;Relative to input&#39; 상속 메서드에 대한 아이콘](../../assets/ds-inheritance-relative-to-input.png "&#39;Relative to input&#39; 상속 메서드에 대한 아이콘"){width="128px"}

<b>입력 기준</b>

입력은 그래프의 기본 매개변수에 관계없이 이산 입력 데이터에서 상속됩니다. 이는 입력당 데이터를 제어하는 데 매우 유용합니다.

</td>
<td style="border: 0;" valign="top">

![부모 상속 메서드에 대한 아이콘](../../assets/ds-inheritance-relative-to-parent.png "부모 상속 메서드에 대한 아이콘"){width="128px"}

<b>부모에 대한 상대</b>

입력은 그래프에서 상속되고, 그 입력이 받는 데이터는 그에 따라 조정된다.

</td>
<td style="border: 0;" valign="top">



</td>
</tr>
</table>

### 기본 입력

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![기본 입력 색상/회색 음영](../../assets/inheritance-primary-input-both.png){width="48px"}

</td>
<td style="border: 0;" valign="top">

![기본 입력 색상](../../assets/inheritance-primary-input-color.png){width="48px"}

</td>
<td style="border: 0;" valign="top">

![기본 입력 회색 음영](../../assets/inheritance-primary-input-grayscale.png){width="48px"}

</td>
</tr>
</table>

해당 [입력](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/input/input.md) 노드에서 **RMB**&#x200B;을 클릭하고 컨텍스트 메뉴에서 **기본 입력으로 설정** 옵션을 선택하여 입력 중 하나를 그래프의 **기본 입력**&#x200B;으로 설정할 수 있습니다.

</td>
<td style="border: 0;" valign="top">

![입력 커넥터 형식](../../assets/inheritance-primary-input.jpg "입력 커넥터 형식")

</td>
</tr>
</table>

그래프가 인스턴스 노드로 다른 그래프에 인스턴스화되면 *입력 기준*&#x200B;으로 설정된 모든 인스턴스 노드의 기본 매개 변수는 *해당 입력*&#x200B;에 연결된 데이터를 상속합니다. 인스턴스 노드의 기본 입력은 그 커넥터에서 작은 어두운 점에 의해 식별될 수 있다.

*부모 항목*(으)로 설정된 다른 입력은 기본 입력에서 상속하는 *인스턴스 노드\**에서 상속하는*&#x200B;그래프*에서 상속하는 것과 동일한 기본 매개 변수의 값을 상속합니다.

\*: 이 값은 그래프에서*&#x200B;부모에 대한 상대* 상속 방법을 사용하므로 true입니다.

## 예

아래는 상위에서 아래로 이어지는 배우들에서 설정한 다양한 상속 사례들과 상속 방법의 상호 작용을 다룬 몇 가지 예들이다.

1. 애플리케이션
1. 호스트 그래프
1. 호스트 그래프의 인스턴스 노드
1. 하위 그래프 - 즉, 인스턴스 노드에서 참조하는 그래프
1. 하위 그래프의 노드

배우에 대해 설정된 *상속 메서드*&#x200B;가 주황색으로 표시됩니다. 소스에 대한 *상속 흐름*&#x200B;이 주황색 선으로 표시됩니다.

문자는 기본 매개 변수의 *개별 집합*&#x200B;을 나타내며, 각 작업자가 상속한 데이터를 팔로우하는 데 도움이 됩니다.

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

**예제 A**

![상속 다이어그램 A](../../assets/inheritance-schematic-a.png "상속 다이어그램 A"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

**예제 B**

![상속 다이어그램 B](../../assets/inheritance-schematic-b.png "상속 다이어그램 B"){zoomable="yes"}

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

**예제 C**

![상속 다이어그램 C](../../assets/inheritance-schematic-c.png "상속 다이어그램 C"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

**예제 D**

![상속 다이어그램 D](../../assets/inheritance-schematic-d.png "상속 다이어그램 D"){zoomable="yes"}

</td>
</tr>
</table>

## 상속 문제 해결

그래프를 만들고 복잡성을 증가시키면 상속으로 인해 예기치 않은 결과가 발생할 수 있습니다. 노드의 출력에 잘못된 해상도나 정밀도(즉, 비트 심도)가 있는 경우 이러한 값의 출처를 *상속 체인 위로* 이동해야 합니다.

좋은 시작점은 노드 바로 아래에 표시된 데이터를 확인하는 것입니다. 노드 *첫 번째 출력*&#x200B;에서 출력한 이미지의 해상도, 색상 형식 및 정밀도입니다. 해결책은 간단하지만 두 번째 데이터를 세부적으로 설명할 필요가 있습니다.

* *문자 접두어*&#x200B;는 이미지의 색상 형식을 참조합니다.
  * <b>L</b>: 광도(회색 음영)
  * <b>C</b>: 색상
* *숫자*&#x200B;는 가장 낮은 정밀도에서 가장 높은 정밀도로 이미지의 비트 심도를 나타냅니다.
  * <b>8</b>: 8비트 정수(0-1에서 256단계)
  * <b>16</b>: 16비트 정수(0-1에서 65 536단계)
  * <b>16F</b>: 16비트 부동 소수점(음수 포함, 0-1을 초과하는 낮은 정밀도 값)
  * <b>32F</b>: 32비트 부동 소수점(음수 포함, 0-1을 초과하는 높은 정밀도 값)

노드에 두 개 이상의 출력이 있는 경우 다음 두 가지 방법으로 분해능과 정밀도를 확인할 수 있습니다.

* *출력 커넥터*&#x200B;에서 <b>LMB</b>를 두 번 클릭하여 [2D 보기](../../interface/2d-view/2d-view.md)에 이미지를 표시하고 2D 보기 뷰포트의 *왼쪽 아래 모서리*&#x200B;에 표시된 이미지 정보를 확인합니다
* [수준](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/levels/levels.md) 또는 [변환 2D](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/transformation-2d/transformation-2d.md) 노드를 만들고 해당 입력을 확인할 출력에 연결합니다. 노드는 기본적으로 *출력에서 상속*&#x200B;되며 노드 아래의 값을 확인할 수 있습니다.

이제 그래프의 노드 체인 위로 이동하여 예기치 않은 값이 나타나는 *첫 번째 노드*&#x200B;를 찾을 수 있습니다. 해당 Base 매개변수의 상속 방법을 확인합니다.

잘못된 것이 없고 노드가 인스턴스 노드인 경우 더 깊게 이동하여 해당 인스턴스 노드에서 참조하는 그래프를 열어야 합니다. 그래프의 출력 노드에서 시작해 업스트림으로 향하는 프로세스를 반복합니다.

### 일반적인 예

특히 *기본 입력* 개념은 쉽게 *간과되고* 상속 문제가 발생할 수 있습니다.

[Blend](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/blend/blend.md) 노드는 매우 자주 사용되기 때문에 매우 취약합니다. <b>배경</b> 입력은 기본 입력입니다.

![출력 크기 상속](../../assets/inheritance-blend.jpg "출력 크기 상속"){width="512px"}

두 입력을 혼합하는 순서에 주의해야 합니다. 필요한 혼합 모드가 가능하게 하는 경우 그래프를 아래로 유지하려는 해상도와 정밀도가 배경 입력에 연결되어야 합니다. 그렇지 않은 경우 블렌드 노드의 베이스 매개변수와 상속 방법을 조정하여 보정할 수 있습니다.
