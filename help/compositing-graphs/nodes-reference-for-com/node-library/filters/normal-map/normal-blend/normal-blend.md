---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/normal-map/normal-blend.html"
breadcrumb-title: ''
description: 표준 블렌드(Normal Blend) 노드를 사용하면 표준 맵을 함께 블렌딩하여 표면 세부 사항 간의 부드러운 전환을 만들 수 있습니다.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Normal Map > Normal Blend
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 표준 혼합
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '160'
ht-degree: 2%

---


# 표준 혼합

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/normal-blend.png){width="128px"}

## 표준 혼합

**내부:** *필터/표준 맵*

**중간**

</td>
<td style="border: 0;" valign="top">

## 설명

[표준 혼합]을 사용하면 선택적 마스크를 사용하여 두 개의 표준 맵을 혼합하고 모든 값을 표준화 상태로 유지할 수 있습니다. [원자 혼합 노드](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/blend/blend.md)와 크게 다르지 않지만 표준 맵에 대한 내부 계산을 추가했습니다.

[표준 혼합]은 표준 맵을 결합(오버레이)하기 위한 것이 아닙니다. 표준 맵에서는 위쪽 맵이 아래쪽 맵에 디테일을 추가합니다. 대신 [일반 결합](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/normal-map/normal-combine/normal-combine.md)을 사용하십시오.

## 매개변수

### 입력

* **NormalFG**: *색상 입력*\
  전경/위쪽 표준 맵
* **NormalBG**: *색상 입력*\
  배경/하단 표준 맵.
* **마스크**: *회색 음영 입력*\
  노드의 효과를 마스킹하는 데 사용되는 마스크 슬롯입니다. &quot;마스크 사용&quot; 매개 변수로 전환할 수 있습니다.

### 매개변수

* **불투명도**: *0.0 - 1.0*\
  전경과 배경 간 불투명도 혼합
* **마스크 사용**: *False/True*\
  마스크 맵 사용을 설정하거나 해제합니다.

## 예제 이미지

![](../../../../../../assets/normalblend-ex.gif)

*(.gif 형식은 예제에서 디더링을 도입하며 응용 프로그램 내 결과는 매끄럽습니다.)*

</td>
</tr>
</table>
