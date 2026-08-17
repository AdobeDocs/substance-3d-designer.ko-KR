---
title: 셸
description: Designer > Substance 합성 그래프 > Substance 합성 그래프의 노드 참조 > 노드 라이브러리 > SDF 함수 > 연산자 > 셸
source-git-commit: 68fa6e85c7fe7318a4dafd491f9dc9e945a458e2
workflow-type: tm+mt
source-wordcount: '84'
ht-degree: 4%

---


# 셸

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![셸 아이콘](./3d-sdf-op-shell.png "셸")

<b>내부:</b> SDF 함수 > 연산자

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 설명

SDF 모양을 빈 공간으로 만들고 Thickness을 조정하여 결과 엔벨로프를 만들 수 있습니다.

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
| <b>Thickness</b> *부동* | 셸의 Thickness은 안쪽과 바깥쪽으로 모두 적용됩니다.<br>Thickness이 증가할 때 셸이 둥글게 됩니다.<br><br><i>기본값: 0.02</i> |
