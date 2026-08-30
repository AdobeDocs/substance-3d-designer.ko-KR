---
helpx_url: "https://helpx.adobe.com/kr/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/blending-material/material-color-blend.html"
breadcrumb-title: ''
description: 재질 색상 혼합 노드를 사용하여 복합 재질 효과를 만들기 위해 재질 간에 색상 채널을 혼합합니다.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > Blending (Material) > Material Color Blend
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 재질 색상 혼합
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '455'
ht-degree: 2%

---


# 재질 색상 혼합

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](material-color-blend.resources/material-color-blend.png){width="128px"}

<b>내부:</b> 재질 필터 > 혼합

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 설명

이 노드를 사용하면 맨 위에 단색을 혼합하여 다중 채널 전체 재질을 조정할 수 있습니다. 이는 [재질 조정 혼합](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/blending-material/material-adjustment-blend/material-adjustment-blend.md)의 주된 차이점으로, 채널에는 [레벨](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/levels/levels.md) 유형의 조정만 허용되지만 이 노드에서는 단색과 함께 [혼합](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/blend/blend.md) 유형의 조정을 사용합니다.

이 확산은 단색 힌트를 채널이나 기본 색상에 적용하거나 설정된 단색 값을 사용하여 다른 채널을 &quot;병합&quot;하려는 경우에 가장 유용합니다.

</td>
</tr>
</table>

<a name="inputs"></a>

## 입력

|  |  |
|:---|:---|
| <b>ColorID</b> <i>색상 입력</i> | 노드의 효과를 마스킹하는 데 사용되는 마스크 슬롯입니다. |
| <b>회색조 마스크</b> <i>회색 음영 입력</i> | 노드의 효과를 마스킹하는 데 사용되는 마스크 슬롯입니다. |

<a name="parameters"></a>

## 매개변수

|  |  |
|:---|:---|
| <b>채널</b> | 예를 들어 [금속/거칠음] 대신 [Specular/광택] 맵을 사용하는 경우 이 그룹에서 재질 채널을 켜거나 끌 수 있습니다. |
| <b>확산</b> |  |
| <b>색상</b> <i>(색상 값)</i> | 확산 채널 위에서 혼합할 색상 값입니다. |
| <b>불투명도</b> <i>0.0 - 1.0</i> | 전경과 배경 간 불투명도 혼합. |
| <b>혼합 모드</b> <i>표준, 추가, 빼기, 곱하기, 추가/하위, 최대, 최소, 스위치</i> | 작업에 사용할 혼합 모드입니다. |
| <b>기본 색상</b> | [확산] 그룹에서와 같은 옵션을 사용하여 이 채널 위에 단색을 혼합합니다. |
| <b>표준</b> |  |
| <b>원본</b> <i>Height, 마스크</i> |  |
| <b>혼합 모드</b> <i>결합, 혼합</i> |  |
| <b>Height 강도</b> <i>0.0 - 1.0</i> |  |
| <b>Height 불투명도</b> <i>0.0 - 1.0</i> |  |
| <b>형식</b> <i>DirectX, OpenGL</i> |  |
| <b>Specular</b> | [확산] 그룹에서와 같은 옵션을 사용하여 이 채널 위에 단색을 혼합합니다. |
| <b>발광</b> | [확산] 그룹에서와 같은 옵션을 사용하여 이 채널 위에 단색을 혼합합니다. |
| <b>광택</b> | [확산] 그룹에서와 같은 옵션을 사용하여 이 채널 위에 단색을 혼합합니다. |
| <b>거칠음</b> | [확산] 그룹에서와 같은 옵션을 사용하여 이 채널 위에 단색을 혼합합니다. |
| <b>금속</b> | [확산] 그룹에서와 같은 옵션을 사용하여 이 채널 위에 단색을 혼합합니다. |
| <b>Specular level</b> | [확산] 그룹에서와 같은 옵션을 사용하여 이 채널 위에 단색을 혼합합니다. |
| <b>주변 오클루전</b> | [확산] 그룹에서와 같은 옵션을 사용하여 이 채널 위에 단색을 혼합합니다. |
| <b>Height</b> | [확산] 그룹에서와 같은 옵션을 사용하여 이 채널 위에 단색을 혼합합니다. |
| <b>불투명도</b> | [확산] 그룹에서와 같은 옵션을 사용하여 이 채널 위에 단색을 혼합합니다. |
| <b>색상 ID 마스크</b> <i>거짓/참</i> | 회색 음영 마스크 대신 색상 ID 마스크를 사용합니다. 이 옵션은 한 가지 색상에만 적용됩니다!<br><br>아래 옵션을 모두 사용할 수 있습니다. |
| <b>색상</b> <i>(색상 값)</i> | 선택하여 흰색으로 변환할 색상입니다. |
| <b>허용량</b> <i>0.01 - 1.0</i> | 선택한 색상이 인접 색상으로 혼합되는 정도입니다. |
| <b>패딩</b> <i>0.0 - 1.0</i> | 선택한 색상의 전환 대비입니다. |
