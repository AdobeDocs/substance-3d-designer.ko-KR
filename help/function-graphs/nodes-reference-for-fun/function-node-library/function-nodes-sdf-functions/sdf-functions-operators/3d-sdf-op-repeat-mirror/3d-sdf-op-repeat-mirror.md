---
title: 미러링 범위 반복
description: Designer > Substance 합성 그래프 > Substance 합성 그래프의 노드 참조 > 노드 라이브러리 > SDF 함수 > 연산자 > 미러 범위 반복
source-git-commit: 68fa6e85c7fe7318a4dafd491f9dc9e945a458e2
workflow-type: tm+mt
source-wordcount: '246'
ht-degree: 0%

---


# 미러링 범위 반복

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![미러링 범위 반복 아이콘](./3d-sdf-op-repeat-mirror.png "미러링 범위 반복")

<b>내부:</b> SDF 함수 > 연산자

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 설명

SDF 모양을 X, Y 및 Z 양축 또는 음축의 일정한 간격으로 여러 번 미러링하고 복제합니다.<br>이 연산자는 모양을 반복할 때마다 모양을 미러링합니다. 그러면 시각적으로 모양의 원본 방향과 뒤집힌 사본이 번갈아가며 표시됩니다.

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
| <b>금액 +</b> *정수3* | 양의 X, Y, Z축을 따라 복제한 양입니다.<br><br><i>기본값: (2, 0, 0)</i> |
| <b>금액 -</b> *정수3* | 음수 X, Y, Z축을 따라 복제한 양입니다.<br><br><i>기본값: (2, 0, 0)</i> |
| <b>간격</b> *Float3* | 각 복제 사이의 공백입니다.<br><br>간격은 큐빅 도우미에 의해 시각화됩니다. 큐빅 도우미는 X, Y 및 Z 방향으로 중복된 항목 사이의 간격을 나타냅니다. 간격은 <b>원점 위치</b>에서 시작되고 대칭으로 증가합니다.<br><br><i>기본값: (2, 2, 2)</i> |
| <b>원본 위치</b> *Float3* | 복제할 SDF 모양의 가운데를 정의합니다.<br><br>원점 위치는 큐빅 도우미의 가운데 위치로 시각화됩니다.<br><br><i>기본값: (0, 0, 0)</i> |
| <b>P</b> *Float3* | 변형된 세계 공간 위치. <b>오프셋 P</b> 및 <b>회전 P</b> 노드를 사용하여 추가 변형을 적용하려면 이 입력을 사용합니다.<br><br><i>기본값: 변환되지 않은 월드 공간 위치.</i> |
