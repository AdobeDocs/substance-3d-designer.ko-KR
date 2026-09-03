---
helpx_url: "https://helpx.adobe.com/kr/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/3d-view-library/hdri-tools/hdr-merge.html"
breadcrumb-title: ''
description: HDR 병합 노드를 사용하여 합성 환경 맵을 만들기 위해 여러 HDR 이미지를 단일 파노라마로 병합합니다.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > 3D View (Library) > HDRI Tools > HDR Merge
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: HDR 병합
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '98'
ht-degree: 13%

---


# HDR 병합

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](hdr-merge.resources/hdr-merge-01.png){width="200px"}

<b>내부:</b> 3D 보기 > HDRI 도구

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 설명

여러 사진 노출을 병합하여 High Dynamic Range 이미지를 만듭니다. 첫 번째 입력은 가장 노출이 부족한 이미지입니다.

</td>
</tr>
</table>

<a name="inputs"></a>

## 입력

|  |  |
|:---|:---|
| <b>입력 1-16</b> <i>색상 입력</i> | 입력 이미지. 사용 가능한 양은 매개변수에 따라 다릅니다. |

<a name="parameters"></a>

## 매개변수

|  |  |
|:---|:---|
| <b>입력</b> <i>2 - 16</i> | 사용 가능한 입력 양을 설정합니다. |
| <b>노출 델타(EV)</b> <i>0.0 - 4.0</i> | 이미지 간 해석을 위해 노출의 차이를 설정합니다. |
| <b>흰 점</b> <i>0.0 - 13.0</i> | 최종 결과에 대해 일부 조정을 수행하려면 흰 점을 설정합니다. |
