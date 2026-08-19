---
title: 형태
description: Designer > Substance 합성 그래프 > Substance 합성 그래프의 노드 참조 > 노드 라이브러리 > SDF 함수 > 연산자 > 형태
source-git-commit: 68fa6e85c7fe7318a4dafd491f9dc9e945a458e2
workflow-type: tm+mt
source-wordcount: '102'
ht-degree: 1%

---


# 형태

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![형태 아이콘](./3d-sdf-op-morph.png "형태")

<b>내부:</b> SDF 함수 > 연산자

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 설명

조정 가능한 혼합 계수에 따라 기본 SDF 모양과 대상 SDF 모양 사이의 선형 보간을 반환합니다.

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
| <b>기본 SDF</b> *부동* | 기본 SDF 모양입니다. |
| <b>대상 SDF</b> *부동* | 대상 SDF 셰이프입니다. |
| <b>혼합 계수</b> *부동* | 입력 모양을 모핑하는 데 사용되는 혼합 계수입니다. 여기서 0은 기본 모양이고, 1은 대상 모양입니다. |
