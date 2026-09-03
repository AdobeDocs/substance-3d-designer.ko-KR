---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/non-uniform-directional-warp.html"
breadcrumb-title: ''
description: 다양한 왜곡 효과를 만들기 위해 Non Uniform Directional Warp 노드를 사용하여 균일하지 않은 방향 뒤틀기를 적용합니다.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Non Uniform Directional Warp
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Non Uniform Directional Warp
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '293'
ht-degree: 5%

---


# Non Uniform Directional Warp

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](non-uniform-directional-warp.resources/non-uniform-directional-warp-01.png)![](non-uniform-directional-warp.resources/non-uniform-directional-warp-02.png)

<b>인:</b> 필터 > 효과

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 설명

[비균일 방향 비틀기]는 [방향 비틀기](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/directional-warp/directional-warp.md)의 고급 버전으로, 이미지 입력에 의해 비틀기의 강도와 방향이 제어되도록 합니다. [경사 흐림 효과](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/blurs/slope-blur/slope-blur.md)와 마찬가지 로 훨씬 더 많은 제어를 허용하고 매우 유용하고 흥미로운 이미지 왜곡을 만들 수 있습니다.

사용자 지정 맵 입력을 통해 각도를 제어할 수 있다는 점에서 [다중 방향 뒤틀기](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/multi-directional-warp/multi-directional-warp.md)와 차이가 있지만, 다중 방향 뒤틀기는 매개 변수를 통해 방향만 제어할 수 있습니다. 그러면 다른 방법으로는 불가능한 고급 후행 및 곡선 효과를 만들 수 있습니다.

</td>
</tr>
</table>

<a name="inputs"></a>

## 입력

|  |  |
|:---|:---|
| <b>입력</b> <i>회색 음영 입력</i> | 뒤틀기가 적용될 기본 맵입니다. |
| <b>강도 입력</b> <i>회색 음영 입력</i> | 뒤틀기 효과의 강도를 제어하는 필수 마스크 맵은 회색 음영이어야 합니다. |
| <b>뒤틀기 각도 입력</b> <i>회색 음영 입력</i> | 뒤틀기 효과의 [각도]를 제어하는 필수 마스크 맵은 회색 음영이어야 합니다. |

<a name="parameters"></a>

## 매개변수

|  |  |
|:---|:---|
| <b>강도</b> <i>0.0 - 20.0</i> | 뒤틀기 효과의 강도 및 픽셀을 얼마나 멀리 밀지 설정합니다. |
| <b>뒤틀기 각도</b> <i>0.0 - 1.0</i> | [뒤틀기] 효과를 적용할 각도나 방향을 설정합니다. |
| <b>뒤틀기 각도 입력 승수</b> <i>0.0 - 1.0</i> | [뒤틀기 각도] 입력 맵의 효과를 설정합니다. 뒤틀기 각도 입력 맵은 0부터 이 매개 변수 값까지 보간하는 데 사용됩니다. |
| <b>트레일 모드</b> <i>최소, 최대, 평균</i> | 트레일 혼합 방식을 설정합니다. |
| <b>트레일 길이</b> <i>0.0 - 1.0</i> | 트레일 길이를 설정합니다. |
| <b>흔적 페이드</b> <i>0.0 - 1.0</i> | 각 Trail이 페이드 아웃되는 양을 설정합니다. |
| <b>트레일 곡선</b> <i>-1.0 - 1.0</i> | 트레일 페이드가 0이 아닌 경우에만 효과가 적용됩니다. 페이드 효과의 작동 방식을 설정합니다. |
