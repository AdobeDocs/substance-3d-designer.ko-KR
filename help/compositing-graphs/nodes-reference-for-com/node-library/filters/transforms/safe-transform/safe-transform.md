---
helpx_url: "https://helpx.adobe.com/kr/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/transforms/safe-transform.html"
breadcrumb-title: ''
description: 텍스처 경계를 보존하고 아티팩트를 피하는 동안 안전한 변환 노드를 사용합니다.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Transforms > Safe Transform
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 안전한 변형
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '185'
ht-degree: 5%

---


# 안전한 변형

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](safe-transform.resources/safe-transform-01.png)

![](safe-transform.resources/safe-transform-02.png)

<b>필터</b>:

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 설명

[변환-D](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/transformation-2d/transformation-2d.md)의 타일링 안전 버전. 작은 오프셋과 회전으로 인해 타일링 없이 픽셀 세부 묘사를 손실하지 않고(선명도/선명도 손실) 비율 조정, 회전 및 오프셋을 수행할 수 있습니다.

최대 제어 또는 완벽한 선명도(sharpness)가 필요할 때 유용합니다.

</td>
</tr>
</table>

<a name="parameters"></a>

## 매개변수

|  |  |
|:---|:---|
| <b>타일</b> <i>1 - 16</i> | 타일링하여 입력 크기를 줄입니다. |
| <b>오프셋 모드</b> <i>수동, 무작위</i> | 수동으로 정의된 오프셋 대신 임의의 오프셋으로 전환합니다. |
| <b>오프셋</b> <i>0.0 - 1.0</i> | 결과를 이동하거나 변환합니다. 픽셀이 스냅되고 보간되지 않았는지 확인합니다. |
| <b>회전</b> <i>0.0 - 1.0</i> | 각도를 따라 입력을 회전합니다. |
| <b>타일 보호 회전</b> <i>거짓/참</i> | 픽셀을 흐리게 하지 않는 안전한 값에 스냅할지 여부를 포함하여 회전 동작을 결정합니다. |
| <b>대칭</b> <i>없음, X, Y, X+Y</i> |  |
| <b>배경색</b> <i>(색상 값)(색상 버전만)</i> |  |
| <b>맵 모드</b> <i>자동, 수동</i> | 밉매핑 모드를 결정합니다. 이를 수동으로 설정하면 결과가 더 선명해집니다. |
| <b>밉맵 레벨</b> <i>0 - 10</i> | [밉맵] 모드를 [수동]으로 설정하면 다른 밉맵을 선택할 수 있습니다. |
