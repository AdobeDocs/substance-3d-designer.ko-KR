---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/normal-map/normal-combine.html"
breadcrumb-title: ''
description: 표준 결합 노드를 사용하여 표면 세부 사항 및 세부 사항 레이어를 위해 여러 개의 표준 맵을 결합합니다.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Normal Map > Normal Combine
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 표준 결합
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '139'
ht-degree: 4%

---


# 표준 결합

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](normal-combine.resources/normal-combine-01.png){width="128px"}

<b>내부:</b> 필터 > 표준 맵

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 설명

표준 두 노멀 맵의 세부 사항을 수학적으로 정확하게 결합합니다.

다른 2D 이미지 편집 소프트웨어의 잘 알려진 &quot;오버레이&quot; 방법과 유사하지만 내부적으로 약간 다르게 작동합니다(세 가지 옵션).

</td>
</tr>
</table>

이 방법은 2D로 생성된 표준 맵 세부 정보를 베이킹된 맵에 추가하는 가장 좋은 방법입니다.

마스크 등을 사용하여 두 노멀 맵의 세부 사항을 결합하지 않고 혼합하려면 [표준 혼합](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/normal-map/normal-blend/normal-blend.md)를 사용해야 합니다.

<a name="inputs"></a>

## 입력

|  |  |
|:---|:---|
| <b>일반 2</b> <i>색상</i> | 설명 |
| <b>보통 1</b> <i>색상</i> | 설명 |

<a name="parameters"></a>

## 매개변수

|  |  |
|:---|:---|
| <b>기법</b> *정수* | 사용할 내부 혼합 기술을 설정하고 품질에 대한 속도에서 거래합니다.<br><br>*- 화이트아웃(저품질)<br>* 채널 혼합(고품질)<br>* 디테일 지향(고품질)* |

## 예
