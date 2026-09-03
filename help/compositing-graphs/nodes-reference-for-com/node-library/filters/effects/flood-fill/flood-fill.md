---
helpx_url: "https://helpx.adobe.com/kr/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/flood-fill.html"
breadcrumb-title: ''
description: 마스크 및 텍스처 처리 효과를 만들기 위해 Flood Fill 노드를 사용하여 비슷한 색상의 연결된 영역을 채웁니다.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Flood Fill
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Flood Fill
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '339'
ht-degree: 1%

---


# Flood Fill

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](flood-fill.resources/flood-fill-01.png){width="128px"}

<b>인:</b> 필터 > 효과

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 설명

Flood Fill은 기본 이진 타일 텍스처에 훨씬 더 많은 변형을 추가할 수 있는 고급 효과 세트의 일부입니다. 이 글꼴은 그 자체로 사용되지는 않습니다. 대신 [기타 Flood Fill] 효과의 출발점에 가깝습니다. 이렇게 분리된 별도의 데이터를 사용하면 보다 역동적이고 최적화되어 보다 파괴적인 워크플로를 수행할 수 있습니다.

다른 Flood Fill 효과는 [그레이디언트에 Flood Fill](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/flood-fill-to-gradient/flood-fill-to-gradient.md), [색상/회색 음영에 Flood Fill](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/flood-fill-grayscale-col/flood-fill-to-grayscale-color.md), [무작위 회색 음영에 Flood Fill](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/flood-fill-random-gra/flood-fill-to-random-grayscale.md), [무작위 색상에 Flood Fill](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/flood-fill-random-color/flood-fill-to-random-color.md), [상자 크기에 Flood Fill](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/flood-fill-to-bbox-size/flood-fill-to-bbox-size.md), [위치에 Flood Fill](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/flood-fill-to-position/flood-fill-to-position.md), [Flood Fill 매퍼](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/flood-fill-mapper/flood-fill-mapper.md) 및 [색인에 Flood Fill](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/flood-fill-to-index/flood-fill-to-index.md)입니다

>[!WARNING]
>
> 입력 맵은 Flood Fill 작업에 적합해야 합니다. 모든 타일이 모든 픽셀에 대해 완전 검정(0,0,0)인 테두리로 다른 선과 분리되는 이진 맵(흑백만, 회색 음영 없음)인 것이 이상적입니다. 완벽한 후보 예로는 [Tile Generator](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/tile-generator/tile-generator.md)이 있습니다.
> 
> 일반적으로 회색 음영, 경사 값을 사용할 때 타일이 완전히 검정색 픽셀로 분리되지 않으면 문제가 발생합니다. 결과에서 전체적으로 빨간색 값이 부족하거나 이상한 아티팩팅 선이 있어 이러한 점을 확인할 수 있습니다. 이러한 경우 입력 맵의 대비를 조정하거나 입력 맵을 전환합니다. 안전/속도(Safety/Speed) 할인 설정을 변경하여 어떤 것이 개선되는지 확인하십시오.

</td>
</tr>
</table>

<a name="parameters"></a>

## 매개변수

|  |  |
|:---|:---|
| <b>안전/속도 트레이드 오프</b> <i>단순하거나 작은 모양, 복잡하거나 큰 모양, 실패 모드 없음</i> | 입력 모양에 가장 적합한 계산 모드로 설정합니다. 올바른 모드가 선택된 경우 훨씬 더 정확한 결과를 얻을 수 있습니다. |
| <b>고급 옵션</b> <i>고급 매개 변수 및 출력/숨기기</i> 표시 |  |
| <b>안전/속도 무시</b> <i>-1 - 100</i> | 고급 옵션 이 켜져 있는 경우에만 표시됩니다. 내부 기능을 재정의할 수 있습니다. 매우 고급 기능으로 고유한 효과를 만들거나 디버깅하는 데 사용됩니다. |

## 예

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="flood-fill.resources/flood-fill-02.png" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="flood-fill.resources/flood-fill-03.png" />
        </td>
    </tr>
</table>

Flood Fill 결과의 좋은 그리고 나쁜 예.
