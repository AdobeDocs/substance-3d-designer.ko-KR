---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/3d-texture-sdf.html"
breadcrumb-title: ''
description: 3D 텍스처 SDF 노드를 사용하여 매끄러운 모양과 효과를 만들기 위해 3D 데이터에서 서명된 거리 필드 텍스처를 생성합니다.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > 3D Texture SDF
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 3D 텍스처 SDF
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '142'
ht-degree: 2%

---


# 3D 텍스처 SDF

<table>
<tr style="border: 0;">
<td width="41.60%" style="border: 0;" valign="top">

![](../../../../../../assets/3dtexturesdf.png){width="200px"}

**내부:** *필터/효과*

**단순**

</td>
<td width="58.30%" style="border: 0;" valign="top">

## 설명

**3D 텍스처 SDF** 노드는 모양의 *볼륨*&#x200B;의 조각들을 나타내는 **입력**&#x200B;의 *3D 텍스처* 마스크에서 모양의 *부호 있는 거리 필드*&#x200B;를 생성합니다.

</td>
</tr>
</table>

## 매개변수

### 입력

* **마스크 입력** *회색 음영*\
  모양의 *볼륨*&#x200B;의 조각을 나타내는 *3D 텍스처* 마스크입니다.

### 매개변수

* **임계값** *부동*\
  모양 볼륨이 *페이딩 그레이디언트*&#x200B;로 기술되면 모양의 *표면*&#x200B;이 *검색*&#x200B;되는 그레이디언트 값을 설정합니다.
* **출력** *정수*\
  출력해야 하는 거리 필드의 유형:
  * *거리 필드*: 셰이프의 *외부* 거리를 설명하는 거리 필드를 출력합니다.
  * *부호 거리 필드*: 모양 *외부*(양수) 및 *내부*(음수)의 거리를 설명하는 거리 필드를 출력합니다.

## 예제 이미지

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/3dtexturesdf-variant.jpg){width="256px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../../../assets/3dtexturesdf-variant2.jpg){width="256px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../../../assets/3dtexturesdf-node.png){width="256px"}

</td>
</tr>
</table>
