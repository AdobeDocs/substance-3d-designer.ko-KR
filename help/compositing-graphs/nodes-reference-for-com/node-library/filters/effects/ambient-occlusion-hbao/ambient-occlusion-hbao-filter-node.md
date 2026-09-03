---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/ambient-occlusion-hbao-filter-node.html"
breadcrumb-title: ''
description: 앰비언트 오클루전 HBAO 필터 노드를 사용하면 사실적인 음영을 위해 수평선 기반 알고리즘을 사용하여 앰비언트 오클루전 맵을 생성할 수 있습니다.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Ambient Occlusion (HBAO) (Filter Node)
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 앰비언트 오클루전(HBAO)(필터 노드)
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '197'
ht-degree: 5%

---


# 앰비언트 오클루전(HBAO)(필터 노드)

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](ambient-occlusion-hbao-filter-node.resources/ambient-occlusion-hbao-filter-node-01.png){width="128px"}

<b>인:</b> 필터 > 효과

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 설명

Heightmap을 입력으로 받아 앰비언트 오클루전 맵을 생성합니다. 원래 화면-공간 실시간 AO 생성을 위한 알고리즘인 수평선 기반 앰비언트 오클루전(Horizon-Based Animation)을 사용한다. 프로시저 Heightmaps에서 프로시저 AO 지도를 만드는 데 매우 유용합니다.

보다 향상되었지만 속도가 느린 다른 버전의 AO는 [앰비언트 오클루전(RTAO)](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/ambient-occlusion-rtao/ambient-occlusion-rtao.md)을 참조하세요

</td>
</tr>
</table>

<a name="parameters"></a>

## 매개변수

|  |  |
|:---|:---|
| <b>세계 단위 사용</b> <i>거짓/참</i> | 월드 또는 화면 공간 단위 사용을 전환합니다. 보다 정확하게 제어할 수 있는 추가 매개 변수를 활성화합니다. |
| <b>Height 깊이</b> <i>0.0 - 1.0</i> | [세계 단위]가 [거짓]으로 설정된 경우에만 사용됩니다. 전역 크기 조절을 제어합니다. |
| <b>표면 크기</b> <i>0.0 - 1000.0</i> | [세계 단위]가 True로 설정된 경우에만 사용됩니다. 전역 크기 조절을 제어합니다. |
| <b>Height 크기(cm)</b> <i>0.0 - 1000.0</i> | [세계 단위]가 True로 설정된 경우에만 사용됩니다. 전역 크기 조절을 제어합니다. |
| <b>반경</b> <i>0.0 - 1.0</i> | AO의 확산을 제어합니다. |
| <b>품질</b> <i>4개 샘플, 8개 샘플, 16개 샘플</i> | 계산에 사용되는 샘플 양을 결정하여 품질 레벨을 설정합니다. |
| <b>GPU 최적화</b> <i>거짓/참</i> | 내부 GPU 최적화를 구현하고 처리 속도를 높입니다. |

## 예

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="ambient-occlusion-hbao-filter-node.resources/ambient-occlusion-hbao-filter-node-02.png" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="ambient-occlusion-hbao-filter-node.resources/ambient-occlusion-hbao-filter-node-03.png" />
        </td>
    </tr>
</table>
