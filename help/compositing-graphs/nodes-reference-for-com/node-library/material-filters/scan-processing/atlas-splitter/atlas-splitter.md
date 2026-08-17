---
helpx_url: "https://helpx.adobe.com/kr/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/scan-processing/atlas-splitter.html"
breadcrumb-title: ''
description: Atlas Splitter 노드를 사용하여 스캔한 재료를 처리하기 위해 텍스처 아틀라스를 개별 텍스처로 분할합니다.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > Scan Processing > Atlas Splitter
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Atlas Splitter
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '386'
ht-degree: 0%

---


# Atlas Splitter

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![노드 아이콘](../../../../../../assets/atlas-splitter.png "노드 아이콘")

<b>인:</b> 재질 필터/스캔 처리

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 설명

아틀라스 이미지 입력을 가져와 모든 개별 요소를 *개별 재질*(으)로 분할합니다.

또한 모든 요소를 재구성하여 그리드로 이동할 때도 사용할 수 있습니다.

노드는 [Flood Fill](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/flood-fill/flood-fill.md) 노드의 고급 응용 프로그램으로 작동합니다.

</td>
</tr>
</table>

## 매개변수

<b>격자 보기</b> *부울*\
감지된 모든 모양을 격자에 표시합니다.

<b>격자 불투명도</b> *부동*\
격자 보기가 True일 때 격자 선의 불투명도를 설정합니다. 디버그 옵션

<b>격자 선택 불투명도</b> *부동*\
격자 보기가 True인 경우 격자 선택 영역의 불투명도를 강조 표시합니다. 디버그 옵션

<b>자동 크기 조절</b> *부울*\
자동으로 격자 셀에 맞게 모양 크기를 조정합니다.

<b>자동 자르기</b> *부울*\
빈 공간을 최소화하기 위해 가장 큰 모양에 따라 출력 크기를 자동으로 자릅니다.

<b>모양 선택</b> *정수*\
격자 보기에서는 강조 표시된 셀이 설정되고 격자 보기 외부에서는 반환된 셀이 설정됩니다.

<b>다음보다 작은 모양 무시</b> *부동 소수점*\
대각선 크기가 지정된 값보다 작은 모양을 무시합니다.

<b>자동 회전</b> *부울*\
해당 테두리 상자 크기 비율에 따라 모양을 자동으로 회전합니다.

<b>회전</b> *부동*\
전체 모양 회전 각도

<b>입력 일반 형식</b> *정수*\
입력 형식을 표준으로 설정합니다. 잘못된 형식을 설정하면 잘못된 결과가 나옵니다.

<b>불투명도 마스크 축소</b> *정수*\
잠재적 노이즈나 격리된 픽셀을 제거하기 위해 불투명도 마스크를 축소합니다. 원치 않는 모양이 감지되지 않도록 하고 성능을 향상시킵니다.

<b>확장 너비</b> *부동*\
[표준] 및 [Height]을 제외한 모든 채널에서 [불투명도] 마스크를 기반으로 확장 효과를 적용합니다.

<b>추가 입력 사용</b> *부울*\
포함되지 않은 추가 맵에 대해 사용자 1 및 사용자 2 입력 및 설정을 사용할 수 있도록 합니다.

<b>사용자 지정 배경색</b> *부울*\
해당 레이어 내용의 확장 대신 사용자 정의 배경색을 선택할 수 있습니다.

<b>기본 색상 배경색</b> *부동 소수점3*\
기본 색상에 대한 사용자 정의 BG 색상.

<b>표준 배경색</b> *부동 소수점3*\
표준 맵에 대한 사용자 정의 배경색입니다.

<b>금속성 배경색</b> *부동*\
금속에 대한 사용자 정의 BG 색상.

<b>거칠기 배경색</b> *부동*\
거칠기에 사용자 정의 BG 색상

<b>Height 배경색</b> *부동*\
Height을 위한 사용자 정의 배경색

<b>사용자 1 배경색</b> *부동*\
사용자 정의 사용자 1 맵에 대한 사용자 정의 배경색

사용자 정의 사용자 1 맵에 대한 <b>사용자 2 배경색</b> *부동*&#x200B;사용자 정의 배경색

## 예
