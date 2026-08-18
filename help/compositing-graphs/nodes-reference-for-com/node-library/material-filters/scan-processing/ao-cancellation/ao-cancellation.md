---
helpx_url: "https://helpx.adobe.com/kr/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/scan-processing/ao-cancellation.html"
breadcrumb-title: ''
description: AO 취소 노드를 사용하여 깨끗한 텍스처 처리를 위해 스캔한 재질에서 주변 오클루전을 제거합니다.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > Scan Processing > AO Cancellation
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: AO 취소
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '145'
ht-degree: 1%

---


# AO 취소

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/ao-cancel.png){width="128px"}

## AO 취소

**내부:** *재질 필터/스캔 처리*

**단순**

</td>
<td style="border: 0;" valign="top">

## 설명

이 노드는 별도의 AO 맵 입력을 기반으로 알베도(기본 색상) 맵에서 앰비언트 오클루전 조명 정보를 제거하려고 시도합니다. 알베도 정보가 PBR로 정확하고 대부분 (강한) 조명 정보가 없는지 확인하는 데 사용할 수 있습니다.

스캔한 메쉬에서 AO 맵을 불러올 때 또는 Height 또는 일반 정보에서 생성된 AO 맵을 불러올 때 유용한 노드입니다.

## 매개변수

* **AO 취소**: *0.0 - 1.0*&#x200B;조명 정보를 제거하는 강도.
* **AO 채도**: 조명이 제거된 영역에 대한 *0.0 - 1.0*(De)채도 보상. 이를 사용하여 어두운 영역에서 색상 손실을 되돌릴 수 있습니다.

## 예제 이미지

|  |
| --- |
| 이 페이지에 첨부된 이미지가 없습니다. |

</td>
</tr>
</table>
