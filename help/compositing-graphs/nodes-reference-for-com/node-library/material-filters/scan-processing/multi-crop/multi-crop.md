---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/scan-processing/multi-crop.html"
breadcrumb-title: ''
description: 다중 자르기 노드를 사용하여 스캔한 재질을 효율적으로 처리하기 위해 여러 텍스처 채널을 동시에 자릅니다.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > Scan Processing > Multi Crop
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 다중 자르기
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '185'
ht-degree: 1%

---


# 다중 자르기

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/crop-multi.png){width="128px"}

![](../../../../../../assets/crop-multi-grayscale.png){width="128px"}

## 다중 자르기(회색 음영)

**내부:** *재질 필터/스캔 처리*

**중간**

</td>
<td style="border: 0;" valign="top">

## 설명

자르기의 멀티 채널 버전입니다. 이미지에서 영역을 자르고 주로 다각 사진에 사용하기 위한 것으로, [다각 대 알베도](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/multi-angle-to-albedo/multi-angle-to-albedo.md) 또는 [다각 대 일반](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/multi-angle-to-normal/multi-angle-to-normal.md)과 결합됩니다.

>[!NOTE]
>
> 자세한 내용은 원본 [자르기](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/crop/crop.md)를 참조하세요.

## 매개변수

### 매개변수

* **입력 수**: *1 - 8*&#x200B;병렬로 처리할 입력 수를 설정합니다.
* **입력 크기**: *0 - 8192*&#x200B;이미지 해상도 및 비율을 입력합니다. 정사각형이 아닌 이미지에 매우 중요합니다.
* **배경**: *(색상 값) / (회색 음영 값)*자르기로 가려지지 않은 영역에 대한 배경 균일 값.
* **변환**: *(변환 행렬)*\
  결과를 회전하고 크기를 조절합니다. 캔버스와 직접 상호 작용하여 결과를 수정할 수 있습니다.
* **오프셋**: *0.0 - 1.0*\
  결과를 이동하거나 변환합니다. 캔버스와 직접 상호 작용하여 결과를 수정할 수 있습니다.
* **일반(색상 버전에만 해당)**: *False/True*&#x200B;입력을 표준 맵으로 처리할지 여부.

## 예제 이미지

|  |
| --- |
| 이 페이지에 첨부된 이미지가 없습니다. |

</td>
</tr>
</table>
