---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/patterns/shape-splatter.html"
breadcrumb-title: ''
description: 모양 스플래터 노드를 사용하여 절차 패턴과 세부 사항을 만들기 위해 텍스처 간에 모양을 산란 합니다.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Patterns > Shape Splatter
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 모양 튀김
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '960'
ht-degree: 7%

---


# 모양 튀김

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](shape-splatter.resources/shape-splatter.png){width="128px"}

<b>내부:</b> 텍스처 생성기 > 패턴

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 설명

함께 제공되는 노드 [모양 튄 혼합](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/shape-splatter-blend/shape-splatter-blend.md), [모양 튄 마스크](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/shape-splatter-to-mask/shape-splatter-to-mask.md) 및 [모양 튄 데이터 추출](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/shape-splatter-data-ext/shape-splatter-data-extract.md)과 함께 사용하도록 설계된 매우 복잡한 노드입니다. [Flood Fill](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/flood-fill/flood-fill.md)와 유사한 다단계 시스템을 통해 [타일 Sampler](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/tile-sampler/tile-sampler.md) 또는 [생성기](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/tile-generator/tile-generator.md)와 유사한 방식으로, 그러나 모든 단계를 제어할 수 있는 동적이고 비파괴적인 프로세스를 통해 모양을 튀기는 데 사용됩니다. Flood Fill이 외부 소스에서 기본 입력 맵을 가져오는 반면, 모양 스플래터는 [Flood Fill](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/flood-fill/flood-fill.md)의 고급 버전처럼 맵과 후속 데이터를 한 번에 생성합니다.

주요 목적은 Height 맵에 모양을 배치할 수 있도록 하고 그 위에 있는 모양을 배치한 다음 스플래터 데이터에서 다양한 맵을 생성하는 것입니다. 예를 들어 풍경에 바위, 잔가지, 나뭇잎 등을 배치합니다. 그런 다음 서로 다른 맵을 Height, 표준, 기본 색상, 거칠기 및 기타 채널에 사용할 수 있으며 모든 맵은 여전히 동일한 공유 스플래터 데이터를 기반으로 합니다.

</td>
</tr>
</table>

<a name="inputs"></a>

## 입력

|  |  |
|:---|:---|
| <b>배경 Height</b> <i>회색 음영 입력</i> | 다양한 효과 위에 타일을 배치하고 구동하는 배경 Height. |
| <b>패턴 1-8</b> <i>회색 음영 입력</i> | 선택적 패턴 |
| <b>패턴 분포</b> <i>회색 음영 입력</i> | 회색 음영 매핑 대상 |
| <b>모양 비율</b> <i>회색 음영 입력</i> | 타일 비율을 제어하는 회색 음영 맵 |
| <b>모양 회전</b> <i>회색 음영 입력</i> | 타일 회전을 구동하는 회색 음영 맵 |
| <b>Height 오프셋</b> <i>회색 음영 입력</i> | 타일 Height의 오프셋으로 사용할 회색 음영 맵 |
| <b>Height 크기</b> <i>회색 음영 입력</i> | 타일 Height의 오프셋으로 사용할 회색 음영 맵 |
| <b>무작위 마스크</b> <i>회색 음영 입력</i> | 노드의 효과를 마스킹하는 데 사용되는 마스크 슬롯입니다. |
| <b>벡터 맵</b> <i>색상 입력</i> | 타일 위치 지정 및 회전을 구동하는 색상 벡터 맵 |

<a name="parameters"></a>

## 매개변수

|  |  |
|:---|:---|
| <b>X 양</b> <i>1 - 64</i> | 패턴의 X 반복 정도. |
| <b>Y 양</b> <i>1 - 64</i> | 패턴의 Y 반복의 양입니다. |
| <b>패턴</b> |  |
| <b>패턴 입력 번호</b> <i>1 - 8</i> | 사용할 패턴 양을 설정합니다. 새 패턴 입력 슬롯을 잠금 해제합니다. |
| <b>패턴 분포 모드</b> <i>임의, 패턴 색인, 선 색인, 열 색인</i> | 사용할 패턴을 결정하는 방법을 설정합니다. 무작위로 또는 패턴, 선 또는 열별로 지정합니다. |
| <b>패턴 분포 맵 승수</b> <i>0.0 - 1.0</i> | 패턴 배치에 대한 분포 맵(옵션)의 영향을 설정합니다. |
| <b>패턴 회전</b> <i>0, 90, 180, 270</i> | 사전 설정, 패턴의 90도 회전을 설정합니다. |
| <b>패턴 회전 무작위</b> <i>0.0 - 1.0</i> | 패턴에 대한 임의의 90도 스텝 회전의 양을 설정합니다. |
| <b>크기</b> |  |
| <b>크기 조절</b> <i>0.0 - 5.0</i> | 모든 타일에 대해 균일한 크기를 설정합니다. |
| <b>무작위 크기 조정</b> <i>0.0 - 1.0</i> | 모든 타일에 대해 균일한 크기를 임의화합니다. |
| <b>겹치지 않게 크기 조정</b> <i>0.0 - 1.0</i> | 타일이 겹치지 않도록 무작위를 균일하게 축소합니다. 이전의 두 매개 변수와 함께 사용하면 안 됩니다. |
| <b>맵 배율 조정</b> <i>0.0 - 1.0</i> | 비율 맵의 영향을 설정합니다. |
| <b>크기</b> <i>0.0 - 1.0</i> | 균일하지 않은 타일 크기 조절을 허용합니다. |
| <b>배경색 경사의 크기 비율</b> <i>0.0 - 1.0</i> | 균일하지 않은 크기 조절 타일에 [배경 맵] 경사(계산된 [표준])을 사용합니다. 원근 뒤틀기를 시뮬레이션합니다. |
| <b>X/Y 양 비율별 크기</b> <i>0.0 - 1.0</i> | X 및 Y 양에서 다른 비율을 보정하기 위한 균일하지 않은 배율 조정입니다. |
| <b>위치</b> |  |
| <b>위치 무작위</b> <i>0.0 - 2.0</i> | 모든 타일에 대해 위치를 임의로 오프셋합니다. |
| <b>무작위 분포</b> <i>가우스, 균일</i> | 이전 매개 변수에 사용할 계산을 설정합니다. 큰 차이를 만들지 않고, 숫자가 높을수록 더 두드러집니다. [가우스]은 퍼짐이 더 균일해지는 경향이 있습니다. |
| <b>벡터 맵 멀티플라이어</b> <i>0.0 - 1.0</i> | 오프셋에 대한 벡터 입력 맵의 영향. |
| <b>오프셋 가로</b> <i>-2.0 - 2.0</i> | 전역 가로 오프셋. |
| <b>오프셋 세로</b> <i>-2.0 - 2.0</i> | 전역 세로 오프셋. |
| <b>범위를 벗어남 옵션</b> <i>모양 크기 조정, 위치 제한</i> | 타일이 범위를 벗어난 경우 수행할 작업입니다. |
| <b>회전</b> |  |
| <b>회전</b> <i>0.0 - 1.0</i> | 모든 타일을 전역적으로 회전합니다. |
| <b>회전 무작위</b> <i>0.0 - 1.0</i> | 타일당 임의로 회전합니다. |
| <b>배경에서 회전 경사</b> <i>0.0 - 1.0</i> | [배경 맵 경사](계산된 표준)를 사용하여 타일을 회전합니다. 경사 위나 아래를 가리키는 모양을 만드는 데 사용할 수 있습니다. |
| <b>회전 맵 승수</b> <i>0.0 - 1.0</i> | 타일 단위 회전에 대한 회전 맵 효과의 혼합. |
| <b>벡터 맵 멀티플라이어</b> <i>0.0 - 1.0</i> | 타일 단위 회전에 대한 회전 맵 효과의 혼합. |
| <b>Height</b> |  |
| <b>Height 크기 자동 조정</b> <i>거짓/참</i> | 절대 범위를 정의하는 대신 배경을 기준으로 Height 범위를 자동으로 조정합니다. 제어를 줄이거나 늘릴 수 있습니다. |
| <b>Height 오프셋</b> <i>-1.0 - 1.0</i> | 수정자를 사용하여 Height 범위 내에서 모든 타일을 균일하게 오프셋하거나 이동합니다. |
| <b>Height 오프셋 무작위</b> <i>0.0 - 1.0</i> | 타일을 기준으로 Height 오프셋을 임의로 변경합니다. |
| <b>Height 오프셋 맵 배율기</b> <i>0.0 - 1.0</i> | 오프셋 맵의 영향을 설정하는 수정자입니다. |
| <b>Height 크기</b> <i>0.0 - 1.0</i> | Height 범위 전체에서 모든 타일의 크기를 균일하게 조정/확장하는 수정자입니다. 오프셋과 반대로 하면 대비와 같이 값이 더 멀어집니다. |
| <b>Height 비율 무작위</b> <i>0.0 - 1.0</i> | 타일을 기준으로 Height 배율을 임의로 변경합니다. |
| <b>Height 비율 맵 승수</b> <i>0.0 - 1.0</i> | 비율 표시의 영향을 설정하는 수정자입니다. |
| <b>배경 일치</b> <i>0.0 - 1.0</i> | 타일과 배경의 혼합에 영향을 줍니다. 순응은 하이맵을 엄격하게 유지하고 순응은 배경 모양을 따르는 것을 의미합니다. 예를 들어 나뭇잎과 스틱에 적합합니다. |
| <b>일치된 배경 매끄럽게</b> <i>0.0 - 2.0</i> | 이전 효과의 매끄러움 값으로, 잘못되거나 극단적인 변화를 방지할 수 있습니다. |
| <b>배경 경사에서 기울이기</b> <i>0.0 - 1.0</i> | 배경 경사에 의해 제어되는 타일 Height 조정/경사(계산된 표준) |
| <b>배경 경사 Smoothness</b> <i>0.0 - 2.0</i> | 이전 효과의 매끄러움 값으로, 잘못되거나 극단적인 변화를 방지할 수 있습니다. |
| <b>검정 픽셀 오려내기</b> <i>거짓/참</i> | 타일 기준 모양에서 전체 검정(0) 픽셀을 무시하도록 전환합니다. |
| <b>패턴 기준 병합</b> <i>거짓/참</i> | 배경과 타일 혼합 비헤이비어를 조정합니다. 타일은 배경과 교차하거나(False) 배경이 낮을 때 재정의됩니다. |
| <b>마스킹</b> |  |
| <b>무작위 마스크</b> <i>0.0 - 1.0</i> | 타일을 임의로 숨깁니다. 이 값이 높을수록 타일이 더 많이 사라집니다. |
| <b>마스크 무작위 맵 승수</b> <i>0.0 - 1.0</i> | 타일 숨기기를 시작할 때 마스크 맵을 검색합니다. |
| <b>배경에서 마스크 경사</b> <i>-1.0 - 1.0</i> | [배경 맵 경사](계산된 표준)를 사용하여 타일을 숨깁니다. |
