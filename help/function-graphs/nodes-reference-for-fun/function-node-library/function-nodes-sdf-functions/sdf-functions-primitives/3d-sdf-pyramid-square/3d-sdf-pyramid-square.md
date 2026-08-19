---
title: 피라미드 정사각형
description: Designer > Substance 합성 그래프 > Substance 합성 그래프의 노드 참조 > 노드 라이브러리 > SDF 함수 > 프리미티브 > 피라미드 정사각형
source-git-commit: 68fa6e85c7fe7318a4dafd491f9dc9e945a458e2
workflow-type: tm+mt
source-wordcount: '138'
ht-degree: 1%

---


# 피라미드 정사각형

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![피라미드 정사각형 아이콘](./3d-sdf-pyramid-square.png "피라미드 정사각형")

<b>내부:</b> SDF 함수 > 기본

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 설명

Height과 베이스 위치를 조정할 수 있는 사각형 베이스가 있는 피라미드용 SDF 함수.

</td>
</tr>
</table>

<a name='inputs'></a>

>[!INFO]
> 
> SDF 함수와 관련된 개념 및 작업 과정에 대해 자세히 알아보려면 전용 페이지로 이동하십시오. [SDF 함수 작업](../../working-with-sdf-functions.md)

## 입력

|  |  |
| :--- | :--- |
| <b>Height</b> *부동* | 기본 피라미드의 꼭짓점의 Z-업 Height.<br><br><i>기본값: 1</i> |
| <b>기본 크기</b> *부동* | 피라미드의 기본 가장자리 길이입니다.<br>모든 가장자리의 길이가 같습니다.<br><br><i>기본값: 1</i> |
| <b>기본 위치</b> *Float3* | 피라미드 기반의 월드 공간 위치입니다.<br><br><i>기본값: (0, 0, 0)</i> |
| <b>P</b> *Float3* | 변형된 세계 공간 위치. <b>오프셋 P</b> 및 <b>회전 P</b> 노드를 사용하여 추가 변형을 적용하려면 이 입력을 사용합니다.<br><br><i>기본값: 변환되지 않은 월드 공간 위치.</i> |
