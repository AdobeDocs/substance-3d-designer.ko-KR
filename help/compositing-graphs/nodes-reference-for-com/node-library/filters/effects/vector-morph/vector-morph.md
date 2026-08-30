---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/vector-morph.html"
breadcrumb-title: ''
description: 매끄러운 전환을 위해 벡터 필드를 사용하여 두 입력 간의 텍스처를 모핑하려면 벡터 모핑 노드를 사용합니다.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Vector Morph
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 벡터 형태
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '188'
ht-degree: 2%

---


# 벡터 형태

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](vector-morph.resources/vector-morph-grayscale.png)![](vector-morph.resources/vector-morph.png)

<b>인:</b> 필터 > 효과

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 설명

벡터 맵을 사용하여 입력 이미지를 왜곡합니다. 이 효과는 표준 맵을 사용한 UV 왜곡 또는 비디오 게임 셰이더에서 &quot;플로우 맵&quot;을 사용하는 것과 유사합니다. 입력 픽셀은 벡터 맵의 빨강 및 녹색 값에 정의된 벡터에 의해 이동됩니다.

이 노드 자체는 가장 사용하기 어려운 것이 아니라 적절한 벡터 맵을 만드는 것이 중요합니다. 변형 작업 시 정밀도를 보장하기 위해 가장 높은 비트 깊이로 작업하는 것이 좋습니다.

벡터 모프는 [벡터 뒤틀기](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/vector-warp/vector-warp.md)와 매우 유사합니다. 주된 차이점은 이 모프 노드가 캔버스 경계 밖으로 밀릴 때 결과를 &quot;반복&quot; 또는 &quot;바둑판식&quot;하지 않는다는 것입니다. 대신 모서리를 클램프하고 반복합니다.

</td>
</tr>
</table>

<a name="inputs"></a>

## 입력

|  |  |
|:---|:---|
| <b>입력</b> <i>색상/회색 음영 입력</i> | 뒤틀기 대상이어야 하는 소스 입력입니다. |
| <b>벡터 필드</b> <i>색상 입력</i> | 뒤틀기를 제어하는 데 사용되는 벡터 맵 |

<a name="parameters"></a>

## 매개변수

|  |  |
|:---|:---|
| <b>금액</b> <i>0.0 - 1.0</i> | 뒤틀기 효과의 강도를 설정합니다. 이 설정은 벡터 맵에 대한 승수로 작동합니다. |
