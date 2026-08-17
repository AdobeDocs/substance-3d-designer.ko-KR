---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/blending/switch.html"
breadcrumb-title: ''
description: 조건부 텍스처 선택을 위해 마스크를 기준으로 두 입력 텍스처 간을 전환하려면 [전환] 노드를 사용합니다.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Blending > Switch
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 전환
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '139'
ht-degree: 4%

---


# 전환

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/switch-1.png){width="128px"}

![](../../../../../../assets/switch-grayscale.png){width="128px"}

## 전환(회색 음영)

**내부:** *필터/혼합*

**단순**

</td>
<td style="border: 0;" valign="top">

## 설명

간단한 2위치 스위치 노드 Switch 매개 변수 설정에 따라 Input 1 또는 Input 2를 반환합니다. 결과가 수정되지 않았습니다. 고급 버전은 [다중 스위치](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/blending/multi-switch/multi-switch.md)를 참조하세요.

전체 옵션 선택에 대해 복잡한 드롭다운 목록이 아닌 단일 버튼만 있으면 되는, 그래프에 부울(True/False) 선택 사항을 표시하는 데 매우 유용합니다.

중요: 입력에 적합한 버전을 사용해야 합니다. 색상 입력에는 &quot;전환&quot;을 사용하고, 회색 음영 입력에는 &quot;회색 음영 전환&quot;을 사용합니다.

## 매개변수

### 입력

* **입력 1(True)**: *색 또는 회색 음영 입력*
* **입력 2(False)**: *색상 또는 회색 음영 입력*

### 매개변수

* **전환**: *False/True*&#x200B;입력 1(True)과 2(False) 사이를 전환합니다.

## 예제 이미지

</td>
</tr>
</table>
