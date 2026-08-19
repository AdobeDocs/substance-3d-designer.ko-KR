---
title: 라운딩
description: Designer > Substance 합성 그래프 > Substance 합성 그래프의 노드 참조 > 노드 라이브러리 > SDF 함수 > 연산자 > 라운딩
source-git-commit: 68fa6e85c7fe7318a4dafd491f9dc9e945a458e2
workflow-type: tm+mt
source-wordcount: '85'
ht-degree: 2%

---


# 라운딩

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![반올림 아이콘](./3d-sdf-op-rounding.png "반올림")

<b>내부:</b> SDF 함수 > 연산자

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 설명

SDF 모양을 확장하여 부풀리고 굵은 가장자리를 매끄럽게 합니다.

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
| <b>SDF</b> *부동* | 입력 SDF 셰이프입니다. |
| <b>반경</b> *부동* | 모양의 가장자리에 적용된 둥근 호의 반경입니다.<br><br><i>참고:</i> 둥근 반경이 교차하는 곳에 단단한 가장자리가 나타날 수 있습니다.<br><br><i>기본값: 0.05</i> |
