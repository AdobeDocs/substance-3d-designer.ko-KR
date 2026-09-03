---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/scan-processing/smart-auto-tile.html"
breadcrumb-title: ''
description: 스마트 자동 타일 노드를 사용하면 지능형 패턴 감지를 사용하여 스캔한 재질에서 매끄러운 타일을 자동으로 만들 수 있습니다.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > Scan Processing > Smart Auto Tile
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 스마트 자동 타일
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '393'
ht-degree: 5%

---


# 스마트 자동 타일

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](smart-auto-tile.resources/smart-auto-tile-01.png){width="128px"}

<b>내부:</b> 재질 필터 > 스캔 처리

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 설명

이 노드는 입력의 스마트 분석에 따라 Basecolor, Normal 및 Heightmaps의 비 타일링 세트를 타일링 버전으로 바꿉니다. [바둑판식 사진 만들기](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/tiling/make-it-tile-photo/make-it-tile-photo.md)와 비슷하지만, 모든 채널의 정보를 사용하여 가장 스마트하게 모든 것을 혼합하기 때문에 훨씬 더 향상되었습니다([복제 패치](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/clone-patch/clone-patch.md)와 유사). 또한 타일링 시 사용할 영역을 결정하는 내부 [자르기](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/crop/crop.md) 기능이 있습니다. 이 기능을 제대로 이해하려면 [자르기 노드에 대해 자세히 읽기](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/crop/crop.md)를 확인하세요.

이 노드를 사용하려면 먼저 자른 영역을 정의한 다음 가장자리 설정을 사용하여 타일 가장자리가 중앙에 혼합되는 방법을 결정합니다. 이 작업에 Treshold 매개 변수가 매우 중요합니다! 크고 균일한 영역은 이 효과와 잘 맞지 않는다는 점을 명심하십시오. 세부 사항 및 모양이 많을수록 더 많이 사용해야 합니다.

</td>
</tr>
</table>

<a name="inputs"></a>

## 입력

|  |  |
|:---|:---|
| <b>마스크</b> <i>회색 음영 입력</i> | 노드의 효과를 마스킹하는 데 사용되는 마스크 슬롯입니다. &quot;마스크 사용&quot; 매개 변수로 전환할 수 있습니다. |

<a name="parameters"></a>

## 매개변수

|  |  |
|:---|:---|
| <b>자르기</b> |  |
| <b>입력 크기</b> <i>0 - 8192</i> | 이미지의 해상도와 비율을 입력합니다. 정사각형이 아닌 이미지에 매우 중요합니다. |
| <b>변형</b> <i>(변환 행렬)</i> | 결과를 회전하고 크기를 조절합니다. 캔버스와 직접 상호 작용하여 결과를 수정할 수 있습니다. |
| <b>오프셋</b> <i>0.0 - 1.0</i> | 결과를 이동하거나 변환합니다. 캔버스와 직접 상호 작용하여 결과를 수정할 수 있습니다. |
| <b>가장자리</b> |  |
| <b>가장자리 감지</b> <i>거짓/참</i> | 특수 가장자리가 감지하는 혼합을 켜거나 끕니다. |
| <b>채널당 임계값 사용</b> <i>거짓/참</i> | 전역 임계값 사이를 전환하거나 모든 채널에 대해 하나의 값을 전환합니다. |
| <b>임계값</b> <i>0.0 - 1.0</i> |  |
| <b>임계값 기본 색상</b> <i>0.0 - 1.0</i> |  |
| <b>임계값 정상</b> <i>0.0 - 1.0</i> |  |
| <b>임계값 Height</b> <i>0.0 - 1.0</i> |  |
| <b>오프셋 자르기</b> <i>0.0 - 0.5</i> | 컷을 이동하는 기본 컨트롤인 X축과 Y축은 모두 분리됩니다. |
| <b>흐림 효과</b> <i>0.0 - 2.0</i> | 혼합 전환을 흐리게 합니다. |
| <b>Smoothness</b> <i>0.0 - 2.0</i> | 가장자리 분석 결과의 들쭉날쭉한 정도를 제어합니다. |
| <b>격자 해상도</b> <i>1 - 11</i> | 모서리 분석의 품질 해상도입니다. |
| <b>기본 색상 사용</b> <i>거짓/참</i> | 기본 색상 처리(시작 및 종료)를 전환합니다. |
| <b>표준 사용</b> <i>거짓/참</i> | 일반 처리(시작 및 종료)를 전환합니다. |
| <b>Height 사용</b> <i>거짓/참</i> | 일반 처리(시작 및 종료)를 전환합니다. |
| <b>마스크 사용</b> <i>거짓/참</i> | 사용자 정의 스탬프 마스크 모양에 대한 마스크 맵 사용을 켜거나 끕니다. |
