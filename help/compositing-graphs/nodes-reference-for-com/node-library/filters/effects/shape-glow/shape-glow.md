---
helpx_url: "https://helpx.adobe.com/kr/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/shape-glow.html"
breadcrumb-title: ''
description: '[모양 광선] 노드를 사용하여 모양과 텍스처에 광선 효과를 추가하여 빛나는 분위기 있는 시각 효과를 만들 수 있습니다.'
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Shape Glow
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Shape Glow
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '181'
ht-degree: 1%

---


# Shape Glow

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/shape-glow-grayscale.png){width="128px"}

![](../../../../../../assets/shape-glow.png){width="128px"}

## 모양 광선(회색 음영)

**내부:** *필터/효과*

**중간**

</td>
<td style="border: 0;" valign="top">

## 설명

입력 마스크(회색 음영 버전) 또는 알파 채널이 있는 모양(색상 버전) 주위에 부드러운 광선을 만듭니다. [광선](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/glow/glow.md)과 비교하여 이 기능은 더 많은 컨트롤을 사용하여 더 완벽한 효과이므로 다른 2D 이미지 편집 소프트웨어와 더 유사한 방식으로 작동합니다.

## 매개변수

* **모드**: *소프트, 정밀*&#x200B;두 정확도 모드 사이를 전환합니다.
* **폭**: *-1.0 - 1.0*&#x200B;광선이 도달하는 거리를 제어합니다.
* **스프레드**: *0.0 - 1.0*&#x200B;흐림 효과를 위한 잘라내기/임계값. 광선이 모양에 가깝게 단단하게 표시됩니다.
* **불투명도**: *0.0 - 1.0*\
  광선 효과에 대한 혼합 불투명도.
* 광선에 적용할 **(그림자) 색상**: *(색상 값)*색상 색조입니다.
* **마스크 색상**: *(색상 값) *(회색 음영 버전만)**투명도 매핑 출력에 사용할 단색.
* **입력이 미리 곱해졌습니다**: *False/True *(색상 버전만 해당)**입력이 미리 곱해졌다고 가정해야 하는지 여부.
* **미리 곱하기 출력**: *False/True*&#x200B;미리 곱해야 하는지 여부를 지정합니다.

| <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid_items_grid-cell1_position-par_dx_table_row-r0-column-c0_image" src="../../../../../../assets/shapeglow-ex.png" width="300px"/></div> |
| --- |
|  |

</td>
</tr>
</table>
