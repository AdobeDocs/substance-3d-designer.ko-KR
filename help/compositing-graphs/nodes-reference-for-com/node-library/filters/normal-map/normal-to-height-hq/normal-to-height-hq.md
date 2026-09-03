---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/normal-map/normal-to-height-hq.html"
breadcrumb-title: ''
description: Height HQ에 수직 노드를 사용하면 표면 세부 정보 추출을 위해 노멀 맵을 고품질 높이 맵으로 변환할 수 있습니다.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Normal Map > Normal To Height HQ
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Height HQ에 수직
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '190'
ht-degree: 3%

---


# Height HQ에 수직

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](normal-to-height-hq.resources/normal-to-height-hq-01.png){width="128px"}

<b>내부:</b> 필터 > 노멀 맵

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 설명

탄젠트 공간 정규맵을 다시 Heightmap으로 변환하려는 역방향 변환 노드입니다. 이 Height은 고급 노드입니다. [노드에 대한 일반](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/normal-map/normal-to-height/normal-to-height.md)은(는) 옵션이 적으며 다른 계산을 사용합니다.

Normalmap 소스만 있지만 Heightmap과 결합하는 작업을 수행하려는 경우에 유용합니다. Height이 [일반]으로 변환되는 프로세스의 특성상 정보가 손실되므로 이 경우 100% 정확한 결과를 제공할 수 없다는 점을 명심하십시오. 올바르게 생성된 Heightmap은 절대 바꿀 수 없습니다!

</td>
</tr>
</table>

<a name="parameters"></a>

## 매개변수

|  |  |
|:---|:---|
| <b>표준 형식</b> <i>DirectX, OpenGL</i> | 서로 다른 표준 맵 포맷 사이를 전환합니다(녹색 채널을 반전합니다). |
| <b>부조 균형</b> <i>0.0 - 1.0</i> | 저주파 바이어스와 고주파 바이어스 사이의 혼합. |
| <b>Height 강도</b> <i>0.0 - 1.0</i> | 하이트맵의 강도 또는 승수는 전체 불투명도와 약간 비슷하게 작동합니다. |
| <b>Height 표준화</b> <i>거짓/참</i> | [자동 수준](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/auto-levels/auto-levels.md)과 같이 완전한 대비를 사용하도록 Heightmap 범위를 자동으로 조절합니다. |
| <b>품질</b> <i>보통, 높음</i> | 속도 또는 품질 사이를 전환합니다. |

## 예

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="normal-to-height-hq.resources/normal-to-height-hq-02.png" />
        </td>
    </tr>
</table>
