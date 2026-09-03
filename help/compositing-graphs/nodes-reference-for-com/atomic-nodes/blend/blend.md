---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/atomic-nodes/blend.html"
breadcrumb-title: ''
description: 혼합 노드 를 사용하여 합성 효과를 만드는 다양한 혼합 모드를 사용하여 두 텍스처를 혼합합니다.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Atomic nodes > Blend
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 혼합
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '332'
ht-degree: 9%

---


# 혼합

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Atomic node: Blend](blend.resources/blend-01.png "Atomic node: Blend"){width="200px"}

</td>
<td width="100.00%" style="border: 0;" valign="top">

지정된 혼합 모드와 선택 사항인 마스크를 사용하여 두 이미지를 결합합니다.

모든 Atomic 노드 중 가장 유용한 노드이며, [Substance 3D Designer](https://www.adobe.com/kr/products/substance3d-designer.html)에서 작성하는 거의 모든 그래프가 이 노드를 사용합니다.

</td>
</tr>
</table>

이 기능은 [Substance 3D Painter](https://www.adobe.com/products/substance3d-painter.html) 또는 [Photoshop](https://www.adobe.com/ch_fr/products/photoshop/landpa.html)에서 상위 레이어에 설정한 혼합 모드를 통해 서로 혼합되는 두 개의 레이어를 포함하는 것과 비슷합니다.

>[!TIP]
>
> [이 전용 페이지](../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/blend/blending-modes-des/blending-modes-description.md)의 혼합 노드에서 사용할 수 있는 혼합 모드에 대해 알아봅니다.

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
| <b>불투명도</b> *부동* | 배경에 혼합되는 전경 레이어의 불투명도입니다. 불투명도 입력에 대해 독립적으로 작동하고 이에 대한 추가 승수 역할을 합니다. |
| <b>혼합 모드</b> *정수* [정적](../../../../glossary/glossary.md) | 사용할 혼합 작업을 설정합니다.   혼합 모드에 대한 [전용 페이지](../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/blend/blending-modes-des/blending-modes-description.md)를 참조하십시오. |
| <b>Alpha 혼합</b> *정수* [정적](../../../../glossary/glossary.md) | 색상 입력에 Alpha 채널이 있는 경우 혼합 동작을 결정합니다.<ul data-preserve-html="true"> <li data-preserve-html="true">소스 알파 사용</li> <li data-preserve-html="true">알파 무시</li> <li data-preserve-html="true">직선 알파 혼합</li> <li data-preserve-html="true">미리 곱하기 알파 혼합</li> </ul> |
| <b>자르기 영역</b> *Float4* [Static](../../../../glossary/glossary.md) | 추가 불투명도 마스크처럼 작동하는 사용자 정의 자르기 영역을 설정할 수 있습니다. 자른 모든 영역에는 배경만 표시됩니다. |

## 입력 커넥터

|  |  |
| --- | --- |
| <b>전경</b> *회색 음영/색상* | 혼합 작업의 위쪽 또는 전경 레이어입니다. |
| <b>배경</b> 기본 *회색 음영/색상* | 혼합 작업의 아래쪽 또는 배경 레이어입니다. |
| <b>불투명도</b> *회색 음영* | 선택적 Alpha 마스크 입력입니다. |

>[!IMPORTANT]
>
> 혼합 노드에는 연결에 따라 회색 음영과 색상 사이를 전환하는 동적 입력이 있습니다.<b> 혼합 노드는 같은 유형</b>의 두 입력만 혼합할 수 있습니다.
> 
> 색상과 회색 음영 입력을 전경과 배경에 연결하면 빨간색 연결 점선이 표시되어 계산 오류가 있음을 나타냅니다.
> 
> 이는 신규 사용자가 색상 및 회색 음영 연결 문제를 겪는 가장 큰 이유입니다. 두 연결 모두 동일한 유형인지 확인하십시오!

## 출력 커넥터

|  |  |
| --- | --- |
| <b>출력</b> *회색 음영/색상* |  |

## 예

*곧 출시 예정*
