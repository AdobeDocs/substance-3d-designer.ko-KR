---
helpx_url: ""
breadcrumb-title: ''
description: Substance 3D Designer 버전 16.0의 릴리스 정보를 검토하여 새로운 기능, 개선 사항 및 버그 수정에 대해 알아보십시오.
helpx_creative_field: ""
helpx_description: Designer > Release Notes > Version 16.0
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 버전 16.0
user-guide-description: ''
user-guide-title: ''
source-git-commit: dd03ffc77a6d09c680dcf3e1fc204e4cb86cc336
workflow-type: tm+mt
source-wordcount: '2246'
ht-degree: 0%

---


# 버전 16.0

이 16.0 버전에서는 새로운 모양 스플래터와 SDF 노드를 사용하여 패턴 분산 및 조작을 위한 더 창의적인 워크플로우를 도입했습니다. 또한 기본적으로 OpenPBR을 지원하며 3D 보기의 변위 설정을 개선합니다.

*출시일: 2026년 4월 14일*

<img src="./version-16-0.resources/version-16-0-banner.jpg" alt="Substance 3D Designer 버전 16.0 배너" style="margin-top: 32px; margin-bottom: 32px">

<a name="shape-splatter-v2-nodes"></a>

## 모양 스플래터 v2 노드

### 모양을 분산하는 새로운 방법

새로운 [모양 스플래터 v2](../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/shape-splatter-v2/shape-splatter-v2.md) 노드는 기본적으로 *충돌 없음*&#x200B;인 **더 많은 모양 배포 방법**(포아송 디스크, 유니폼)으로 지금까지 어려웠던 복잡한 분산 동작을 잠금 해제하고 **밀도 맵**&#x200B;를 사용하여 특정 영역의 *셰이프 정리*&#x200B;를 제어합니다.\
고급 사용자는 함수 그래프로 정의된 *사용자 지정 분포*&#x200B;를 설정할 수 있습니다.

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="width: 33%; border: 0">
            <img src="../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/shape-splatter-v2/shape-splatter-v2.resources/shape-splatter-v2-3d-distribution-poisson.gif" alt="모양 스플래터 v2: 포아송 분포" /><br><i>포아송 분포</i>
        </td>
        <td style="width: 33%; border: 0">
            <img src="../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/shape-splatter-v2/shape-splatter-v2.resources/shape-splatter-v2-3d-distribution-uniform.gif" alt="모양 스플래터 v2: 균일 분포" /><br><i>균일 분포</i>
        </td>
        <td style="width: 33%; border: 0">
            <img src="../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/shape-splatter-v2/shape-splatter-v2.resources/shape-splatter-v2-density-map.gif" alt="밀도 맵" /><br><i>모양 스플래터 v2: 밀도 맵</i>
        </td>
    </tr>
</table>

### 3D 모양

흩어진 모양은 이제 모든 XYZ 축을 기준으로 이동, 회전 및 크기 조정이 가능한 **3D 개체**&#x200B;입니다.

큐브, 구, 원기둥과 같은 **간단한 기본 모양** 또는 *Height 맵을 돌출시키거나* *3D SDF 모양을 제작하여&#x200B;**복잡한 사용자 정의 모양**을 사용하세요*. (자세한 내용은 아래를 참조하세요.)

이렇게 하면 보드 전체에 걸쳐 더 역동적이고, 더 다양하고, 더 믿을 수 있는 산산이 나타납니다. 또한 이제 3D 모양을 뒤집어 변형에 맞게 용도를 변경할 수 있습니다. (환경 예술가님, 고객님을 뵙겠습니다!)

<table style="margin-top: 32px; margin-bottom: 32px; border: none">
    <tr style="border: 0">
        <td style="width: 33%; border: 0">
            <img src="../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/shape-splatter-v2/shape-splatter-v2.resources/shape-splatter-v2-3d-rotation.gif" alt="모양 스플래터 v2: 무작위 3D 회전" /><br><i>임의 3D 회전</i>
        </td>
        <td style="width: 33%; border: 0">
            <img src="../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/shape-splatter-v2/shape-splatter-v2.resources/shape-splatter-v2-shape-extrusion.gif" alt="모양 스플래터 v2: 모양 돌출" /><br><i>모양 돌출</i>
        </td>
        <td style="width: 33%; border: 0">
            <img src="../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/shape-splatter-v2/shape-splatter-v2.resources/shape-splatter-v2-sdf.jpg" alt="모양 스플래터 v2: 3D SDF 모양" /><br><i>3D SDF 모양</i>
        </td>
    </tr>
</table>

### 컴패니언 노드

모양 스플래터 v1 노드 패밀리와 마찬가지로 모양 스플래터 v2에는 자체 코호트의 동반 노드가 제공됩니다.

[모양 스플래터 v2 매퍼](../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/shape-splatter-v2-mapper-color/shape-splatter-v2-mapper-color.md) 노드를 사용하면 여러 텍스처를 매핑하기 위한 *삼면체 투영* 및 *재질 ID*&#x200B;를 지원하여 흩어진 3D 모양의 텍스처를 투영할 수 있습니다. 텍스처 오프셋 및 색상 변화에 대해 전역적으로 또는 모양별로 결과를 조정할 수 있습니다.\
다시 한 번 고급 사용자는 함수 그래프로 정의된 *사용자 지정 텍스처 매핑*&#x200B;을 설정할 수 있습니다.

[마스킹할 모양 스플래터 v2](../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/shape-splatter-v2-to-mask/shape-splatter-v2-to-mask.md)는 모양 및/또는 재질 ID의 특정 선택을 위한 마스크를 만들어 그래프 하류의 모양을 더 세분화하여 사용할 수 있습니다.

<table style="margin-top: 32px; margin-bottom: 32px; border: none">
    <tr style="border: 0">
        <td style="width: 33%; border: 0">
            <img src="../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/shape-splatter-v2-mapper-color/shape-splatter-v2-mapper-color.resources/shape-splatter-v2-mapper-color-tiling.gif" alt="모양 스플래터 v2 색상 매퍼: 삼면 매핑" /><br><i>삼평면 매핑</i>
        </td>
        <td style="width: 33%; border: 0">
            <img src="../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/shape-splatter-v2-mapper-color/shape-splatter-v2-mapper-color.resources/shape-splatter-v2-mapper-color-normal.gif" alt="모양 스플래터 v2 색상 매퍼: 표준 매핑" /><br><i>표준 매핑</i>
        </td>
        <td style="width: 33%; border: 0">
            <img src="../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/shape-splatter-v2-mapper-color/shape-splatter-v2-mapper-color.resources/shape-splatter-v2-mapper-color-matID-02.jpg" alt="모양 스플래터 v2 색상 매퍼: SDF 모양에서 재질 ID별 매핑" /><br><i>SDF 모양에서 재질 ID별 매핑</i>
        </td>
    </tr>
</table>

### 그리드 아틀라스

<table>
    <tr style="vertical-align: top; border: 0">
        <td style="border: 0">
            <p>사용자 정의 패턴은 모양 스플래터 v2 노드에 별도로 제공되거나 그리드 아틀라스에 압축되어 보다 학습되고 효율적인 워크플로우를 수행할 수 있습니다.</p><p>새로운 <a href="../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/grid-atlas-color/grid-atlas-color.md">그리드 아틀라스</a> 노드 덕분에 패킹 패턴이 단순화되었습니다.</p>
        </td>
        <td style="text-align: right; width: 33%; margin-left: 32px; border: 0">
            <img src="../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/grid-atlas-color/grid-atlas-color.resources/grid-atlas-color-graph.png" alt="그리드 아틀라스 색상 노드" />
        </td>
    </tr>
</table>

<a name="3d-sdf-nodes"></a>

### 재질 샘플

<table style="border: none">
    <tr style="border: none">
        <td style="border: none; vertical-align: top">
            <p><b>녹슨 볼트</b> <a href="../../compositing-graphs/creating-compositing-gra/material-samples/material-samples.md">재질 샘플</a>을 사용하여 모양 스플래터 v2 노드 및 해당 기능을 사용할 수 있습니다.</p><p>그래프는 구조, 노드 설정 및 기법을 안내하기 위해 구성되고 주석이 달려 있습니다.</p><p>또한 <i>완전히 편집 가능한</i>이므로 샌드박스로 사용하여 모양 스플래터 v2 도구 세트를 더 자세히 이해할 수 있습니다. 원하는 만큼 샘플 그래프를 만들 수 있으므로 자유롭게 사용해 보세요!</p>
        </td>
        <td style="border: none; width: 20%; vertical-align: top; text-align: right">
            <img src="../../function-graphs/nodes-reference-for-fun/function-node-library/function-nodes-sdf-functions/working-with-sdf-functions.resources/working-with-sdf-functions-material-sample.png" alt="3D 뷰어 노드의 테두리 프레임 기능(SDF 함수)." />
        </td>
    </tr>
</table>

## 3D SDF 노드(서명된 거리 필드)

<table>
    <tr style="vertical-align: top; width: 75%; border: 0">
        <td style="border: 0">
            <p>Designer 16.0에는 SDF 함수 작성을 위한 방대한 노드 카탈로그를 사용하여 함수 그래프에 3D 모양을 생성하는 강력한 방법이 추가되었습니다.</p><p>서명된 거리 필드는 수학적으로 정의된 서피스에 대한 거리로 공간을 표현합니다. 다양한 연산자를 사용하여 이러한 표면이 변형되고 결합됨에 따라 복잡성이 증가하는 모양을 정의하는 데 사용할 수 있습니다.</p>
        </td>
        <td style="text-align: right; width: 25%; margin-left: 32px; border: 0">
            <img src="./version-16-0.resources/version-16-0-SDFFunctionsBreakdown.gif" alt="SDF 함수로 모양 만들기" />
        </td>
    </tr>
</table>

### 3D SDF 함수 제작

SDF 함수는 다음 4개 범주의 [새 노드 집합](../../function-graphs/nodes-reference-for-fun/function-node-library/function-node-library.md#sdf-functions)과 관련되어 있습니다.

* **프리미티브**&#x200B;는 기본 구성 요소이며, 필요에 따라 조정할 수 있는 몇 가지 컨트롤을 사용하여 간단하게 조정할 수 있는 모양을 생성합니다.
* **연산자**&#x200B;는 간단한 부울 연산자에서 형태, 셸 및 대칭에 이르기까지 노드에 따라 직접적이거나 복잡한 방식으로 모양을 결합하거나 복제하며, 어떤 종류의 3D 모양을 얻을 수 있는지 그 가능성을 극적으로 확장합니다
* **변형**&#x200B;을 사용하면 모양의 위치, 회전 및 크기를 원하는 대로 조정할 수 있으며 굽히기, 비틀기 및 신장을 사용할 수 있습니다.
* **재질** 노드를 사용하면 [모양 스플래터 v2](../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/shape-splatter-v2/shape-splatter-v2.md) 노드 패밀리에서 모양을 마스킹하거나 색칠하는 데 사용할 수 있는 색상 및 재질 ID와 같은 몇 가지 기본 재질 특성을 설정할 수 있습니다.

>[!INFO]
> 
> 이러한 SDF 함수 작업을 시작하려면 [노드 작업](../../function-graphs/nodes-reference-for-fun/function-node-library/function-nodes-sdf-functions/working-with-sdf-functions.md) 페이지로 이동하십시오.

<img style="display: block; margin: auto" src="../../function-graphs/nodes-reference-for-fun/function-node-library/function-nodes-sdf-functions/working-with-sdf-functions.resources/working-with-sdf-mograph.gif" alt="SDF 함수 노드" />

명확하고 읽기 쉬운 아이콘이 있는 경량 SDF 함수를 사용하면 3D 도구를 생각보다 쉽게 구축할 수 있습니다. 특히 도구 세트에 이 추가 기능을 사용하면 더욱 쉽습니다.

### 3D 뷰어 노드

3D SDF 함수를 제작할 때는 3D 공간에서 결과 모양을 시각화해야 합니다. [3D 뷰어 노드](../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/3d-viewer/3d-viewer.md)는 조정 가능한 카메라 컨트롤, 사용자 정의 환경 조명 및 기본 재질 렌더링 지원을 통해 3D SDF 또는 교차 기능을 3D 장면으로 렌더링합니다. (색상, 거칠음 및 금속성)

또한 노드에는 생성된 모양을 자세히 검사하고 AOV(Separate Rendering Pass), SDF 아이소라인 및 시각적 도우미 등의 디버깅 문제를 확인할 수 있는 기능이 포함되어 있습니다. (E.g. 상자 도련 색상, 격자 및 회전 호)

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="width: 50%; border: 0">
        <td style="text-align: center; width: 50%; border: 0; padding: 15px">
            <img src="../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/3d-viewer/3d-viewer.resources/3d-viewer-example-01.jpg" alt="예제 1" />
        </td>
        <td style="width: 50%; border: 0; padding: 0">
            <table>
                <tr style="vertical-align: top; border: 0">
                    <td style="text-align: center; border: 0">
                        <img src="../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/3d-viewer/3d-viewer.resources/3d-viewer-example-02a.jpg" alt="예제 1" />
                    </td>
                    <td style="text-align: center; border: 0">
                        <img src="../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/3d-viewer/3d-viewer.resources/3d-viewer-example-02b.jpg" alt="예제 2" />
                    </td>
                </tr>
                <tr style="vertical-align: top; border: 0; background: transparent">
                    <td style="text-align: center; border: 0; background: transparent">
                        <img src="../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/3d-viewer/3d-viewer.resources/3d-viewer-example-02c.jpg" alt="예제 3" />
                    </td>
                    <td style="text-align: center; border: 0; background: transparent">
                        <img src="../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/3d-viewer/3d-viewer.resources/3d-viewer-example-02d.jpg" alt="예제 4" />
                    </td>
                </tr>
            </table>
    </tr>
</table>

<a name="openpbr-support"></a>

## OpenPBR 지원

[OpenPBR 표면](https://academysoftwarefoundation.github.io/OpenPBR/)은 컴퓨터 그래픽의 표준으로 사용되는 표면 음영 모델의 사양이며 대다수의 재료를 정확하게 모델링할 수 있습니다.

이 재질 모델은 이제 애플리케이션 전체에서 지원되며, 새로운 렌더러(래스터라이저, GPU 패스트레이서)와 OpenGL 렌더러 모두에서 [전용 셰더](../../interface/3d-view/material-properties/material-properties.md#openpbr)가 제공됩니다.

<img style="display: block; margin: auto" src="./version-16-0.resources/OpenPBRShort.gif" alt="Substance 3D Designer에서의 OpenPBR 지원 및 다른 DCC와의 비교" />

새로운 그래프 템플릿으로 널리 채택된 업계 표준을 시작하거나 이제 OpenPBR 기반의 내장 재질 샘플을 살펴보십시오.

<table style="border: none; margin-top: 32px; margin-bottom: 32px">
    <tr style="vertical-align: top; border: 0">
        <td style="text-align: center; border: 0">
            <img src="./version-16-0.resources/version-16-0-openpbr-01.png" alt="OpenPBR 틀" />
        </td>
        <td style="text-align: center; border: 0">
            <img src="./version-16-0.resources/version-16-0-openpbr-02.png" alt="OpenPBR 재료 샘플" />
        </td>
    </tr>
</table>

OpenPBR 셰이더는 이제 3D 뷰의 기본값이 되며 기본적으로 이전 PBR 사용을 OpenPBR에 대응시켜 이전 버전의 그래프를 지원합니다.

OpenPBR 셰이더는 얇은 필름, 얇은 벽 등의 기존 셰이더보다 더 많은 효과를 지원합니다. 마침내 굴절 효과를 비롯하여 모든 효과를 래스터화(래스터화, OpenGL)할 수 있습니다.

<table style="border: none;">
    <tr style="vertical-align: top; border: 0">
        <td style="border: 0">
            또한 3D 보기에서 보는 그래프가 그래프 재질 모델에 적절한 셰이더를 사용하도록 하는 Substance 그래프용 새로운 <a href="../../compositing-graphs/graph-parameters/graph-parameters.md#attributes">'재질 모델' 특성</a>을 통해 특정 셰이더와 관련된 워크플로우를 보다 쉽게 동기화할 수 있습니다.
        </td>
        <td style="text-align: right; margin-left: 32px; border: 0">
            <img src="./version-16-0.resources/version-16-0-materialModel.png" alt="OpenPBR 재료 샘플" />
        </td>
    </tr>
</table>

>[!NOTE]
> 
>재료 워크플로우에 통합하기 위해 게시된 SBSAR 파일에도 특성이 포함됩니다.

<a name="displacement-popup"></a>

## 3D 보기의 변위 컨트롤

이제 3D 보기 도구 모음에서 사용할 수 있는 [새 변위 팝업](../../interface/3d-view/displacement/displacement.md)에서 직접 액세스하여 3D 보기에서 변위 및 쪽맞춤을 더 빠르고 쉽게 조정할 수 있습니다.

재질 속성과 렌더러 설정에서 앞뒤로 반복하지 않고 **Height 비율**, **Height 수준** 및 **테셀레이션** 값을 조정합니다.

이러한 컨트롤은 새로운 렌더러(래스터라이저, GPU 패스트레이서)와 OpenGL 렌더러 모두에 사용할 수 있습니다.

<img style="display: block; margin: auto" src="../../interface/3d-view/displacement/displacement.resources/3d-view-displacement-popup-mograph.gif" alt="3D 보기의 변위 팝업" />

장면에 여러 재질이 포함된 경우 <code>Shift를 누르고 미리 조정할 장면의 개체를 선택합니다</code> 이 효과를 클릭한 다음(래스터화 및 GPU 패스트레이서 전용) [장면] 브라우저에서 선택합니다.

>[!NOTE]
> 
>테셀레이션은 래스터라이저와 GPU 패스트레이서에서 *개체당*&#x200B;이고 OpenGL에서 *재질당*&#x200B;입니다.

<a name="other-changes"></a>

## 기타 변경 사항

### 상수 값 노드

<table style="border: none; margin-top: 32px; margin-bottom: 32px">
    <tr style="vertical-align: top; border: 0">
        <td style="border: 0">
            <p>Substance 그래프의 상수 값에 더 쉽게 액세스할 수 있도록 각 유형의 간단한 값을 생성하기 위해 <a href="../../compositing-graphs/nodes-reference-for-com/node-library/values/constant.md">새 노드</a>가 추가되었습니다.</p><p>라이브러리의 <b>값 &gt; 상수</b> 섹션에서 이러한 값을 모두 찾을 수 있습니다.</p>
        </td>
        <td style="width: 60%; border: 0">
            <img src="../../compositing-graphs/nodes-reference-for-com/node-library/values/constant.resources/constants-float-01.png" alt="상수 &apos;Float&apos; 노드" />
        </td>
    </tr>
</table>

### MDL 그래프 및 Iray 서비스 종료

15.1 릴리스에서 알림을 받았으므로 이제 MDL 그래프 기능 세트 및 Ray 렌더러가 Designer에서 제거됩니다.\
사내 GPU 패스트레이서는 Designer에서 고품질 사실적 렌더링을 위해 선택한 렌더러입니다.

Designer은 MDL에서 벗어나, 호환되고 널리 지원되는 재질 정의를 위해 선택하는 음영 언어인 MaterialX를 선호하고 있습니다.\
MaterialX는 컴퓨터 그래픽 업계에서 빠르게 인기를 얻고 있으며 USD 파일로 운반할 수 있어 DCC와 렌더러 간 전체 장면의 휴대성이 향상되었습니다.

>[!NOTE]
> 
>MDL 그래프 및 Iray 렌더러의 설명서는 [전용 수명 종료 페이지](../../technical-issues/mdl-graph-iray-eol/mdl-graph-iray-eol.md)를 통해 사용할 수 있습니다.

### VFX 플랫폼 업그레이드 및 macOS 최소 버전

다음 라이브러리가 최신 VFX 플랫폼 표준을 충족하도록 업그레이드되었습니다.

* C++ 20
* 파이썬
* 6.8
* 부스트 1.88
* OpenColorIO 2.5
* OpenSubDiv 3.7
* OpenEXR 3.4
* oneTBB 2022

macOS의 최소 지원 버전에 대한 요구 사항이 macOS 14 Sonoma로 업데이트되었습니다.

<a name="release-notes"></a>

## 릴리스 정보

### 16.0.0

*(2026년 4월 14일 릴리스)*

### 추가됨

* [Content] 모양 스플래터 v2 노드
* [콘텐츠] 모양 스플래터 v2 매퍼 색상/회색 음영 노드
* [Content] 마스크 노드에 모양 스플래터 v2
* [Content] 그리드 아틀라스 노드
* [Content] 3D 뷰어 노드
* [Content] 3D SDF 연산자 노드
* [Content] 3D SDF 프리미티브 노드
* [Content] 3D SDF 변환 노드
* [Content] 3D SDF 재질 노드
* [Content] 벡터 노드에 대한 각도
* [Content] 상수 값 노드
* [3D 보기] OpenGL 렌더러를 위한 OpenPBR 셰이더
* [3D 보기] 래스터라이저 및 GPU 패스트레이서 렌더러를 위한 OpenPBR 셰이더
* [3D 보기] 변위 크기, Height 레벨 및 쪽맞춤을 설정하는 Height 창
* [3D 보기] 도구 모음 항목 재구성
* [3D 보기] 3D 보기에서 OpenPBR을 기본 재질 모델으로 설정
* [3D 보기] 3D 보기에서 &#39;재질 모델&#39; 그래프 특성을 고려합니다.
* [3D 보기] 래스터라이저/GPU 패스트레이서와 OpenGL 렌더러 간에 전환할 때 재질 모델을 동기화합니다.
* [3D 보기] 3D 렌더러 및 재질 정의 변경을 전환할 때 재질 모델이 지속적인지 확인합니다.
동기화됨
* [3D 보기] GPU 패스트레이서: 파랑 노이즈 픽셀 사이클링 활성화
* [3D 보기] 주변 오클루전 불투명도 컨트롤 노출
* [3D 보기] 모든 셰이더에 대해 &#39;타일링&#39; 매개 변수 범위를 [0, 10]으로 설정
* [3D 보기] &#39;Focus&#39; 동작의 이름을 &#39;Frame&#39;으로 바꿉니다.
* [3D 보기] tessellationFactor를 대체하는 새 refineLevel 매개 변수를 처리합니다.
* [3D 보기] FPS 카운터 추가
* [3D 보기] 동일한 수평 도구 모음의 진행률 막대를 하단의 색상 공간으로 이동합니다
* [베이커] 미리 보기에서 선택한 베이커의 UV를 표시합니다
* [그래프] Substance 그래프에 새로운 &#39;재질 모델&#39; 속성 추가
* [NewGraph] 축소판 보기에 구분 기호를 추가합니다
* [매개 변수] &#39;함수&#39; 편집기를 사용하여 입력 매개 변수의 기본 상수 값을 정의합니다.
* [Parameters] `Set` 및 `Is defined` 노드 매개 변수의 콤보 상자를 사용 가능한 변수로 채웁니다.
* [환경 설정] &#39;3D 보기&#39; 탭에서 더 이상 사용되지 않는 &#39;크기 조정 요소&#39; 옵션을 제거합니다.
* [Publish] Publish 대화 상자: 그래프 정보에 재질 모델 포함
* [Python] 새 클래스 SDMaterialModelDescription을 추가하여 재질 모델 정보를 가져옵니다.
* [Python] SDSBSCompGraph 개체의 재질 모델 속성을 가져오거나 설정할 수 있습니다.
* [Python Editor] 글꼴 크기를 12로 늘리기
* [템플릿] OpenPBR 템플릿 추가
* [Templates] 재질 샘플을 OpenPBR으로 변환
* [ThirdParty] 1.88 버전으로 업데이트 부스트
* [ThirdParty] C++ API를 C++20으로 업데이트
* [서드파티] NGL을 1.42로 업데이트합니다.
* [서드파티] oneTBB를 2022.x 버전으로 업데이트
* [서드파티] OpenColorIO를 2.5.x 버전으로 업데이트
* [서드파티] OpenEXR을 3.4.x 버전으로 업데이트
* [서드파티] Qt &amp; QtForPython을 6.8.x로, Python을 3.13.x로 업데이트
* [서드파티] TBB를 oneTBB 2021.x로 업데이트
* [Deprecation] Iray 및 MDL 편집기 제거

### 수정 사항

* [2D 보기] 위젯의 폭이 작아질 때 막대 그래프 선택 범위가 유지되지 않습니다
* [3D 내보내기] Designer에서 내보낸 메시가 usdview에서 동일하게 렌더링되지 않습니다
* [3D 보기] 비udim 항목을 3D 보기에 할당하면 단일 타일 렌더링 모드가 사라집니다.
* [3D 보기] OCIO를 사용할 때 클램핑된 결과
* [3D 보기] 특정 장면의 재정의되지 않은 재질에 그래프 텍스처를 적용할 때 충돌이 발생합니다
* [3D 보기] 프레임 버퍼를 만들 때 충돌이 발생합니다.
* [3D 보기] Eclair GPU 패스트레이서: 특정 모델을 렌더링할 때 형상이 손상되고 성능이 저하됨
* [3D 보기] 특정 장면에 대한 텍스처 변환이 잘못되었습니다.
* [3D 보기] 고정 렌더링 해상도를 사용할 때 장면/선택 프레임이 일관되지 않습니다.
* [3D 보기] 특정 GLTF 파일을 렌더링할 때 확산 색상이 잘못 표시됩니다
* [3D 보기] 특정 경우에 렌더러를 전환할 때 보이지 않는 환경
* [3D 보기] 일부 .fbx 파일을 가져올 때 재질이 올바르게 인식되지 않음
* [3D 보기] 재질을 두 번 이상 오버라이드하면 타일링이 1로 재설정됩니다
* [3D 보기] &#39;UVs&#39; 범주의 속성이 SBSSCN 파일에 저장되지 않음
* [3D 보기] 단일 출력 그래프에서 &#39;3D 보기에서 출력 재설정 및 보기&#39;가 재질을 재설정하지 않음
* [3D 보기] &#39;렌더링 저장&#39;: 편집된 이미지 형식이 유지되지 않습니다.
* [3D 보기] AMD GPU에서 선택이 작동하지 않음
* [3D 보기] 자체 포함된 3D 장면은 디스크에서 수정할 때 새로 고쳐지지 않습니다.
* [3D 보기] 일부 색상 재질 속성을 재정의할 때 색상 관리가 제대로 되지 않습니다
* [3D 보기] UDIM 텍스처가 특정 메시에서 올바르게 적용되지 않습니다.
* [3D 보기] MaterialX 재질이 있는 USD 장면이 더 이상 올바르게 렌더링되지 않음
* [베이커] 일부 망과 충돌합니다.
* [베이커] 텍스처 전송: bkBufferViewCopy에서 충돌
* [조리기] 방지할 수 있는 경우 While Loop 노드의 무한 루프
* [엔진] 응용 프로그램을 닫을 때 Substance 엔진을 중지합니다.
* [일반] 응용 프로그램을 종료할 때 임의 충돌 방지(Windows만 해당)
* [그래프] 함수 그래프: 일부 상황에서는 형식 전파가 제대로 작동하지 않습니다
* [그래프] 이미지 입력 노드의 이름이 바뀌면 그래프 링크가 삭제됩니다
* [그래프] 링크와 핀에 아티팩트가 표시되는 경우가 있습니다
* [Preferences] &#39;Viewport scaling&#39;이 반전됨
* [속성] 인스턴스 매개 변수를 표시하는 동안 그래프 입력 조정 기능을 수정할 때 충돌이 발생합니다
* [Python] PySide6 모듈을 가져올 수 없습니다(기존 PySide6 설치와 충돌할 수 있음).
* [Python] 기존 PySide 및 Shiboken 모듈이 Designer의
* [UI] 특정 경우 버튼에서 마우스 오버 스타일이 사라짐(Windows만 해당)
* [UI] 클릭 시 마우스 오버 스타일이 드롭다운 버튼에 표시되지 않음 (macOS만 해당)
* [UI] 도구 설명이 대화 상자 경계를 벗어난 경우 &#39;?&#39; 도구 설명의 &#39;자세히 알아보기&#39; 버튼이 작동하지 않음(Windows만 해당)

### 알려진 문제

* [그래프] OpenPBR 그래프에 대해 생성된 아이콘이 정확하지 않습니다.
* [3D 보기] 애니메이션이 적용된 프리미티브가 있는 장면은 제대로 지원되지 않습니다
* [3D 보기] 일부 AMD 그래픽 카드에서는 Pathtracer가 지원되지 않습니다.

