---
helpx_url: "https://helpx.adobe.com/kr/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/3d-view-library/hdri-tools/exposure-preview.html"
breadcrumb-title: ''
description: 최종 렌더링 전에 HDRI 환경에서 노출 조정을 미리 보려면 노출 미리 보기 노드를 사용합니다.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > 3D View (Library) > HDRI Tools > Exposure Preview
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 노출 미리 보기
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '102'
ht-degree: 1%

---


# 노출 미리 보기

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/hdr-exposure-preview.png){width="200px"}

## 노출 미리 보기

**내부:** *3D 보기/HDRI 도구*

**단순**

</td>
<td style="border: 0;" valign="top">

## 설명

노출 단계를 미리 볼 보조 노드입니다. 사용자는 최소 및 최대 값을 설정하며, 노드는 원래 입력의 여러 노출된 버전을 사용하여 훨씬 더 큰 이미지를 생성한다. 서로 다른 버전은 항상 가로로 누적되며, 양은 노드 또는 그래프의 해상도에 따라 달라집니다.

## 매개변수

* **최대 노출(EV)**: *-8.0 - 8.0*\
  가장 밝은 이미지의 가장 높은 노출입니다.
* **최소 노출(EV)**: *-8.0 - 8.0*&#x200B;가장 어두운 아래쪽 이미지의 최소 노출.

## 예제 이미지

![](../../../../../../assets/exp-preview-ex.png)

</td>
</tr>
</table>
