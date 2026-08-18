---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/atomic-nodes/pixel-processor.html"
breadcrumb-title: ''
description: 고급 텍스처 조작을 위해 사용자 정의 표현식을 사용하여 개별 픽셀을 처리하려면 픽셀 프로세서 노드를 사용합니다.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Atomic nodes > Pixel processor
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 픽셀 프로세서
user-guide-description: ''
user-guide-title: ''
source-git-commit: ea96f5a148246d20263c4ecf0b67d0b4a51f28a8
workflow-type: tm+mt
source-wordcount: '355'
ht-degree: 1%

---


# 픽셀 프로세서

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![기본 노드: 픽셀 프로세서](../../../../assets/comp_pixelprocessor_1.png "기본 노드: 픽셀 프로세서"){width="200px"}

</td>
<td width="100.00%" style="border: 0;" valign="top">

각 픽셀의 값이 지정된 [Substance 함수 그래프](../../../../function-graphs/the-function-graph/the-function-graph.md)의 결과인 이미지를 생성합니다.

픽셀 프로세서를 사용하면 선택적 입력에서 출력으로 반환되는 모든 픽셀에 대해 사용자 정의 함수를 실행할 수 있습니다.

그래프 내에서 모든 수학적 연산을 실행하고 결과를 반환할 수 있으므로 가장 활용도가 높은 노드입니다.

</td>
</tr>
</table>

[FX-Map](../../../../function-graphs/fxmaps/fxmaps.md)과(와) 마찬가지로 어떤 작업도 수행하려면 내부 기능을 설정해야 합니다. 픽셀 프로세서가 FX-Map과 다른 점은 패턴 모양과 배치를 제어하는 여러 기능을 사용하여 패턴 배치에는 중점을 두지 않는다는 것입니다. 대신, 단일 함수는 모든 픽셀에 대해 병렬로 실행되며, 여기서 각 픽셀은 그것의 이웃들의 계산 결과들을 인식하지 못한다.

픽셀 프로세서는 [값 프로세서](../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/value-processor/value-processor.md)와 비슷합니다. 이 프로세서는 단일 값에서만 실행되며 픽셀 프로세서와 비교하여 최적화를 제공할 수 있습니다.

노드 기반 편집기에서 [셰이더](../../../../glossary/glossary.md) 함수를 만드는 데 사용되는 모든 사용자의 경우 픽셀 프로세서가 익숙한 환경을 제공해야 합니다.

<table>
<tr style="border: 0;">
<td width="100.00%" style="border: 0;" valign="top">



</td>
<td width="83.33%" style="border: 0;" valign="top">



</td>
<td width="100.00%" style="border: 0;" valign="top">



</td>
</tr>
</table>

>[!TIP]
>
> 픽셀 프로세서 노드의 간단한 사용을 보여 주는 주석이 달린 프로젝트 파일은 이 설명서의 [샘플 Substance 그래프](../../../../compositing-graphs/sample-compositing-graphs/sample-substance-compositing-graphs.md) 섹션에서 사용할 수 있습니다.
> 
> [값 프로세서](../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/value-processor/value-processor.md) 노드는 [Substance 함수 그래프](../../../../function-graphs/the-function-graph/the-function-graph.md)를 배울 수 있는 좋은 출발점입니다.
> 
> 또한 이러한 유형의 그래프를 사용하여 작업하고 수학적 연산을 수행하면 이 노드에서 모든 것을 가져올 수 있다는 점을 고려하십시오.
> 
> 또한 [UV](../../../../glossary/glossary.md), [텍스처 샘플링](../../../../glossary/glossary.md) 및 벡터의 개념을 익히는 것이 좋습니다.

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

## 출력 커넥터

</td>
<td style="border: 0;" valign="top">

### 예

</td>
</tr>
</table>

## 매개변수

|  |  |
| --- | --- |
| <b>색상 모드</b> *부울* | 회색 음영과 색상 출력 이미지 사이를 전환합니다. |
| <b>픽셀 단위 함수</b> *Float/Float4* | 출력 이미지의 픽셀당 [Substance 함수 그래프](../../../../function-graphs/the-function-graph/the-function-graph.md)가 평가되었습니다.   <b>$pos</b> 변수로 설정된 [Get Float2](../../../../function-graphs/nodes-reference-for-fun/atomic-function-nodes/get-nodes/get-nodes.md) 노드를 사용하여 현재 픽셀의 [정규화된](../../../../glossary/glossary.md) 위치에 액세스합니다. |

## 입력 커넥터

|  |  |
| --- | --- |
| <b>입력 이미지 #</b> *회색 음영/색상* | [샘플 색상](../../../../function-graphs/nodes-reference-for-fun/atomic-function-nodes/sampler-nodes/sampler-nodes.md) 또는 [샘플 회색 음영](../../../../function-graphs/nodes-reference-for-fun/atomic-function-nodes/sampler-nodes/sampler-nodes.md) 노드를 사용하여 지정된 색인의 입력에 있는 값에 액세스합니다. |

## 출력 커넥터

|  |  |
| --- | --- |
| <b>출력</b> *회색 음영/색상* |  |

## 예

*곧 출시 예정*
