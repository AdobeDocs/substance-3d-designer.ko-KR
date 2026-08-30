---
helpx_url: "https://helpx.adobe.com/kr/substance-3d-designer/substance-compositing-graphs.html"
breadcrumb-title: ''
description: Substance 3D Designer에서 프로시저 텍스처 및 재질 작업 과정을 만들기 위한 Substance 합성 그래프에 대해 알아봅니다.
helpx_creative_field: ""
helpx_description: Designer > Substance graphs
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Substance 그래프
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '345'
ht-degree: 1%

---


# Substance 그래프

<table>
<tr style="border: 0;">
<td width="16.67%" style="border: 0;" valign="top">

[![](substance-compositing-graphs.resources/graph-5.png){width="120px"}](https://substance3d.adobe.com/)

</td>
<td width="100.00%" style="border: 0;" valign="top">

[Substance 그래프](https://substance3d.adobe.com/)는 Substance 3D Designer에서 만든 주요 그래프 유형입니다. 그 목적은 설정된 해상도, 색상 또는 모양에 제한되지 않는 <b>2D 이미지 데이터를 생성하고 처리하는 것</b>입니다. 이 제품은 정적인 사전 설정 결과뿐만 아니라 매우 다양한 이미지 처리 및 생성 도구입니다.

단순한 흑백 패턴, 다른 이미지에서만 실행되며 콘텐츠를 자체 생성하지 않는 필터 또는 여러 채널이 있는 완전한 절차 자료 형태로 결과를 얻을 수 있습니다.

Substance 그래프는 [가장 널리 지원되는 그래프 유형](../getting-started/overview/overview.md)이며 다양한 작업 과정에서 내보내고 사용할 수 있습니다.

</td>
</tr>
</table>

## 예

아래에서 일반적인 사용 사례의 몇 가지 예를 확인할 수 있습니다.

+++단순 도형
![Substance 그래프의 단순 모양](substance-compositing-graphs.resources/simpleshape.png "Substance 그래프의 단순 모양"){width="512px"}



데칼에 대한 간단한 마스크 모양은 [텍스트 조각](../compositing-graphs/nodes-reference-for-com/atomic-nodes/text/text.md)과 [디스크 모양](../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/shape/shape.md)을 생성하고, 디스크에서 [가장자리를 추출](../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/edge-detect/edge-detect.md)한 다음 최종적으로 [함께 혼합](../compositing-graphs/nodes-reference-for-com/atomic-nodes/blend/blend.md)한 다음 최종 [출력](../compositing-graphs/nodes-reference-for-com/atomic-nodes/output/output.md)으로 설정하여 만듭니다.

숫자가 있는 텍스트 또는 가장자리의 Thickness을 외부로 노출하여 보다 역동적인 그래프를 만들 수 있습니다.

+++

+++조정 필터
![Substance 그래프의 조정 필터](substance-compositing-graphs.resources/simplefilter.png "Substance 그래프의 조정 필터"){width="512px"}



필터 그래프는 노멀 맵을 [입력](../compositing-graphs/nodes-reference-for-com/atomic-nodes/input/input.md)(사용자 지정 미리 보기 포함)으로 받아들이고, [곡률을 변환](../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/curvature-smooth/curvature-smooth.md)한 다음 [대비를 조정](../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/histogram-scan/histogram-scan.md)하여 최종 [출력](../compositing-graphs/nodes-reference-for-com/atomic-nodes/output/output.md)으로 볼록 가장자리 마스크를 만듭니다.

[막대 그래프]에 설정된 대비 값을 표시할 수 있으므로 동적 입력 슬롯과 결합하여 간단하지만 유용한 필터가 됩니다.

+++

+++완전 재질
![Substance 그래프의 전체 재질](substance-compositing-graphs.resources/simplematerial.png "Substance 그래프의 전체 재질"){width="512px"}



더 복잡한 그래프[두 기본 재질을 혼합](../compositing-graphs/nodes-reference-for-com/node-library/material-filters/blending-material/material-blend/material-blend.md)합니다. 하나[기본 재질](../compositing-graphs/nodes-reference-for-com/node-library/material-filters/pbr-utilities/base-material/base-material.md)은(는) 간단하게 유지되며 다른 하나는 일부 사용자 지정 입력을 사용하여 관심을 추가합니다. 마스크는 최종 [출력](../compositing-graphs/nodes-reference-for-com/atomic-nodes/output/output.md)(으)로 설정되기 전에 두 재질 중 표시할 재질을 결정하는 데 사용됩니다.

이 예제에서는 [링크 만들기 모드](../interface/the-graph-view/link-creation-modes/link-creation-modes.md)를 사용하여 여러 링크 사용을 단순화합니다.

+++
