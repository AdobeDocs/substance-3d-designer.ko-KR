---
helpx_url: "https://helpx.adobe.com/kr/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/adjustments/color-match.html"
breadcrumb-title: ''
description: 색상 일치 노드를 사용하면 텍스처 간 색상을 일치시켜 일관된 색상 팔레트를 만들고 텍스처를 조화시킬 수 있습니다.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Adjustments > Color Match
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 색상 일치
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '290'
ht-degree: 1%

---


# 색상 일치

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](color-match.resources/color-match-3.png){width="128px"}

<b>내부:</b> 필터 > 조정

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 설명

정의된 *소스 색상* 범위를 *대상 색상* 범위와 일치시키려고 합니다. 소스 및 대상을 정의하는 입력 슬롯이 지원됩니다.

더 단순한 버전에 대해서는 [색상 범위 바꾸기](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/replace-color-range/replace-color-range.md) 또는 [색상 바꾸기](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/replace-color/replace-color.md)를 참조하세요.

</td>
</tr>
</table>

<a name="inputs"></a>

## 입력

|  |  |
|:---|:---|
| <b>입력</b> <i>색상 입력</i> | 결과를 수정하기 위한 기본 입력입니다. |
| <b>소스 색상</b> <i>색상 입력</i> | 소스 색상에 대한 입력 슬롯입니다. &#39;소스 색상 모드&#39;가 *입력*(으)로 설정된 경우에만 사용됩니다. |
| <b>대상 색상</b> <i>색상 입력</i> | 대상 색상에 대한 입력 슬롯입니다. &#39;대상 색상 모드&#39;가 *입력*(으)로 설정된 경우에만 사용됩니다. |

<a name="parameters"></a>

## 매개변수

|  |  |
|:---|:---|
| <b>소스 색상 모드</b> <i>평균, 매개 변수, 입력</i> | [소스 색상]이 입력 이미지의 평균을 내서 정의되는지, 매개 변수를 설정해서 정의되는지, 아니면 입력 슬롯을 사용해서 정의되는지를 설정합니다. |
| <b>소스 색상</b> <i>(색상 값)</i> | [소스 색상 모드]가 *매개 변수*(으)로 설정되어 있으면 이 매개 변수는 소스 색상을 결정합니다. |
| <b>대상 색상 모드</b> <i>매개 변수, 이미지 입력</i> | [소스 색상]이 입력 이미지의 평균을 내서 정의되는지, 매개 변수를 설정해서 정의되는지, 입력 슬롯을 이용해서 정의되는지를 설정합니다. |
| <b>대상 색상</b> <i>(색상 값)</i> | 대상 색상 모드가 *매개 변수*(으)로 설정된 경우 이 매개 변수는 대상 색상을 결정합니다. |
| <b>사용자 지정 색상 변형</b> <i>거짓/참</i> | 추가 색상 변형을 활성화합니다. |
| <b>색상 변형</b> | 활성화된 경우 색조, 색차 또는 광도 변화를 결과로 설정합니다. |
| <b>마스크 사용</b> <i>거짓/참</i> | 아래의 마스크 모드에 따라 마스크 입력 또는 출력의 사용을 전환합니다. |
| <b>마스크 모드</b> <i>매개 변수, 입력</i> | [매개 변수 모드]에서는 색상이 변경된 위치를 자세히 설명하는 마스크를 출력합니다. 입력 모드를 사용하면 마스크에서 색상 일치 효과의 강도를 제어할 수 있습니다. |
| <b>마스크</b> | 결과 마스크를 매끄럽게 하고 흐리게 만드는 추가 컨트롤과 함께 색상 일치 효과가 적용된 위치를 정확하게 보여 주는 마스크를 출력합니다. |
