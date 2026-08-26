---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/atomic-nodes/warp.html"
breadcrumb-title: ''
description: 뒤틀기 노드를 사용하여 텍스처에 왜곡 효과를 적용하여 뒤틀기 및 변위 효과를 만듭니다.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Atomic nodes > Warp
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 뒤틀기
user-guide-description: ''
user-guide-title: ''
source-git-commit: 5b9c9d12e2ccd76f75ec2a74815f9c68c43c06a2
workflow-type: tm+mt
source-wordcount: '263'
ht-degree: 9%

---


# 뒤틀기

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Atomic node: 뒤틀기](../../../../assets/comp_warp_1.png "Atomic node: 뒤틀기"){width="200px"}

</td>
<td width="100.00%" style="border: 0;" valign="top">

별도의 그레이디언트 입력에서 계산된 기울기 정보에 따라 입력 이미지의 픽셀 값을 변위시켜 변형을 일으킵니다.

[방향 비틀기]와는 달리 이 노드는 [그레이디언트 입력]의 경사 또는 그레이디언트에 의해 정의된 방향으로 흰색 영역에서 균일하게 밀어냅니다.

</td>
</tr>
</table>

노드는 작업하기 약간 까다로울 수 있습니다. 효과의 결과는 그레이디언트 입력에 매우 크게 의존하기 때문입니다. 그레이디언트에 대한 작은 수정은 동일한 강도 값으로 큰 시각적 차이를 만들 수 있습니다. 이 노드의 [강도] 슬라이더뿐만 아니라 그레이디언트 입력의 [대비], [광도] 및 [비율]을 사용해 보십시오.

[표준] 맵에 익숙한 경우 이 노드의 작업은 그레이디언트 입력을 [표준 맵](../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/normal/normal.md)으로 변환한 다음 기본 입력을 표준 맵 벡터로 정의된 방향으로 왜곡하는 것과 비슷하다고 생각할 수 있습니다. 실제로 [벡터 뒤틀기](../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/vector-warp/vector-warp.md)에서도 이와 동일한 작업을 수행할 수 있습니다. [경사 흐림 효과](../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/blurs/slope-blur/slope-blur.md)에서도 유사한 효과를 확인할 수 있습니다.

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
| <b>강도</b> *부동* | 뒤틀기의 강도를 설정합니다. |
| <b>필터링 모드 입력</b> *부울* | 입력을 샘플링하는 데 가장 가까운 필터링을 사용할지 또는 쌍선형 필터링을 사용할지 여부를 제어합니다. |

## 입력 커넥터

|  |  |
| --- | --- |
| <b>입력</b> 기본 *회색 음영/색상* | 색상 또는 회색 음영 이미지입니다. |
| <b>그레이디언트 입력</b> *회색 음영* | 회색 음영 입력 이미지의 그레이디언트 경사에 따라 출력 이미지에서 뒤틀기 효과가 결정됩니다. |

## 출력 커넥터

|  |  |
| --- | --- |
| <b>출력</b> *회색 음영/색상* |  |

## 예

*곧 출시 예정*
