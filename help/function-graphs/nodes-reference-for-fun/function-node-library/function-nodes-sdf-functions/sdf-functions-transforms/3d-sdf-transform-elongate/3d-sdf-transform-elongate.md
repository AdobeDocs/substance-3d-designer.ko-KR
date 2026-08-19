---
title: 늘이기
description: Designer > Substance 합성 그래프 > Substance 합성 그래프의 노드 참조 > 노드 라이브러리 > SDF 함수 > 변형 > 연장
source-git-commit: 68fa6e85c7fe7318a4dafd491f9dc9e945a458e2
workflow-type: tm+mt
source-wordcount: '132'
ht-degree: 1%

---


# 늘이기

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![늘이기 아이콘](./3d-sdf-transform-elongate.png "늘이기")

<b>내부:</b> SDF 함수 > 변형

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 설명

조정 가능한 위치에서 SDF 모양을 늘립니다.<br>조정 가능한 슬라이스에서 시작하여 SDF 모양의 볼륨을 효과적으로 선형적으로 확장합니다.

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
| <b>신장</b> *Float3* | X, Y, Z축의 신장 길이 |
| <b>가운데 위치</b> *Float3* | 모양이 길어질 세계 공간 위치<br>즉, 길어지는 슬라이스의 위치입니다. |
| <b>P</b> *Float3* | 변형된 세계 공간 위치. <b>오프셋 P</b> 및 <b>회전 P</b> 노드를 사용하여 추가 변형을 적용하려면 이 입력을 사용합니다.<br><br><i>기본값: 변환되지 않은 월드 공간 위치.</i> |
