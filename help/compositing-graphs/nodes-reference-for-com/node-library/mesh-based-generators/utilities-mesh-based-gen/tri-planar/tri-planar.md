---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/utilities-mesh-based-generators/tri-planar.html"
breadcrumb-title: ''
description: 3개의 평면 노드를 사용하여 3개의 직교 평면에서 텍스처를 투영하여 복잡한 지오메트리에 대한 원활한 텍스처 매핑을 수행할 수 있습니다.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Utilities (Mesh Based Generators) > Tri Planar
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 삼중 평면
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '443'
ht-degree: 6%

---


# 삼중 평면

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](tri-planar.resources/triplanar-1.png){width="128px"}

![](tri-planar.resources/triplanar-grayscale.png){width="128px"}

<b>내부:</b> 메시 기반 생성기 > 유틸리티

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 설명

이 고급 노드는 베이킹된 위치 및 월드 스페이스 표준 데이터를 기반으로 2D에서 삼평면 투영 매핑을 수행합니다. 이는 메쉬 자체를 기반으로 UV 좌표를 (대부분) 이음새가 없는 매핑으로 완전히 변환하는 것을 의미합니다.

이것은 매번 다시 구울 필요 없이 솔기를 피하기 위한 좋은 방법입니다 (제빵사와 유사한 것을 달성 할 수 있습니다). 단점은 이 노드가 상당히 무겁기 때문에 빠르지 않다는 점이다.

베이크는 고정밀이어야 한다는 점을 염두에 두십시오. 8비트 베이크는 매우 좋은 결과로 이어지지 않습니다.

</td>
</tr>
</table>

<a name="inputs"></a>

## 입력

|  |  |
|:---|:---|
| <b>위치</b> <i>색상 입력</i> | 위치 맵을 구웠습니다. 16비트 이상의 정밀도를 사용하는 것이 좋습니다. |
| <b>월드 스페이스 표준</b> <i>색상 입력</i> | Baked World Space Normal 지도, 이상적으로 16비트 이상의 정밀도. |
| <b>입력 X</b> <i>색상 입력(회색 음영 입력)</i> | 삼각면 투영을 통해 UV에서 월드 공간으로 다시 매핑할 맵을 입력합니다. [이미지 입력]을 1로 설정한 경우 모든 축에 사용되고, [X 축]을 3으로 설정한 경우 모든 축에 사용됩니다. |
| <b>입력 Y</b> <i>색상 입력(회색 음영 입력)</i> | 이미지 입력이 3으로 설정된 경우에만 가능합니다. Y축의 UV에서 월드 공간으로 다시 매핑할 맵을 입력합니다. |
| <b>입력 Z</b> <i>색상 입력(회색 음영 입력)</i> | 이미지 입력이 3으로 설정된 경우에만 가능합니다. Z축의 UV에서 월드 공간으로 다시 매핑할 맵을 입력합니다. |

<a name="parameters"></a>

## 매개변수

|  |  |
|:---|:---|
| <b>투영</b> <i>모든 축, X만, Y만, Z만</i> | 혼합할 축을 설정합니다. |
| <b>이미지 입력</b> <i>1개 입력, 3개 입력</i> | 모든 축에 하나의 맵을 사용할지, 아니면 축당 특정 맵을 사용할지 설정합니다. |
| <b>혼합 모드</b> <i>선형, 고급</i> | 정확도와 정밀도를 높입니다. |
| <b>대비 혼합</b> <i>0.001 - 1.0</i> | 전환 대비, 매끄러운 전환 또는 거친 전환을 혼합합니다. |
| <b>정규화 요소</b> <i>0.0 - 1.0</i> | 혼합 영역에서 대비의 손실을 복원하여 투영 혼합을 개선합니다. |
| <b>텍스처 타일링</b> <i>0.0 - 10.0</i> | 입력 텍스처를 바둑판식으로 배열한 횟수입니다. |
| <b>전역 회전</b> <i>0.0 - 1.0</i> | 모든 축에 대한 전역 회전입니다. |
| <b>미러링된 투영 수정</b> <i>거짓/참</i> | 대칭복사된 투영을 처리하는 방법을 설정합니다. |
| <b>회전 X</b> <i>0.0 - 1.0</i> | 투영 X축에 대한 개별 회전 |
| <b>회전 Y</b> <i>0.0 - 1.0</i> | 투영 Y축에 대한 개별 회전입니다. |
| <b>회전 Z</b> <i>0.0 - 1.0</i> | 투영 Z축을 통한 개별 회전 |
| <b>오프셋 X</b> <i>0.0 - 1.0</i> | 투영 X축 위의 오프셋 |
| <b>임의 오프셋 X</b> <i>0.0 - 1.0</i> | X축 오프셋의 임의화를 허용합니다. |
| <b>오프셋 Y</b> <i>0.0 - 1.0</i> | 투영 Y축 위로 오프셋합니다. |
| <b>임의 오프셋 Y</b> <i>0.0 - 1.0</i> | Y축 오프셋의 임의화를 허용합니다. |
| <b>오프셋 Z</b> <i>0.0 - 1.0</i> | 투영 Z축 위로 오프셋 |
| <b>임의 오프셋 Z</b> <i>0.0 - 1.0</i> | Z축 오프셋의 임의화를 허용합니다. |
