---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/flood-fill-to-index.html"
breadcrumb-title: ''
description: '[인덱스 Flood Fill] 노드를 사용하여 번호가 매겨지고 레이블이 지정된 패턴을 만들기 위한 인덱스 값으로 영역을 채웁니다.'
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Flood Fill to Index
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 색인으로 Flood Fill
user-guide-description: ''
user-guide-title: ''
source-git-commit: 4f8830fa9ab6012f0a7ba5054eb171b151c44874
workflow-type: tm+mt
source-wordcount: '201'
ht-degree: 2%

---


# 색인으로 Flood Fill

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/floodfill-index.png){width="200px"}

## 색인으로 Flood Fill

**내부:** *필터/효과*

**복합**

</td>
<td style="border: 0;" valign="top">

## 설명

[Flood Fill에서 인덱스]를 선택하면 모든 Flood Fill 셀이 인덱스 번호에 따른 값으로 변환되며 왼쪽 상단에는 0부터 시작합니다. 이는 정규화된 형태(0.0 내지 1.0, Flood Fill에 의해 발견되는 수의 셀들로 나누기)로 또는 HDR, 언클램핑된 값(0 내지 n, 여기서 n은 셀의 수임)으로 회색 음영 색조를 반환하는데 사용될 수 있다.

또한 색인에 Flood Fill을 사용하면 [값](../../../../../values-compositing-graphs/values-in-substance-compositing-graphs.md)이 사용되므로 발견된 모양의 양과 선택적 내부 데이터 테이블이 반환됩니다.

### 입력

* **Flood Fill 상자**: *색상 입력*&#x200B;표준 Flood Fill 입력 맵. 필수 여부.
* **특수 모양 정보**: *색상 입력*&#x200B;추가 Flood Fill 맵, 이전 Flood Fill 노드에서 명시적으로 활성화해야 하며 연결해야 합니다!

### 매개변수

* **출력**: *정규화, 정수*&#x200B;출력 값이 LDR 0-1 범위에 있는지 HDR 0-n 범위에 있는지 확인합니다.
* **다음보다 작은 모양 무시**: *0.0 - 1.0*&#x200B;작은 모양을 무시하기 위한 허용치 값.
* **Flood Fill 데이터 테이블 표시**: *False/True*&#x200B;고급 사용을 위한 추가(디버그) 데이터를 반환합니다.

## 예

![](../../../../../../assets/flood-fill-ex02.jpg)

</td>
</tr>
</table>
