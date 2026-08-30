---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/function-graphs/fxmaps/using-functions-in-fxmaps/using-the-sampler-nodes.html"
breadcrumb-title: ''
description: FXMaps의 sampler 노드를 사용하여 텍스처를 샘플링하고 프로시저 재질 베리에이션을 만드는 방법을 알아봅니다.
helpx_creative_field: ""
helpx_description: Designer > Function graphs > FXMaps > Using Functions in FXMaps > Using the Sampler nodes
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Sampler 노드 사용
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '201'
ht-degree: 0%

---


# Sampler 노드 사용

![](using-the-sampler-nodes.resources/sampler-graph.jpg)

샘플러 노드는 fx-맵 노드에 플러깅된 이미지 입력의 픽셀 값을 샘플링하는 데 사용될 수 있다. 그 후, 샘플링된 값들은 함수들을 사용하여 임의의 파라미터들을 구동하는 데 사용될 수 있다.

## 간단한 예

이 예에서는 사분면 노드 체인을 생성하여 패턴 그리드를 생성했습니다. 마지막 사분면의 불투명도/광도 매개 변수에서 함수가 만들어집니다.

![](using-the-sampler-nodes.resources/sampler-function.jpg){width="300px"}![](using-the-sampler-nodes.resources/sampler-result-1.jpg){width="300px"}

Sample 노드는 float2 입력을 샘플링 좌표(x, y)로 취한다. 이 예제에서는 $pos 변수를 사용했습니다. 각 패턴에 대해 픽셀 값은 FxMap 노드에 연결된 첫 번째 이미지 입력의 패턴 위치에서 샘플링됩니다.

Sample Gray 노드는 0, 1 범위의 float1 값을 반환합니다.

[샘플 색상] 노드는 0, 1 범위의 float4(rgba) 값을 반환합니다.

## 고급 예

여기서 우리는 샘플링된 값을 상수(0.3)와 비교한다. 샘플링된 값이 0.3보다 크면 함수는 1을 반환하고, 그렇지 않으면 0을 반환합니다.

![](using-the-sampler-nodes.resources/sampler-function-advanced.jpg){width="300px"}![](using-the-sampler-nodes.resources/sampler-result-advanced.jpg){width="300px"}

## 샘플 다운로드

[![SBS 파일 아이콘](using-the-sampler-nodes.resources/sbs-1_1.png){width="64px"}](https://shared-assets.adobe.com/link/d5f9adf3-0bb5-49a1-4eb9-a0506d4f3f32)
