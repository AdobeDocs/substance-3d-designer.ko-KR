---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/adjustments/color-match.html"
breadcrumb-title: ''
description: '[색상 일치] 노드를 사용하면 일관된 색상 팔레트를 만들고 텍스처를 조화롭게 만들기 위해 텍스처 간에 색상을 일치시킬 수 있습니다.'
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Adjustments > Color Match
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 색상 일치
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '300'
ht-degree: 1%

---


# 색상 일치

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/color-match-3.png){width="128px"}

## 색상 일치

**내부:** *필터/조정*

**복합**

</td>
<td style="border: 0;" valign="top">

## 설명

정의된 *소스 색상* 범위를 *대상 색상* 범위와 일치시키려고 합니다. 소스 및 대상을 정의하는 입력 슬롯이 지원됩니다.

더 단순한 버전에 대해서는 [색상 범위 바꾸기](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/replace-color-range/replace-color-range.md) 또는 [색상 바꾸기](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/replace-color/replace-color.md)를 참조하세요.

## 매개변수

### 입력

* **입력**: *색상* 입력\
  결과를 수정하기 위한 기본 입력입니다.
* **소스 색상**: *색상 입력*\
  소스 색상에 대한 입력 슬롯입니다. &#39;소스 색상 모드&#39;가 *입력*(으)로 설정된 경우에만 사용됩니다.
* **대상 색상**: *색상 입력*&#x200B;대상 색상에 대한 입력 슬롯. &#39;대상 색상 모드&#39;가 *입력*(으)로 설정된 경우에만 사용됩니다.

### 매개변수

* **소스 색상 모드**: *평균, 매개 변수, 입력*&#x200B;소스 색상이 입력 이미지의 평균을 내거나 매개 변수를 설정하거나 입력 슬롯을 사용하여 정의되는지 여부를 설정합니다.
* **소스 색상**: *(색상 값)*&#x200B;소스 색상 모드가 *매개 변수*(으)로 설정된 경우 이 매개 변수는 소스 색상을 결정합니다.
* **대상 색상 모드**: *매개 변수, 이미지 입력*&#x200B;소스 색상이 입력 이미지의 평균을 내거나 매개 변수를 설정하거나 입력 슬롯을 사용하여 정의되는지 여부를 설정합니다.
* **대상 색상**: *(색상 값)*&#x200B;대상 색상 모드가 *매개 변수*(으)로 설정된 경우 이 매개 변수는 대상 색상을 결정합니다.
* **사용자 지정 색상 변형**: False/True\
  추가 색상 변형을 활성화합니다.
* **색상 변형**\
  활성화된 경우 색조, 색차 또는 광도 변화를 결과로 설정합니다.
* **마스크 사용**: *False/True*\
  아래의 마스크 모드에 따라 마스크 입력 또는 출력의 사용을 전환합니다.
* **마스크 모드**: *매개 변수, 입력*&#x200B;매개 변수 모드에서는 색상이 변경된 방식을 자세히 설명하는 마스크를 출력합니다. 입력 모드를 사용하면 마스크에서 색상 일치 효과의 강도를 제어할 수 있습니다.
* **마스크**\
  결과 마스크를 매끄럽게 하고 흐리게 만드는 추가 컨트롤과 함께 색상 일치 효과가 적용된 위치를 정확하게 보여 주는 마스크를 출력합니다.

## 예제 이미지

|  |
| --- |
| 이 페이지에 첨부된 이미지가 없습니다. |

</td>
</tr>
</table>
