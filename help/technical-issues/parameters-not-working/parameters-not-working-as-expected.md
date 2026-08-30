---
helpx_url: "https://helpx.adobe.com/kr/substance-3d-designer/technical-issues/parameters-not-working-as-expected.html"
breadcrumb-title: ''
description: Substance 그래프 매개 변수가 예상대로 작동하지 않는 문제를 해결하고 해결 방법을 찾으십시오.
helpx_creative_field: ""
helpx_description: Designer > Technical issues > Parameters not working as expected
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 매개변수가 예상대로 작동하지 않음
user-guide-description: ''
user-guide-title: ''
source-git-commit: 21af965a075e8c119d16922f15b867da99c21397
workflow-type: tm+mt
source-wordcount: '295'
ht-degree: 6%

---


# 매개변수가 예상대로 작동하지 않음

이 페이지에서는 Substance 3D Designer에서 매개 변수가 예상대로 작동하지 않는 일반적인 원인을 나열하고 각각에 대한 문제 해결 단계를 제공합니다.

## 매개 변수가 미리 보기 모드에서 작동하지 않고 게시된 Substance 3D 에셋(SBSAR)

<b>![(오류)](parameters-not-working-as-expected.resources/error.svg) 문제</b>

Designer에서 [미리 보기 모드](../../compositing-graphs/manage-parameters/exposing-a-parameter/exposing-a-parameter.md)를 사용하거나 해당 그래프 중 [게시](../../compositing-graphs/publishing-asset-files/publishing-substance-3d-asset-files-sbsar.md)된 Substance 3D 에셋(SBSAR)의 매개 변수 목록에 있는 그래프의 일부 노출 매개 변수가 *나열되지 않음*&#x200B;입니다.

<b>![(틱)](parameters-not-working-as-expected.resources/check.svg)권장 단계</b>

누락된 매개 변수는 [정적 매개 변수](../../glossary/glossary.md)일 가능성이 높으며, *조리*&#x200B;된 그래프는 *즉시 편집할 수 없습니다*. 즉, 알고리즘을 빠르고 효율적으로 실행하기 위해 처리됩니다. 그래프가 *편집* 또는 *게시*&#x200B;될 때마다 Designer에서 요리가 수행됩니다. 이러한 제한의 영향을 받는 매개 변수는 이 설명서의 [매개 변수 노출](../../compositing-graphs/manage-parameters/exposing-a-parameter/exposing-a-parameter.md) 페이지의 [제한](../../compositing-graphs/manage-parameters/exposing-a-parameter/exposing-a-parameter.md) 섹션에 나열되어 있습니다.

따라서 정적 매개 변수는 Designer에서 표시되고 편집할 수 있지만 게시된 Substance 3D 에셋에서는 *숨김*&#x200B;됩니다. Substance 3D 에셋에 게시하기 전에 [미리 보기 모드](../../compositing-graphs/manage-parameters/exposing-a-parameter/exposing-a-parameter.md)를 사용하여 이러한 제한 사항을 확인할 수 있습니다.

다음은 정적 매개 변수 목록입니다.

| 노드 | 매개변수 |
| --- | --- |
| 모든 노드 | 타일링 모드 픽셀 비율 |
| [균일한 색상](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/uniform-color/uniform-color.md) | 색상 모드 |
| [픽셀 프로세서](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/pixel-processor/pixel-processor.md) | 색상 모드 |
| [혼합](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/blend/blend.md) | 혼합 모드 Alpha 혼합 자르기 영역 |
| [FX-Map](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/fx-map/fx-map.md) | 혼합 모드 |
| [사분면](../../function-graphs/fxmaps/the-quadrant-node/the-quadrant-node.md) | 패턴 입력 이미지 알파 입력 이미지 필터링 |

## 매개 변수에 적용된 Substance 함수 그래프에 대해 잘못된 결과

<b>![(오류)](parameters-not-working-as-expected.resources/error.svg) 문제</b>

노드 파라미터에 적용된 Substance 함수 그래프는 음의 정수를 사용할 때 기대값을 출력하지 않는다.

<b>![(틱)](parameters-not-working-as-expected.resources/check.svg) 권장 단계</b>

음의 정수는 현재 제대로 지원되지 않습니다. 해결 방법으로 [Integer2](../../function-graphs/nodes-reference-for-fun/atomic-function-nodes/constant-nodes/constant-nodes.md) 값에 음수 정수 값을 사용하고 [스위즐 정수](../../function-graphs/nodes-reference-for-fun/atomic-function-nodes/vector-and-swizzle-nodes/vector-and-swizzle-nodes.md) 노드를 사용하여 추출합니다.
