---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/mdl-graphs/substance-compositing-graphs-and-mdl-materials.html"
breadcrumb-title: ''
description: Substance 3D Designer에서 Substance 합성 그래프와 MDL 재질이 함께 사용되어 재질을 만드는 방법을 살펴봅니다.
helpx_creative_field: ""
helpx_description: Designer > MDL graphs > Substance graphs and MDL materials
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Substance 그래프 및 MDL 재질
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '713'
ht-degree: 1%

---


# Substance 그래프 및 MDL 재질

이 페이지에서는 [Substance 그래프](../../compositing-graphs/substance-compositing-graphs.md)와 MDL 그래프 간의 시너지 효과 및 Substance 그래프 [출력](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/output/output.md)의 텍스처를 MDL 그래프 입력으로 연결하는 방법에 대해 설명합니다.

## 개요

Substance 그래프의 출력은 이 페이지에서 설명하는 두 가지 방법으로 MDL 재질의 노출 매개 변수&#x200B;*에*&#x200B;전달할 수 있습니다.

3D 보기에서 현재 적용된 MDL 재질에 *[가변](../../mdl-graphs/main-mdl-graph-concepts/main-mdl-graph-concepts.md)* 유형의 노출 매개 변수가 있는 경우 [노출 매개 변수](../../compositing-graphs/manage-parameters/exposing-a-parameter/exposing-a-parameter.md)의 속성에서 <b>유형 수정자</b> 옵션을 사용하여 이 유형을 설정할 수 있으며, 이러한 유형을 *텍스처*&#x200B;에 연결할 수 있습니다.

* <b>Color</b> 매개 변수는 RGBA 텍스처에 연결할 수 있습니다.
* 회색 음영 텍스처의 <b>부동</b> 매개 변수

이러한 경우, 원시 균일 값은 가변적인 값을 공급하는 텍스처 샘플러로 대체된다. 이러한 샘플러에는 노출된 매개 변수에 정의된 <b>usage</b> 특성이 있으며, 이 사용을 통해 Designer은 Substance 그래프로 출력되는 텍스처를 MDL 재질의 적절한 매개 변수에 *일치하는 사용*&#x200B;할 수 있습니다.

## 3D 보기에서 그래프 Substance

Substance 그래프에 대해 <b>3D 보기에서 출력 보기</b> 옵션을 사용하거나 Substance 그래프를 <b>탐색기</b> 패널에서 <b>3D 보기</b>(으)로 드래그할 때, 출력은 현재 3D 보기에 표시된 MDL 재질에서 *일치하는 용도*&#x200B;의 노출된 매개 변수에 연결됩니다.

Substance 그래프의 개별 텍스처는 Substance 그래프 노드에서 RMB를 누르고 3D 뷰로 드래그함으로써, 식별자에 관계없이 텍스처 샘플링을 지원하는 MDL 재료 파라미터 중 임의의 것에 연결될 수 있다. 사용 가능한 샘플러 사용 목록이 표시되며, 선택한 텍스처의 대상 사용을 선택할 수 있습니다.

![노출된 MDL 그래프 입력](substance-compositing-graphs-and-mdl-materials.resources/mdl-graph-inputs-samplers.png "노출된 MDL 그래프 입력")

*Substance 그래프로 출력되는 텍스처는 3D 보기에서 MDL 그래프의 노출된 매개 변수에 연결됩니다.*

## MDL 그래프의 그래프 Substance

Substance 그래프 인스턴스를 <b>탐색기</b> 패널에서 MDL 그래프로 드래그하여 MDL 그래프에 직접 배치할 수 있습니다. MDL 그래프에는 <b>Substance 3D 파일</b>(SBS) 및 <b>Substance 3D 에셋 파일</b>(SBSAR)의 Substance 그래프를 사용할 수 있습니다.

+++Substance 3D 파일(SBS)의 Substance 그래프
![MDL 그래프의 SBS 파일에서 Substance 그래프](substance-compositing-graphs-and-mdl-materials.resources/mdl-sbs-instance-hl.png "MDL 그래프의 SBS 파일에서 Substance 그래프")



MDL 그래프의 [Substance 3D 파일](../../getting-started/overview/overview.md)(SBS)에서 *[Substance 그래프](../../compositing-graphs/substance-compositing-graphs.md) 인스턴스*

+++

+++Substance 3D 에셋(SBSAR)의 Substance 그래프
![MDL 그래프의 SBSAR 파일에서 Substance 그래프](substance-compositing-graphs-and-mdl-materials.resources/mdl-sbsar-instance-hl.png "MDL 그래프의 SBSAR 파일에서 Substance 그래프")



MDL 그래프의 [Substance 3D 에셋](../../getting-started/overview/overview.md)(SBSAR)에서 *[Substance 그래프](../../compositing-graphs/substance-compositing-graphs.md) 인스턴스*

+++

Substance 그래프 인스턴스가 만들어지면 다음 기능을 사용하여 *노드*(으)로 표시됩니다.

* 각 그래프 출력에 대한 *형식화된 출력* 커넥터입니다. 출력 데이터는 다음과 같이 입력됩니다.
  * RGBA 비트맵: 색상(가변)
  * 회색 음영 비트맵: 부동(가변)
  * 값: 값 유형과 일치(가변)
* Substance 그래프에서 출력한 텍스처를 매핑하는 데 사용할 UV 좌표를 지정하는 *입력* 유형의 UV 좌표입니다. 연결되지 않은 상태로 두면 기본값은 UV 공간의 X 및 Y에서 클래식 0-1 선형 그레이디언트입니다
* Substance 그래프 레이블 뒤에 *레이블*&#x200B;이 지정되고 레이블이 정의되지 않은 경우 식별자가 지정되며 첫 번째 비트맵 출력이 축소판으로 표시됩니다.

노드 속성을 사용하면 Substance 그래프의 *모든 동적 속성*&#x200B;을 수정할 수 있습니다.

* 출력 크기
* 임의 시드
* 입력 매개 변수
* …

노드 속성을 사용하면 MDL 재질에서 텍스처가 *매핑*&#x200B;되는 방식과 관련된 매개 변수를 설정할 수도 있습니다.

* 타일링
* 물리적 크기 사용
* 표준 포맷
* 접선 공간

Substance 그래프 인스턴스 노드의 출력은 MDL 그래프에서 매칭 타입의 임의의 노드 입력에 연결될 수 있다.

<b>SBS 기본 매개 변수</b> 섹션에서 매개 변수를 변경하면 하나 이상의 Substance 그래프 출력을 다시 계산해야 합니다. 이 경우 <b>Substance 엔진</b>을 사용하고 MDL 그래프 계산 위에 *성능 오버헤드*&#x200B;가 포함됩니다. 3D 보기에 적용된 MDL 그래프에서 인스턴스화된 *Substance 그래프를 수정*&#x200B;하면 성능에 영향을 줄 수 있습니다.

>[!WARNING]
>
> MDL 그래프에서 Substance 그래프를 사용하는 경우 MDL 그래프를 내보내면 Substance 그래프 출력이 비트맵으로 분리되고 내보낸 MDL 파일과 함께 번들링되어 텍스처로 내보내집니다. 즉, 내보낸 MDL 파일에서 Substance 그래프의 파라메트릭 특성이 *손실*&#x200B;됨을 의미합니다.
