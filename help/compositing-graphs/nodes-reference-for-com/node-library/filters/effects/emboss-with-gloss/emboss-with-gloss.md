---
helpx_url: "https://helpx.adobe.com/kr/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/emboss-with-gloss.html"
breadcrumb-title: ''
description: '[광택 있는 엠보스] 노드를 사용하면 텍스처에 깊이와 광택을 추가하기 위해 광택 맵으로 엠보스 효과를 만들 수 있습니다.'
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Emboss With Gloss
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 광택이 있는 엠보스
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '149'
ht-degree: 2%

---


# 광택이 있는 엠보스

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/emboss-with-gloss.png){width="128px"}

## 광택이 있는 엠보스

**내부:** *필터/효과*

**중간**

</td>
<td style="border: 0;" valign="top">

## 설명

색상 및 Height 입력에 광택(Specular 반사)이 추가된 엠보싱 효과를 수행합니다. 기본적으로 Height 정보를 기반으로 이미지에 가짜 조명을 추가합니다. 텍스처에 반영된 조명을 필요로 하는 일부 텍스처 스타일에 유용합니다.

더 많은 옵션이 있는 버전을 보려면 [Uber Emboss](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/uber-emboss/uber-emboss.md)를 참조하세요. [엠보스](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/emboss/emboss.md)의 간단한 원자 버전도 있습니다.

## 매개변수

### 입력

* **색상**: *색상 입력*
* **Height**: *회색 음영 입력*

### 매개변수

* **밝은 영역 색상**: *(색상 값)*Specular 밝은 영역의 색상입니다.
* **그림자 색상**: *(색상 값)*어두운 영역/밝지 않은 영역에서 사용되는 색상입니다.
* **광택**: *0.0 - 0.5*&#x200B;광택 밝은 영역 크기.
* **강도**: *0.0 - 10.0*&#x200B;밝은 영역의 강도.
* **조명 각도**: *0.0 - 1.0*\
  (가짜) 빛의 입사각입니다.

## 예제 이미지

|  |
| --- |
| 이 페이지에 첨부된 이미지가 없습니다. |

</td>
</tr>
</table>
