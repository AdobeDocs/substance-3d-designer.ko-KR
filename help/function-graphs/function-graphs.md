---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/function-graphs.html"
breadcrumb-title: ''
description: Designer에서 Substance 함수 그래프를 만들고 사용하여 사용자 정의 함수와 재사용 가능한 노드 네트워크를 만드는 방법을 알아봅니다.
helpx_creative_field: ""
helpx_description: Designer > Substance function graphs
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Substance 함수 그래프
user-guide-description: ''
user-guide-title: ''
source-git-commit: ea96f5a148246d20263c4ecf0b67d0b4a51f28a8
workflow-type: tm+mt
source-wordcount: '374'
ht-degree: 0%

---


# Substance 함수 그래프

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

[![](../assets/function-1.png){width="120px"}](https://substance3d.adobe.com/)

</td>
<td style="border: 0;" valign="top">

[Substance 함수 그래프](https://substance3d.adobe.com/) <b>이미지 데이터(전체 픽셀 집합) 대신 단일 값 처리</b>(정수, 부동 소수점, 벡터). 함수도 노드 네트워크가 있는 그래프이지만 [사용된 노드](../function-graphs/nodes-reference-for-fun/function-nodes-overview/function-nodes-overview.md)와 인터페이스는 [일반 Substance 그래프](../compositing-graphs/substance-compositing-graphs.md)와 다릅니다. 작업 과정은 완전히 <b>수학적 작업</b>을 기반으로 하며 이미지 미리 보기 축소판을 표시하지 않으므로 Substance 3D Designer에서 <b>훨씬 더 고급 작업 방법</b>이 됩니다.

함수는 다양한 컨텍스트에서 사용할 수 있습니다. 주로 [노출된 매개 변수](../compositing-graphs/manage-parameters/exposing-a-parameter/exposing-a-parameter.md)의 동작을 수정하고, [픽셀 프로세서](../compositing-graphs/nodes-reference-for-com/atomic-nodes/pixel-processor/pixel-processor.md) 또는 [FX-맵](../compositing-graphs/nodes-reference-for-com/atomic-nodes/fx-map/fx-map.md)의 동작을 작성하고, [그래프의 값을 사용합니다.](https://helpx.adobe.com/substance-3d/unlisted/documentation/sddoc/values-in-substance-3d-graphs-180192235.html)

</td>
</tr>
</table>

## 예

다음은 함수에 대한 일반적인 사용법의 몇 가지 예입니다.

### 단순 함수

![](../assets/lerpfunction_1.png)

노출된 매개 변수 컨텍스트의 단순 함수입니다. 0에서 1(이해하기 쉬운 범위)까지 지정되는 &quot;강도&quot;라는 입력 부동 소수점 값을 가져와서 0.1 - 0.8의 설정된 범위로 다시 매핑합니다. 즉, 사용자가 [강도]를 0으로 설정하면 내부 0.1이 사용되고, Ui를 1로 설정하면 0.8이 사용되며, 그 사이의 값은 선형적으로 보간됩니다. 이 유형의 함수는 [매개 변수를 노출](../compositing-graphs/manage-parameters/exposing-a-parameter/exposing-a-parameter.md)할 때 일반적으로 사용되지만 사용자 지정 함수를 사용할 때 사용됩니다.

이 함수는 HLSL 또는 GLSL과 유사한 의사 코드로 *lerp(0.1, 0.8, Intensity)*&#x200B;로 기록될 수도 있습니다.

### 고급 기능

![](../assets/pixel-function_1.png){width="545px"}

이 고급 기능은 두 번째 회색 음영 마스크 입력의 강도를 기반으로 색상 맵 입력의 색조를 조정하는 [픽셀 프로세서](../compositing-graphs/nodes-reference-for-com/atomic-nodes/pixel-processor/pixel-processor.md)의 내부 작업을 보여 줍니다.

시스템 &quot;$pos&quot; 변수로 두 입력을 모두 샘플링한 다음 Alpha을 제거하고, 색상 값을 HSL로 변환하고, 샘플링된 회색 음영 값과 곱하여 색조 구성 요소를 수정합니다. 그런 다음 벡터를 다시 어셈블하고 HSL을 다시 RGB으로 변환한 다음 최종 출력을 위해 Alpha을 다시 추가합니다.

의사 코드에서는 이 함수가 한 줄에 맞지 않는 훨씬 더 복잡한 함수일 것이다.
