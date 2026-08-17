---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/pbr-utilities/pbr-render-mapping.html"
breadcrumb-title: ''
description: PBR 렌더링 매핑 노드를 사용하여 재질 출력을 다른 PBR 렌더링 매핑 형식으로 변환할 수 있습니다.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > PBR Utilities > PBR Render Mapping
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: PBR 렌더링 매핑
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '193'
ht-degree: 1%

---


# PBR 렌더링 매핑

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/pbr-render-mapping-color.png)![](../../../../../../assets/pbr-render-mapping-grayscale.png)

## PBR 렌더링 매핑(색상/회색 음영)

**내부:** *재질 필터/PBR 유틸리티*

**단순**

</td>
<td style="border: 0;" valign="top">

## 설명

[PBR 렌더링 노드](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/pbr-utilities/pbr-render/pbr-render.md)에 대한 확장 노드입니다. 이 확장 노드를 사용하면 이전 [PBR 렌더링](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/pbr-utilities/pbr-render/pbr-render.md)에서 도형에 별도의 텍스처를 매핑할 수 있습니다. 주요 목표는 [PBR 렌더링](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/pbr-utilities/pbr-render/pbr-render.md)에서 분리된 각 채널을 다시 모양에 매핑하여 아래 예제와 같이 복합 맵 채널 분석을 만드는 것입니다. PBR 렌더링 매핑 노드를 구성 요소로 사용하여 고유한 합성 방법과 마스크를 자유롭게 만들 수 있습니다.

두 가지 유형의 데이터에는 [색상]과 [회색 음영] 버전이 있습니다. 확산 맵에는 [색상]을 사용하고, 거칠기, 금속 및 기타 회색 음영 맵에는 [회색 음영]을 사용합니다.

### 입력

* **텍스처**: *색상/회색 음영 입력*\
  모양에 매핑할 텍스처.
* **UV**: *색상 입력* PBR 렌더링 노드에서 필수 UV 데이터 입력](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/pbr-utilities/pbr-render/pbr-render.md)[

## 매개변수

* **배경색**: *(색상 값)*배경에서 사용할 단색 값을 설정합니다.

## 예제 이미지

예는 [선형 그레이디언트](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/gradient-linear-1/gradient-linear-1.md)에서 [히스토그램 선택](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/histogram-select/histogram-select.md)을 마스크로 사용하는 네 개의 다른 PBR 렌더링 매핑 노드의 합성입니다.

![](../../../../../../assets/pbr-render-mapping-ex.png){width="256px"}

![](../../../../../../assets/pbr-render-mapping-ex-2.png){width="256px"}

</td>
</tr>
</table>
