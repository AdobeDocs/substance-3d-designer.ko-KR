---
helpx_url: ""
breadcrumb-title: ''
description: 모양 스플래터 v2 및 3D 뷰어 노드에서 3D 모양을 생성하는 SDF 함수를 제작할 수 있는 Designer에서 사용할 수 있는 SDF 함수 노드에 대해 알아봅니다.
helpx_creative_field: ""
helpx_description: ""
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: SDF 함수 작업
user-guide-description: ''
user-guide-title: ''
source-git-commit: dd03ffc77a6d09c680dcf3e1fc204e4cb86cc336
workflow-type: tm+mt
source-wordcount: '2573'
ht-degree: 0%

---


# SDF 함수 작업

버전 16.0.0에서 Substance 3D Designer은 절차적 3D 모양을 만들고 조작하는 데 사용할 수 있는 강력한 노드 세트를 만들어 SDF 함수를 제작하도록 도입했습니다.

SDF 함수는 SDF 함수 세트에서 사용 가능한 SDF 노드를 결합하는 Substance 함수 그래프로, 도구를 지원하는 노드의 전용 매개 변수에 적용됩니다.

기본 워크플로우는 다음과 같다는 점에 유의하십시오.

1. 결과를 시각화하기 위해 [3D 뷰어](../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/3d-viewer/3d-viewer.md) 노드에서 SDF 함수를 작성합니다.
2. 최종 함수 그래프(또는 [인스턴스화](../../../../glossary/glossary.md#instance-node))를 [모양 스플래터 v2](../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/shape-splatter-v2/shape-splatter-v2.md)와 같이 SDF 함수를 지원하는 노드의 SDF 함수 매개 변수에 복사합니다.

<img style="display: block; margin: auto;" src="working-with-sdf-functions.resources/working-with-sdf-mograph.gif" alt="Substance 3D Designer의 3D SDF 함수 노드 기능 모그래프" />

## SDF 함수 개요

<table style="border: none">
    <tr style="border: 0">
        <td style="border: 0; vertical-align: top">
            <p>수학 함수가 2D에서 곡선으로 플롯될 수 있는 것처럼 3D에서도 서피스로 플롯될 수 있습니다.</p><p>부호 있는 거리 필드는 공간의 임의의 점에서 서피스의 가장 가까운 점까지의 거리를 계산하여 3D 공간의 서피스를 정의하는 수학 함수입니다.</p><p>더 잘 이해하기 위해 '서명된 거리 필드'라는 이름을 세분화합니다.<ul><li><b>부호</b>은 점이 표면 앞/바깥에 있으면 함수가 양수 값을 반환하고, 점이 표면 안쪽/뒤에 있으면 음수 값을 반환하며, 점이 표면에 있으면 0을 반환합니다.</li><li><b>거리</b>은 함수가 공간의 모든 점에서 표면의 *가장 가까운* 점까지의 거리를 계산한다는 사실을 의미합니다.</li><li><b>필드</b>은 공간의 각 점에 가장 가까운 표면까지의 거리를 나타내는 해당 값이 있으므로 함수가 값 필드를 설명하는 것을 의미합니다.</li></ul></p>
        </td>
        <td style="border: 0; width: 33%; vertical-align: top">
            <img src="./working-with-sdf-functions.resources/working-with-sdf-what-is-an-sdf.gif" alt="스위핑 아이소라인을 사용하여 SDF 함수가 생성한 모양을 시각화합니다." />
        </td>
    </tr>
</table>

이러한 기능은 드로잉 서피스, 그림자 캐스팅, 컨투어 마스킹, 충돌 감지 등과 같은 컴퓨터 그래픽에 많은 응용 프로그램을 가지고 있습니다.

Substance 3D Designer에서는 SDF 함수를 사용하여 3D 모양을 절차적으로 만들고 조작합니다.

### SDF 함수 출력 및 사용 목적

SDF 함수 노드에서 단일 부동 소수점 값(가장 가까운 서피스까지의 부호 거리)을 출력합니다.

그러나 여기에는 더 많은 것이 있습니다. 호스트 노드가 정의하거나 알고 있어야 결과 모양을 조작하고 그릴 수 있는 변수의 값을 내부적으로 얻고 설정합니다.

즉, 이러한 SDF 함수에 대해 알고 있고 해당 변수를 기본적으로 통합하기 때문에 *지원 변수*&#x200B;를 사용하는 노드의 컨텍스트에서 이러한 노드를 사용해야 합니다.

노드에는 [모양 스플래터 v2](../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/shape-splatter-v2/shape-splatter-v2.md) 및 [3D 뷰어](../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/3d-viewer/3d-viewer.md)가 포함됩니다.

### Substance 함수 그래프

SDF 함수 노드는 전용 Substance 함수 그래프에서 사용되므로 해당 그래프 유형에서만 사용할 수 있습니다.
함수로 표시되어야 하는 노드 매개 변수는 &#39;함수 편집&#39; 버튼을 사용합니다.

Substance 함수 그래프에 대해 알아야 할 사항:
* Substance 그래프와 마찬가지로, 노드 커넥터는 *특수*&#x200B;입니다. 즉, 해당 유형을 나타내는 *일치하는 색상* [의 다른 커넥터에만 연결할 수 있습니다](../../function-nodes-overview/function-nodes-overview.md#color-coding).
* 노드에는 매개 변수가 없으며 입력만 있을 수 있습니다. (몇 가지 특정 예외 사항 포함)
* 그래프에는 단일 출력 노드가 있습니다. 노드를 마우스 오른쪽 단추로 클릭하고 `Set as output`을(를) 선택하여 출력 노드로 지정합니다.
* 또한 Substance 그래프와 마찬가지로 기본 빌딩 블록인 *atomic* 노드와 다른 Substance 함수 그래프를 나타내는 *instance* 노드가 있습니다.
* 그래프의 값에 대한 연산을 수행할 수 있는 별도의 연산자(대수, 논리, 비교)가 있지만 SDF 노드에는 [자체 연산자](#operators)가 있습니다

+++ SDF 함수 정의 함수 그래프의 예

![working-with-sdf-function-graph.png](working-with-sdf-functions.resources/working-with-sdf-function-graph.png)

+++

## 시작

SDF 함수를 작성하기 위해서는 먼저 노드를 시각화해야 조정하려는 노드와 매개 변수의 효과를 이해할 수 있습니다.

[3D 뷰어](../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/3d-viewer/3d-viewer.md) 노드에는 SDF 함수를 사용하여 작성된 모양을 시각화하기 위한 전용 모드가 있습니다. 노드의 <b>장면 유형</b> 매개 변수를 `SDF function`(으)로 설정하고 **함수 편집** 단추를 클릭하여 SDF 함수 자체를 호스팅할 함수 그래프를 엽니다.

이 노드는 테두리 프레임 및 아이소라인과 같이 SDF 함수의 측면을 보다 직관적이고 효율적으로 빌드할 수 있도록 시각화하기 위한 전용 기능을 제공합니다.

[실제 태양/하늘](../../../../compositing-graphs/nodes-reference-for-com/node-library/3d-view-library/hdri-tools/physical-sun-sky/physical-sun-sky.md) 노드를 사용하면 3D 뷰어에서 환경 조명을 빠르게 설정할 수 있습니다.

<img style="margin-top: 32px; margin-bottom: 32px;" src="./working-with-sdf-functions.resources/working-with-sdf-setup.gif" alt="SDF 함수 시각화를 위한 3D 뷰어 노드 설정" />

>[!TIP]
> 
> <table style="border: none"><tr style="border: none"><td style="border: none; vertical-align: top"><p>모든 SDF 함수 노드와 입력 커넥터에는 해당 노드의 목적과 사용 방법에 대해 자세히 알 수 있는 도구 설명이 있습니다.</p><p>꼭 확인해 보세요!</p></td><td style="border: none; width: 33%; vertical-align: top"><img src="./working-with-sdf-functions.resources/working-with-sdf-tooltips.png" alt="SDF 함수 노드의 입력 커넥터에 대한 도구 설명입니다." /></td></tr></table>

### 노드 값 설정

Substance 함수 그래프의 모든 노드와 마찬가지로 SDF 함수 노드에는 매개변수가 없고 매개변수로 사용되는 입력 커넥터만 있습니다.

이러한 입력의 값을 설정하려면 **Float**, **Float3** 및 **Integer3**&#x200B;과 같은 [상수 노드](../../atomic-function-nodes/constant-nodes/constant-nodes.md)를 사용할 수 있습니다.\
노드 메뉴를 통해 일반적인 방법으로 이러한 연결을 만들거나, 커넥터에서 새 연결을 드래그하여 일치하는 유형의 필터링된 노드 목록을 활용할 수 있습니다.

SDF 함수 노드의 대부분의 입력 커넥터에는 해당 도구 설명에 표시된 기본값이 있습니다.

<img style="margin-top: 32px; margin-bottom: 32px" src="working-with-sdf-functions.resources/working-with-sdf-constants.gif" alt="SDF 기본 요소를 편집하는 데 사용되는 상수 노드입니다." />

>[!TIP]
> 
> <table style="border: none"><tr style="border: none"><td style="border: none; vertical-align: top"><p>일부 값을 항상 표시할 필요가 없으면 <code>D</code> 키를 사용하여 노드를 고정하여 공간을 절약하고 그래프를 정리합니다.</p><p>주석을 사용하여 값을 추적할 수도 있습니다.</p></td><td style="border: none; width: 67%; vertical-align: top"><img src="./working-with-sdf-functions.resources/working-with-sdf-docked-nodes.png" alt="SDF 함수 노드의 입력 커넥터에 대한 도구 설명입니다." /></td></tr></table>


### 테두리 프레임

<table style="border: none">
    <tr style="border: none">
        <td style="border: none; vertical-align: top">
            <p>테두리 프레임은 SDF 함수가 <a href="../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/shape-splatter-v2/shape-splatter-v2.md">모양 스플래터 v2</a> 노드에서 평가되고 그려지는 <i>테두리</i>를 정의하는 3D 공간의 상자입니다.</p><p>테두리 프레임이 너무 작으면 모양의 일부가 트리밍될 수 있습니다. 너무 크면 불필요한 계산과 더 긴 처리 시간을 초래할 수 있다.</p><p><b>테두리 프레임</b> 매개 변수를 사용하면 테두리 프레임을 시각화할 수 있습니다. 그런 다음 <b>테두리 프레임 크기</b> 매개 변수의 값을 변경하여 테두리 프레임의 크기를 조정할 수 있습니다.</p><p><b>프레임 밖의 색상 입히기</b> 매개 변수를 사용하여 테두리 프레임 바깥의 영역을 밝은 빨간색으로 시각화하면 그에 따라 프레임을 조정할 수 있습니다.</p>
        </td>
        <td style="border: none; width: 33%; vertical-align: top">
            <img src="./working-with-sdf-functions.resources/working-with-sdf-bounding-frame.jpg" alt="3D 뷰어 노드의 테두리 프레임 기능(SDF 함수)." />
        </td>
    </tr>
</table>

### 등치선

<table style="border: none">
    <tr style="border: none">
        <td style="border: none; vertical-align: top">
            <p>모양을 변형하려면 그려진 공간을 *변형해야 하기 때문에 일부 변형 후에 사용되는 노드의 결과는 놀라운 일일 수 있습니다.이러한 경우 공간 자체를 시각화하는 것이 도움이 되며, <i>모양의 거리 필드를 시각화하는</i>으로 수행할 수 있습니다.<br></p><p>이를 위해 3D 뷰어 노드는 모양의 표면으로부터의 지정된 거리를 나타내는 반복되는 윤곽선인 <i>아이소라인</i>을 사용합니다. <b>SDF 등치선</b> 매개 변수를 사용하면 해당 시각화를 사용할 수 있습니다.<br>아이소라인은 <b>SDF 아이소라인 위치</b> 매개 변수에 지정된 Height에 있는 수평 평면에 그려집니다.</p><p>모양에 적용된 변형에 의해 아이소라인이 어떻게 변형되는지 확인하는 것은 모양 자체가 어떻게 변형되는지 이해하고 그에 따라 노드의 매개 변수를 조정하는 데 도움이 될 수 있습니다.</p>
        </td>
        <td style="border: none; width: 33%; vertical-align: top">
            <img src="./working-with-sdf-functions.resources/working-with-sdf-isolines.jpg" alt="3D 뷰어 노드의 테두리 프레임 기능(SDF 함수)." />
        </td>
    </tr>
</table>

## SDF 함수 노드 범주

SDF 함수 노드는 기능 및 목적에 따라 라이브러리에서 분류됩니다.

필요한 만큼 라이브러리 보기를 만들어 모든 것을 유지하면서 SDF 함수 도구 세트를 범주별로 정렬하는 방식으로 작업 영역을 구성할 수 있습니다. **창 > 새 라이브러리** 보기로 이동하여 라이브러리의 개별 보기를 추가합니다.

+++ 작업 영역 예

![working-with-sdf-workspace.png](working-with-sdf-functions.resources/working-with-sdf-workspace.png)

+++

### 기본 도형

구, 상자, 원통 등과 같은 기본 모양을 만들 수 있는 SDF 함수의 기본 구성 요소입니다.

+++ 노드

[닫힌 원뿔](./sdf-functions-primitives/3d-sdf-capped-cone/3d-sdf-capped-cone.md)\
[닫힌 원뿔(2점)](././sdf-functions-primitives/3d-sdf-capped-cone-2-points/3d-sdf-capped-cone-2-points.md)\
[닫힌 원환](./sdf-functions-primitives/3d-sdf-capped-torus/3d-sdf-capped-torus.md)\
[캡슐](./sdf-functions-primitives/3d-sdf-capsule/3d-sdf-capsule.md)\
[원뿔](./sdf-functions-primitives/3d-sdf-cone/3d-sdf-cone.md)\
[큐브](./sdf-functions-primitives/3d-sdf-cube/3d-sdf-cube.md)\
[원통](./sdf-functions-primitives/3d-sdf-cylinder/3d-sdf-cylinder.md)\
[원통(2포인트)](./sdf-functions-primitives/3d-sdf-cylinder-2-points/3d-sdf-cylinder-2-points.md)\
[Ellipsoid](./sdf-functions-primitives/3d-sdf-ellipsoid/3d-sdf-ellipsoid.md)\
[길쭉한 실린더](./sdf-functions-primitives/3d-sdf-elongated-cylinder/3d-sdf-elongated-cylinder.md)\
[지표 평면](./sdf-functions-primitives/3d-sdf-ground-plane/3d-sdf-ground-plane.md)\
[헬릭스](./sdf-functions-primitives/3d-sdf-helix/3d-sdf-helix.md)\
[육각형 프리즘](./sdf-functions-primitives/3d-sdf-hexagonal-prism/3d-sdf-hexagonal-prism.md)\
[무한 평면](./sdf-functions-primitives/3d-sdf-infinite-plane/3d-sdf-infinite-plane.md)\
[평면](./sdf-functions-primitives/3d-sdf-plane/3d-sdf-plane.md)\
[피라미드](./sdf-functions-primitives/3d-sdf-pyramid/3d-sdf-pyramid.md)\
[피라미드 정사각형](./sdf-functions-primitives/3d-sdf-pyramid-square/3d-sdf-pyramid-square.md)\
[록](./sdf-functions-primitives/3d-sdf-rock/3d-sdf-rock.md)\
[구](./sdf-functions-primitives/3d-sdf-sphere/3d-sdf-sphere.md)\
[토러스](./sdf-functions-primitives/3d-sdf-torus/3d-sdf-torus.md)

+++

### 연산자

이러한 노드를 사용하면 프리미티브로 만든 모양을 결합하고 수정할 수 있습니다. 여기에는 다음이 포함됩니다.
* [합집합](sdf-functions-operators/3d-sdf-op-union/3d-sdf-op-union.md), [교차](sdf-functions-operators/3d-sdf-op-intersection/3d-sdf-op-intersection.md) 및 [빼기](sdf-functions-operators/3d-sdf-op-subtraction/3d-sdf-op-subtraction.md)와 같이 모양을 다양한 방법으로 결합할 수 있는 **직선 부울** 연산자
* 모양을 혼합 효과와 결합할 수 있는 [라운딩](sdf-functions-operators/3d-sdf-op-rounding/3d-sdf-op-rounding.md) 및 [형태](sdf-functions-operators/3d-sdf-op-morph/3d-sdf-op-morph.md)와 같은 **변형 부울** 연산자
* [셸](sdf-functions-operators/3d-sdf-op-shell/3d-sdf-op-shell.md) 및 [대칭](sdf-functions-operators/3d-sdf-op-symmetry/3d-sdf-op-symmetry.md)과 같이 모양을 수정 및/또는 복제할 수 있는 **기타 특수** 연산자

+++ 노드

[교차](./sdf-functions-operators/3d-sdf-op-intersection/3d-sdf-op-intersection.md)\
[교차점 매끄럽게](./sdf-functions-operators/3d-sdf-op-intersection-smooth/3d-sdf-op-intersection-smooth.md)\
[교차 표면](./sdf-functions-operators/3d-sdf-op-intersection-surface/3d-sdf-op-intersection-surface.md)\
[형태](./sdf-functions-operators/3d-sdf-op-morph/3d-sdf-op-morph.md)\
[미러링 반복](./sdf-functions-operators/3d-sdf-op-repeat-mirror/3d-sdf-op-repeat-mirror.md)\
[반올림](./sdf-functions-operators/3d-sdf-op-rounding/3d-sdf-op-rounding.md)\
[셸](./sdf-functions-operators/3d-sdf-op-shell/3d-sdf-op-shell.md)\
[빼기](./sdf-functions-operators/3d-sdf-op-subtraction/3d-sdf-op-subtraction.md)\
[빼기 매끄럽게](./sdf-functions-operators/3d-sdf-op-subtraction-smooth/3d-sdf-op-subtraction-smooth.md)\
[대칭](./sdf-functions-operators/3d-sdf-op-symmetry/3d-sdf-op-symmetry.md)\
[공용 구조체](./sdf-functions-operators/3d-sdf-op-union/3d-sdf-op-union.md)\
[공용 모따기](./sdf-functions-operators/3d-sdf-op-union-chamfer/3d-sdf-op-union-chamfer.md)\
[통합 매끄럽게](./sdf-functions-operators/3d-sdf-op-union-smooth/3d-sdf-op-union-smooth.md)

+++

### 변환

모양은 [변환](sdf-functions-transforms/3d-sdf-transform-offset/3d-sdf-transform-offset.md), [회전](sdf-functions-transforms/3d-sdf-transform-rotate/3d-sdf-transform-rotate.md), [크기 조정](sdf-functions-transforms/3d-sdf-transform-scale/3d-sdf-transform-scale.md), [비틀림](sdf-functions-transforms/3d-sdf-transform-twist/3d-sdf-transform-twist.md) 등과 같은 다양한 방법으로 변형할 수 있습니다.
이러한 노드를 사용하면 서피스가 정의된 *공간 자체를 변환*&#x200B;하여 이러한 변환을 수행할 수 있습니다.

해당 공간을 `P`이라고 합니다. 다음 섹션으로 이동하여 이것이 의미하는 것과 공간 변환이 작동하는 방식에 대해 자세히 알아보세요.

+++ 노드

[굽히기](./sdf-functions-transforms/3d-sdf-transform-bend/3d-sdf-transform-bend.md)\
[연장](./sdf-functions-transforms/3d-sdf-transform-elongate/3d-sdf-transform-elongate.md)\
[뒤집기](./sdf-functions-transforms/3d-sdf-transform-flip/3d-sdf-transform-flip.md)\
[오프셋](./sdf-functions-transforms/3d-sdf-transform-offset/3d-sdf-transform-offset.md)\
[오프셋 P](./sdf-functions-transforms/3d-sdf-transform-offset-p/3d-sdf-transform-offset-p.md)\
[회전](./sdf-functions-transforms/3d-sdf-transform-rotate/3d-sdf-transform-rotate.md)\
[P](./sdf-functions-transforms/3d-sdf-transform-rotate-p/3d-sdf-transform-rotate-p.md) 회전\
[크기 조절](./sdf-functions-transforms/3d-sdf-transform-scale/3d-sdf-transform-scale.md)\
[비틀기](./sdf-functions-transforms/3d-sdf-transform-twist/3d-sdf-transform-twist.md)

+++

### 재질

SDF 함수를 사용하여 만든 모양에 기본 재질 관리를 사용할 수 있습니다.

3D 뷰어 노드에서 직접 시각화에 사용하거나 모양 스플래터 v2 노드의 재질 작업을 위한 기반으로 사용할 기본 재질 속성(색상, 거칠기 및 금속도)을 정의할 수 있습니다.\
모양의 다른 부분에 재질 ID를 지정하여 분리할 수도 있습니다.

[아래](#material-id) 노드의 응용 프로그램에 대해 자세히 알아보세요.

+++ 노드

* [재질 ID 설정](./sdf-functions-material/set-id/set-id.md)
* [재질 설정](./sdf-functions-material/set-material/set-material.md)
* [색상 설정](./sdf-functions-material/set-color/set-color.md)
* [금속 설정](./sdf-functions-material/set-metalness/set-metalness.md)
* [거칠음 설정](./sdf-functions-material/set-roughness/set-roughness.md)

+++

## &#39;P&#39; 입력

우리가 오프셋이나 회전과 같은 변형을 모양에 적용할 때, 우리는 실제로 그 모양이 정의되는 공간을 변형시킨다.

변형을 다른 모양에 전파하려면(예: 여러 모양을 동일한 방식으로 회전하려는 경우) 모든 모양이 동일한 변형 공간을 사용하는지 확인해야 합니다.

변환된 공간은 대부분의 SDF 노드에서 찾을 수 있는 전용 `P` 입력을 사용하여 노드 간에 공유됩니다.\
&#39;P&#39;는 월드 공간 **P**&#x200B;위치: 월드 공간에서 한 점의 좌표를 나타내는 3D 벡터입니다.

[오프셋 P](sdf-functions-transforms/3d-sdf-transform-offset-p/3d-sdf-transform-offset-p.md) 및 [회전 P](sdf-functions-transforms/3d-sdf-transform-rotate-p/3d-sdf-transform-rotate-p.md) 노드는 공간을 변형하며 해당 변형을 상속해야 하는 모든 노드에 전파할 수 있도록 합니다.\
예를 들어 여러 모양을 같은 P 회전 노드에 해당 `P` 입력을 연결하여 함께 회전할 수 있습니다.

이것은 단지 편의의 문제가 아니라, 그것은 SDF 노드들이 공간에서 같은 위치들로 작동하도록 확실히 하고 있다.

이에 대한 예시는 다음과 같습니다.

![working-with-sdf-p-input.gif](working-with-sdf-functions.resources/working-with-sdf-p-input.gif)

구를 반복하여 공간을 3D 격자선으로 시각화합니다. *공백 반복*&#x200B;에 의해 반복됩니다.\
공유 `P`이(가) 없으면 굽은 원통은 구가 사용하는 반복 공간을 사용합니다.\
공유 `P`을(를) 사용하면 공유 회전된 공간에서 모양을 올바르게 정의할 수 있습니다.</p>

## &#39;모양 스플래터 v2&#39; 노드에서 SDF 함수 사용

3D 뷰어 노드의 컨텍스트에서 SDF 함수를 완료하면 전체 함수를 복사하여 [모양 스플래터 v2](../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/shape-splatter-v2/shape-splatter-v2.md) 노드에 붙여넣어 해당 노드의 모양 생성기로 사용할 수 있습니다.

**모양 유형** 매개 변수를 `SDF function`(으)로 설정한 다음 **패턴 SDF 함수** 매개 변수로 이동하고 **함수 편집** 단추를 클릭하여 매개 변수의 함수 그래프를 엽니다.
그런 다음 3D 뷰어 노드에서 복사한 함수를 해당 그래프에 붙여넣을 수 있습니다. (함수 그래프의 출력 노드를 다시 설정해야 합니다.)

3D 뷰어 노드에서 사용하던 [테두리 프레임](#the-bounding-frame)과 일치하도록 **SDF 테두리 프레임 크기** 매개 변수를 조정하고 모양이 제대로 그려졌는지 확인하십시오.

![working-with-sdf-shape-splatter-v2.png](working-with-sdf-functions.resources/working-with-sdf-shape-splatter-v2.png)\
**모양 유형**&#x200B;이 `SDF function`(으)로 설정된 *모양 튄 v2.**SDF 경계 프레임 크기**가 모양에 맞게 조정되었습니다.*

>[!TIP]
> 
> SDF 함수를 쉽게 다시 사용하려면 새 Substance 함수 그래프에 복사하고 해당 그래프를 3D 뷰어 및 모양 스플래터 v2 노드 모두에서 **인스턴스 노드**&#x200B;로 사용하십시오.
> 
> 이를 통해 다음과 같은 여러 이점을 얻을 수 있습니다.
> * 함수에 대한 모든 업데이트는 해당 함수를 다시 복사하여 붙여 넣을 필요 없이 두 노드에 모두 반영됩니다. 이는 복잡한 모양의 경우 수명의 질을 크게 향상시킵니다.
> * 그래프에는 인스턴스 노드에 표시될 설명적인 이름이 있을 수 있으므로 자체 SDF 모양 라이브러리를 사용하여 더 쉽게 관리할 수 있고 그래프의 가독성이 높아집니다.
> * [Get](../../atomic-function-nodes/get-nodes/get-nodes.md) 노드에 사용할 수 있는 함수 그래프의 입력을 만들 수 있습니다. 이러한 입력은 인스턴스 노드에 입력 커넥터로 표시되며 쉽게 모양을 변경할 수 있습니다.

### 자료 ID

SDF 모양에는 재질 ID가 할당될 수 있습니다. 이 값은 모양의 일부를 구별하고 [3D 뷰어](../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/3d-viewer/3d-viewer.md) 및 [모양 스플래터 v2](../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/shape-splatter-v2/shape-splatter-v2.md) 노드에서 다른 재질을 할당하는 데 사용할 수 있는 정수 값입니다.

아래 예제와 같이 재질 ID가 다른 서피스는 블렌딩된 모양에서 하드 에지로 분할됩니다.

특정 재질 ID로 태그를 지정할 모양의 부분 뒤에 [재질 ID 설정](./sdf-functions-material/set-id/set-id.md) 노드를 사용하고, [정수](../../atomic-function-nodes/constant-nodes/constant-nodes.md) 상수 노드를 사용하여 원하는 재질 ID 값을 설정합니다.\
3D 뷰어 노드에서 **출력** 매개 변수를 `Material ID`(으)로 설정하여 모양의 재질 ID를 시각화합니다.

![working-with-sdf-material-id.png](working-with-sdf-functions.resources/working-with-sdf-material-id-01.png)\
*오른쪽에 있는 두 3D 뷰어 노드의 출력은 모양(왼쪽)과 해당 질감 ID(오른쪽)를 표시하도록 합성되어 혼합 모양에서 질감 ID가 분할되는 동안 질감이 보간되는 방법을 보여줍니다.*

Material ID는 Shape 스플래터 v2 컴패니언 노드에서 활용할 수 있습니다.
* [모양 스플래터 v2 매퍼](../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/shape-splatter-v2-mapper-color/shape-splatter-v2-mapper-color.md) 노드는 이러한 재질 ID를 사용하여 다른 패턴을 할당할 수 있습니다.
* [마스킹할 모양 스플래터 v2](../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/shape-splatter-v2-to-mask/shape-splatter-v2-to-mask.md)는 해당 재질 ID에 따라 모양의 일부를 마스킹할 수 있습니다.

<table style="border: none; margin-top: 32px">
    <tr style="border: 0">
        <td style="border: 0; width: 33%">
            <img src="./working-with-sdf-functions.resources/working-with-sdf-material-id-06.jpg" alt="모양 스플래터 v2 매퍼 색상 노드의 색상 매핑에 사용할 SDF 재질 ID입니다."/><i>색상 매핑에 사용되는 재질 ID<br>모양 스플래터 v2 매퍼 색상</i>
        </td>
        <td style="border: 0; width: 33%">
            <img src="./working-with-sdf-functions.resources/working-with-sdf-material-id-04.jpg" alt="모양 스플래터 v2 매퍼 색상 노드의 삼면형 매핑을 위한 SDF 재질 ID입니다."/><i>모양 스플래터 v2 매퍼 색상의 삼각 매핑에 사용되는 재질 ID<br></i>
        </td>
        <td style="border: 0; width: 33%">
            <img src="./working-with-sdf-functions.resources/working-with-sdf-material-id-05.jpg" alt="모양 스플래터 v2에서 마스크 노드로 마스킹을 위한 SDF 재질 ID입니다."/><br><i>마스킹에 사용되는 재질 ID<br>모양 스플래터 v2에서 마스킹</i>
        </td>
    </tr>
</table>

### 색상, 거칠음 및 금속성

[색상 설정](./sdf-functions-material/set-color/set-color.md), [거칠기 설정](./sdf-functions-material/set-roughness/set-roughness.md) 및 [금속성 설정](./sdf-functions-material/set-metalness/set-metalness.md) 노드를 사용하면 SDF 함수의 모양에 대해 이러한 재질 특성을 정의할 수 있습니다.

그런 다음 [모양 스플래터 v2](../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/shape-splatter-v2/shape-splatter-v2.md) SDF 함수에서 해당 노드를 모양 유형으로 사용할 때 이러한 재질 특성을 노드의 **SDF 색상**, **SDF 거칠기** 및 **SDF 금속도** 출력에서 맵으로 사용할 수 있습니다. 이러한 맵들은 다른 노드들을 사용하여 보다 복잡한 재료 작업을 위한 베이스 역할을 할 수 있다.

재질 ID와는 달리, 아래 예에서 볼 수 있듯이 값은 그레이디언트로서 블렌딩된 모양 간에 *보간됨*&#x200B;입니다.

<table style="border: none; margin-top: 32px">
    <tr style="border: 0">
        <td style="border: 0; width: 33%">
            <img src="./working-with-sdf-functions.resources/working-with-sdf-color.jpg" alt="모양 스플래터 v2 노드의 SDF 색상 출력입니다."/><i>SDF 색상 출력</i>
        </td>
        <td style="border: 0; width: 33%">
            <img src="./working-with-sdf-functions.resources/working-with-sdf-roughness.jpg" alt="모양 스플래터 v2 노드의 SDF 거칠음"/><br><i>SDF 거칠음 출력</i>
        </td>
        <td style="border: 0; width: 33%">
            <img src="./working-with-sdf-functions.resources/working-with-sdf-metalness.jpg" alt="모양 스플래터 v2 노드의 SDF 금속성입니다."/><i>SDF metalness 출력</i>
        </td>
    </tr>
</table>

### 재질 샘플

<table style="border: none">
    <tr style="border: none">
        <td style="border: none; vertical-align: top">
            <p><b>녹슨 볼트</b> <a href="../../../../compositing-graphs/creating-compositing-gra/material-samples/material-samples.md">재료 샘플</a>은 모양 스플래터 v2 노드의 컨텍스트에서 적용된 SDF 함수로 이동할 수 있습니다.</p><p>그래프는 구조, 노드 설정 및 SDF 함수 설정을 단계별로 안내하기 위해 구성 및 주석 처리됩니다.</p><p>또한 <i>완전히 편집 가능한</i>이므로 샌드박스로 사용하여 모양 스플래터 v2와 SDF 함수 도구 세트를 더 자세히 이해할 수 있습니다. 원하는 만큼 샘플 그래프를 만들 수 있으므로 자유롭게 사용해 보세요!</p>
        </td>
        <td style="border: none; width: 20%; vertical-align: top; text-align: right">
            <img src="./working-with-sdf-functions.resources/working-with-sdf-functions-material-sample.png" alt="3D 뷰어 노드의 테두리 프레임 기능(SDF 함수)." />
        </td>
    </tr>
</table>
